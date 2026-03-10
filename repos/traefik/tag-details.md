<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.40`](#traefik21140)
-	[`traefik:2.11.40-nanoserver-ltsc2022`](#traefik21140-nanoserver-ltsc2022)
-	[`traefik:2.11.40-windowsservercore-ltsc2022`](#traefik21140-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.10`](#traefik3610)
-	[`traefik:3.6.10-nanoserver-ltsc2022`](#traefik3610-nanoserver-ltsc2022)
-	[`traefik:3.6.10-windowsservercore-ltsc2022`](#traefik3610-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.40`](#traefikv21140)
-	[`traefik:v2.11.40-nanoserver-ltsc2022`](#traefikv21140-nanoserver-ltsc2022)
-	[`traefik:v2.11.40-windowsservercore-ltsc2022`](#traefikv21140-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.10`](#traefikv3610)
-	[`traefik:v3.6.10-nanoserver-ltsc2022`](#traefikv3610-nanoserver-ltsc2022)
-	[`traefik:v3.6.10-windowsservercore-ltsc2022`](#traefikv3610-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.40`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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

### `traefik:2.11.40` - linux; amd64

```console
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.40` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.40` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.40` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.40` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.40` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.40-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11.40-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.40-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:2.11.40-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

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

### `traefik:3.6` - unknown; unknown

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

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.10`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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

### `traefik:3.6.10` - linux; amd64

```console
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.10` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.10` - linux; riscv64

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

### `traefik:3.6.10` - unknown; unknown

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

### `traefik:3.6.10` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.10-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6.10-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.10-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:3.6.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
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
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9e134a2c629638bd7cf1d0e22ba56c4be2c8c44ae4080ce3db4cb7446cd28196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:9fc41089c3c97b97f99fddb1f4f32a1d9198b87f0cf1e5018d26d8cbc86e8067
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174301713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb1a915064167eeac02daa40e5b968d21dac934eb61bd6a38aaf660db943a6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:16:56 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Fri, 06 Mar 2026 19:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8799bf77c45f3fa053136d98622fa857db25d678ae677b0206b1609c47c7f4`  
		Last Modified: Fri, 06 Mar 2026 19:17:52 GMT  
		Size: 47.7 MB (47652668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d486061537dbb92089e5652fbb433a00376956e1973d71ecff9b4f6712bae50`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afa6e36c3bcdcfb27947fbe555c6a56f5f9fe44ea0e6a2ecf11ee84fe4c64c`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3674941e786831e1c86f30512d0d0de55baccd8dffb541a80345d4bfebcc104d`  
		Last Modified: Fri, 06 Mar 2026 19:17:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.40`

```console
$ docker pull traefik@sha256:2a2460731a47e9406dfdee0c52734b9b86509fe7e82e96ce06e91a49b83b1c71
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

### `traefik:v2.11.40` - linux; amd64

```console
$ docker pull traefik@sha256:7c1b20687bd3016e61b4a67f6b232c10881bc979ac8ed12cbda8e0b99fe4b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9f2a70652013f4d23ffc5970285be37d9b9c3ac5fe0ceef247d1c387d7058`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:53 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb782125a1abcf8626e8484795835eb6bf8a94ab7940cb3cc322f7bd5911e4`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 460.7 KB (460742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09053d701d61d367129b12f3a450d292c10c4e25a7ea86dff842cda04cdcca`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 46.8 MB (46845990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f76f76535ea04faf6d0e937b570756f4e17a944e5cda5f56fb1a43dd0bf768`  
		Last Modified: Fri, 06 Mar 2026 18:27:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:a0ddcd467528cc7ea1e6130fb1e5845b67630937e29f6c5bf8e95e6349f18225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff47d58e0c6bb211750328f73d05641889376d042e102ff0a4dcc27987dc9f73`

```dockerfile
```

-	Layers:
	-	`sha256:82db944a7dfa06c0a42dd0b0b9643812ab87be56050f8ad6fce6b0be3af6b272`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ccd378ae6288e9c528f7f9036452144948175a44102e16a0a38e7e950fdbb`  
		Last Modified: Fri, 06 Mar 2026 18:27:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.40` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d5417b3d406d5af26e1ff2f8506eb7c4535293086f28ef357761802ea97fdc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46891697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea39ffc05689e8ac886297c89203cba8c267719fc9ca120d3e2a845a73665f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeea259586436adfe00896552908cd8626e1af1b574c421c787c9e2ac5b1add`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec47292cf551720fb0f924479f352159f3aad6aaa1ced6a553a77022ac19360`  
		Last Modified: Fri, 06 Mar 2026 18:57:28 GMT  
		Size: 42.9 MB (42860269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a424129aab48c1e5cfa898c31a1eb349b6333ba6f85b0a1c29efdd1458cdc4`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:e25888b80cfa78c996f3eda7b5bd6d0e10ddeae69b810e54a8271fef84a3320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fdad2702e6b0dadfeaa581433586bc0266815c5ca44251ec5c83f337e78cc`

```dockerfile
```

-	Layers:
	-	`sha256:7ef1f00af45106e80e92e12fb344c1ef0311c6300d1c17f1184ee11c40faeac1`  
		Last Modified: Fri, 06 Mar 2026 18:57:26 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.40` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cdf08ac88bee0bf2737405c8e62b4b9855d468f85e180dc2be53d17a301dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042412a4cc9a4d67f34fe866362293c553903007c2b8cee422808b4bea72441`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:15 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7b4e0ab96fcef3518f20c952323977ca9f2de855c27fa6414d8e07ab20929`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 462.8 KB (462761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e03e016b4cf8b98b8821c6669bb328fb4f35e8f1e9a802113ea581bf727437`  
		Last Modified: Fri, 06 Mar 2026 18:29:41 GMT  
		Size: 42.1 MB (42134149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e15b76ab41b0aac39db4942cb27108981011365fa474d749607187ecdce704`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:6b498f84a1f5af72cc4466a19ea31a2a43ea1e548c71e7ed2173a5b309596c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29381ae7a4bd9b3cd48242882a99cf3a6721fc72dbc545e045a8511680579dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e90bbbfb52327b628fd017eb340a9d371e0db1b22854bd666592bc792cf72ba0`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234a53485d83b7ff250e8c4234743fed66f65f419cdd9a93c17731965b999c0f`  
		Last Modified: Fri, 06 Mar 2026 18:29:39 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.40` - linux; ppc64le

```console
$ docker pull traefik@sha256:524643fc3f1f0977b615ea3c6c9c367b5478265e3d19605e8a7782b529922626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45370950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681848a9a9a3e16c298fe4ff7c70b4bc677a621269054722fa82cd9ccadd385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d43896e5f631a033e87ab26375711e45d0e326538c03c1010bcf03b97fbc84`  
		Last Modified: Fri, 06 Mar 2026 19:09:12 GMT  
		Size: 41.1 MB (41077719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce60087078e608ffa549619ccbcad1b44bccbae714950413d20790cc3d9c11`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:ed8e461f5ca9203dfe0b794a9e65f0e795c42232b0c291103504b6ea6880cb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe430fe38a505da689470d45d07f54b6bc7e637b95bcef8a638c51309dc051`

```dockerfile
```

-	Layers:
	-	`sha256:2d3a362fc13666ae3a06ba910fcaeebb5a84d3833456d5e25b2b320a7b5b1186`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fecbd68abf9ced241b2342b121bc932cb7dbc36700eb5d143d613e2b76f952e`  
		Last Modified: Fri, 06 Mar 2026 19:09:10 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.40` - linux; riscv64

```console
$ docker pull traefik@sha256:348f7e0caef62d9dbe61b3e4f5d62e5128ba7edf2eb859c9808299dbae80ae4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843ae02cf270ae9278c7020d3ac8ac26c0f937b137a612ab6befabebfcef3ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:31:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:31:47 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:31:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5962b35abc3140ecbcfb2aee5b25c5b9a014c0546af5c0e9b5ca20982dc4b925`  
		Last Modified: Fri, 06 Mar 2026 18:37:02 GMT  
		Size: 45.5 MB (45453781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a605b65697fc0945a57284bbcb4ed1e31688a34db30a2f091269618bcce22`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:837c228369c33ae29bb85bf61cffef864608df8b11c06d4d3deb8560463c1386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59036bc36da8658aa40e65fc062cbfb5d47a5074f253c48250e63b6ac777094`

```dockerfile
```

-	Layers:
	-	`sha256:d55bbe8e5bc852a3988cdd3a39b1bd836bf0c8d6bc265a52b832cd638da713c8`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f07113f49c7d10729199703722a0044eba3f64e36a5988dbaf692a913c77d6`  
		Last Modified: Fri, 06 Mar 2026 18:36:55 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.40` - linux; s390x

```console
$ docker pull traefik@sha256:5240e1c9af4e0519a66dcc39c9cdafd9297c9b2b1e1f95bd9deb73521311add3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb9cb218e6ad73490f563939461602f73e5ab27fa1de2e74e07f9e371bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:40 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:40 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e510416fb374b9eb56473a0b59fc495f259c1b13b73a0dae64218561dc67d4c`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 461.5 KB (461533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b71675e04cf1dbfe62b57c17f076065d7416205afb01825579805070d67f3`  
		Last Modified: Fri, 06 Mar 2026 18:53:32 GMT  
		Size: 45.3 MB (45297904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7f586003262c8f363cf8416a9c3d85fd93d55167909a1f03db108661647b39`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.40` - unknown; unknown

```console
$ docker pull traefik@sha256:4a98a73daef385e25b9345690a8a291ecdfc98afa2bd878ccb0923b8f189bde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b7b5d78f5c9f3ad43d17282d7cb39b57e17aed68fbf37fdd8f63b93524f0a`

```dockerfile
```

-	Layers:
	-	`sha256:5718bca8b1a1ce263975e789e77f41701ad049ab5bb525361afaa3bfb1138287`  
		Last Modified: Fri, 06 Mar 2026 18:53:31 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45ed7e55108e80ef7190a695f183e4d6d28308a95ff39dbf0d07f7a4195f56a`  
		Last Modified: Fri, 06 Mar 2026 18:53:30 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.40-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:1a07eed86165e5f067e0990df0c2de97655ca0bf85a54e9e91f4a572fa1899a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v2.11.40-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:8f608cd7b75b88bdc70542502341be1b0e95886ac913a6955b2acf15a6e48609
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174306426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af105e032609920c4c049755dd4bb1964cbdf7aaa5cf78a5fc45151e052ddbf2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:14 GMT
RUN cmd /S /C #(nop) COPY file:c1ea7b3996c7d746acbf57b2356d48f92e3c4736d65d31d9f55d96ada10ea0a8 in \ 
# Tue, 10 Mar 2026 22:36:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 10 Mar 2026 22:36:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:36:17 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861b20f23611951684dafbd1216c3e4c7d3025ea7e5ab657802e7d4483e8026`  
		Last Modified: Tue, 10 Mar 2026 22:36:28 GMT  
		Size: 47.7 MB (47652704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fad2d0ab5c0a2306ed4483f3d6300eab23d190c841aa4f13ad8af51358e2cf1`  
		Last Modified: Tue, 10 Mar 2026 22:36:21 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c5bf090548f38d35db74fdd0fbdb4064f83aebd5d19c45c9f85670ee0c6e7`  
		Last Modified: Tue, 10 Mar 2026 22:36:21 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64623fe254c5a68c27cffb2ba790c0a19e4cef1c347b5bd79febd3a4fe3cc8f`  
		Last Modified: Tue, 10 Mar 2026 22:36:20 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.40-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v2.11.40-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cf1aa201b1e92a0804cefb2dd1146c9b6bf8874a50aea8826be59d1d70a7ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:631e57bb276e394f1a18e36fc6239a238983ae67d0ef7d7f53ff0527d046789f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175596988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656a8918206090e79d3ecf6d778148c9ef2bb78bba3a2ddae05364b482bf4964`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:15:29 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Fri, 06 Mar 2026 19:15:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:15:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 06 Mar 2026 19:15:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266390bdcfcede701df72bd86a9a23055f023e59f3af6e3585a9ad7ba907094`  
		Last Modified: Fri, 06 Mar 2026 19:16:07 GMT  
		Size: 48.9 MB (48948000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6049c739c1e18155b7f17730ed591eef60f7546a41c09ef0ec242a898c2f355`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039ad363fb2c69b77a0d0267fa158cb203dfae1af7e00a183a3216a586c1a336`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6cb6e1a807fdced0867a41d4b945274a21084d47cb01e32e4ceb122a92af2`  
		Last Modified: Fri, 06 Mar 2026 19:15:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

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

### `traefik:v3.6` - unknown; unknown

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

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:4f6e169b54bf46ea7867bdf3ab4e2e3a294e75422075c3798714290eea0d14e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:777f41e990d97011e2fb211423f79d7bb6b176fd7d4506fec4f47118aa1646ec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175601583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efc513bfa1405b5151548ad3dc3a1b71780e6339a4f88a9b0df6979d39eec31`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:54 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Tue, 10 Mar 2026 22:35:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 10 Mar 2026 22:35:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:35:57 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee74e145dfbd616221e4cdff1fecb374c867556624646a1c5819563992776fe`  
		Last Modified: Tue, 10 Mar 2026 22:36:08 GMT  
		Size: 48.9 MB (48947947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0fe73c33568211d0c99bb17acc720e94b801bf7b096f9c4f2f92abe8f19f6c`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d894bc98d44fd1af354269d0d5261179040605cdc9d27a4311742b4997819e19`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cd9b64c761d38f97f96e33d2b430ea8bd5ec73bd6ebb0d7554114edf074cf1`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.10`

```console
$ docker pull traefik@sha256:c549d482c55d7a797398562064f35428cc53e748d84d7190997930e7b31bcc32
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

### `traefik:v3.6.10` - linux; amd64

```console
$ docker pull traefik@sha256:e1ca9744b6f23332f00a41b20fdd9903501e5428f17138a3a9c3e98e2d272ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71678227393a5f65b692d193e0e41ef6f505e9e4ed943b030ed1826eb6881983`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:26:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:26:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:26:49 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:26:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7b8b41235a396c0a0bf3207fab7bd84d3fddabab260272c45ebd69a4a467f`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 460.7 KB (460728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91e1f2c6ad6fa6567f8537e4d97f9cec9c40e920a0b857b2021cf59c51c8eb`  
		Last Modified: Fri, 06 Mar 2026 18:27:14 GMT  
		Size: 48.2 MB (48180620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01185b3b027955913cd0e5cb976ed604b201d7fe681fb1c57740109e202621`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:b76461ddd95ad4026fae6f196f29ee69c89a665a882f0c265fdf11e80fa34e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e290a9071cc90c2dcff08164c3164f8ac057a03dce023975c2341c6b4ef461c`

```dockerfile
```

-	Layers:
	-	`sha256:bdb86b4150bd982cf4ec26d89d23a5f1fc6c511e24b2e3c5fdb0e13edaa9638c`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f9bae9e756a7e3448e21557af22d34d11d956809af448c06647552acba8da5`  
		Last Modified: Fri, 06 Mar 2026 18:27:13 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3964180e58e1e59dd88518cfc1371c99bae99b8d6cea8df9f6fcc3c847f4de51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47769510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2a56cb704fe1b0e53431c7ea5a2c75af5c8e58ea5284b7a4447cd41b54f05c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:57:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:57:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:57:19 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:57:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64460066e8123b47c8c3fd9e29712ab665718546a65e1696ba4e82c9dc8d673e`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 461.2 KB (461245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e774697634ce674649d1aab15bc6f56ee7ba7b2a015084969dc44b4c51ff`  
		Last Modified: Fri, 06 Mar 2026 18:57:29 GMT  
		Size: 43.7 MB (43738076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c0efef6248058dde1253280f33edfaa1d6f59a84e95b584a5fa43bea56e891`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:341fd64b88a1a8e067ae2e143fcf0e1fa698cfc36fd8bc0448a33d85a8b411ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3feb8273b4cc81d51599f82f457d1fb44d7033b134cac486b40fbcaf43b6d`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a23a427d1cd2343c4859597e8c023cce7b6038b1407fe8484e11981a73372`  
		Last Modified: Fri, 06 Mar 2026 18:57:27 GMT  
		Size: 12.7 KB (12686 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1a87097051e6b8e0d8a3d374c60f5239d6329f041a1bd9cdba0344c07644a6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47707145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f685fa390b83ca52671c4535eaec05752701fc2e61dbfa6a9e6089fc6f6ff8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:29:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:29:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:29:09 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:29:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdc53e7ff1625fd062c7262b1ec2d2a766a11de76786edcda242846d13b857`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 462.8 KB (462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d1bcd6fd6d63e2df15cfdc667dd299d272c24d38063a1725f26323fb83c5b5`  
		Last Modified: Fri, 06 Mar 2026 18:29:35 GMT  
		Size: 43.0 MB (43046934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700a70754e37e42f5e1daf4eedcba171358bf65895620359754938ef856714`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:9714866a6e18796a3f3917f5b0f38b2a8ee6d419af02cb5f1e6154f99a61ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93834501511d4be1a3fba3973d176a1ec56bf0810c61bfa9cdbab3d5570e5d95`

```dockerfile
```

-	Layers:
	-	`sha256:2728f1e527fe9bc240051bb17052e558d02e43db13ef5c736ec1cf581af3d7a3`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe4d7d7b3fb2c30421fd9641d3629d6c5ee3eab6c0f1505cfcfba8be7bd3912`  
		Last Modified: Fri, 06 Mar 2026 18:29:34 GMT  
		Size: 12.9 KB (12943 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.10` - linux; ppc64le

```console
$ docker pull traefik@sha256:c8faaeab2bfde143430e0780f609efca2ba2746a28afdbdd7d7012a7a717f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45922457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1612fceed539d7b22f463fc3dadbf3f8d041b9743d99ccb4bd355b46ddb15ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 19:08:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 19:08:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 19:08:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 19:08:17 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 19:08:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd89d0879c6d84b005e6d360fee45e276634fe92726be2ba6034bc5f8a06618`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 463.2 KB (463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456cf893a359fdcf1162a447eb9f36b804244b9cd7fadddd9bbdeb501e8c8b`  
		Last Modified: Fri, 06 Mar 2026 19:09:13 GMT  
		Size: 41.6 MB (41629225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0aa83487c187e7c78ed462e1d7fd4e1e028ba93a78993e1fbd24cb1388fda3`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:ab44f565779200852cc1d3c97407848fabe397536e7de04a21852499662e7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510232bc14437ba4eed52d3c74a02469bec1ad0cf9382125e7f20fb6f47019d9`

```dockerfile
```

-	Layers:
	-	`sha256:bde599f92f30345b208fbef7e2a6a5c08af7406ab086a3a6ccdd7ac81c3485c9`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32700f1f83e29f85d71c3fa1413594a0c3cbe2cd71d2e248eaff96a089c96ba8`  
		Last Modified: Fri, 06 Mar 2026 19:09:11 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.10` - linux; riscv64

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

### `traefik:v3.6.10` - unknown; unknown

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

### `traefik:v3.6.10` - linux; s390x

```console
$ docker pull traefik@sha256:7a5766fd17dab47c9855ea20d9038756cf45ccb1f2aeaa5b62c53bdfd3d214e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f01868c793588eb4a28d9123e64956835555a07fd4ed1a41fbca44afd1c1bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:52:34 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:52:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:52:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:52:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a13623c40de305887d930892529ab178a21163bdcda031038876ddbbe1009`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 461.5 KB (461540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6adc3027d2d56db0bab1dc20ea86ad7ce1f350bde694e38e9de48cad9e1e932`  
		Last Modified: Fri, 06 Mar 2026 18:53:27 GMT  
		Size: 46.4 MB (46370903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc4d57fa8f1030a681bdc5011da1c694f6791fe94dc43c9d46d327f199bb863`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.10` - unknown; unknown

```console
$ docker pull traefik@sha256:4296d8271ab57cc184afaa4f3cee26e7413b8788ae5c8991f81ee0f96d03a065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56da2f66bbf744d7e6ab9a98b5699b68d0fa8c8e5c5a2b8f069ecd4a34f886e6`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed90015653b883e5c728003abb620ea159ca18d52a3f1069c826a09064ec73`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2526cdd78e8c0816905c6c70aeb796ac16b99c1f1048e775a0e03b096fd37ac`  
		Last Modified: Fri, 06 Mar 2026 18:53:26 GMT  
		Size: 12.8 KB (12776 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.10-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:4f6e169b54bf46ea7867bdf3ab4e2e3a294e75422075c3798714290eea0d14e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v3.6.10-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:777f41e990d97011e2fb211423f79d7bb6b176fd7d4506fec4f47118aa1646ec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175601583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efc513bfa1405b5151548ad3dc3a1b71780e6339a4f88a9b0df6979d39eec31`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:54 GMT
RUN cmd /S /C #(nop) COPY file:6eb951e4a48f5f0f3419531de6d9e96edf3f6bcf38fad5fd1d21246477dc4132 in \ 
# Tue, 10 Mar 2026 22:35:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 10 Mar 2026 22:35:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:35:57 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee74e145dfbd616221e4cdff1fecb374c867556624646a1c5819563992776fe`  
		Last Modified: Tue, 10 Mar 2026 22:36:08 GMT  
		Size: 48.9 MB (48947947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0fe73c33568211d0c99bb17acc720e94b801bf7b096f9c4f2f92abe8f19f6c`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d894bc98d44fd1af354269d0d5261179040605cdc9d27a4311742b4997819e19`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cd9b64c761d38f97f96e33d2b430ea8bd5ec73bd6ebb0d7554114edf074cf1`  
		Last Modified: Tue, 10 Mar 2026 22:36:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.10-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:v3.6.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:febcbd013d13867815f38f0544c0dcb51f5e3e2313ad6364d21a136cc657f3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:94dd22624d12e8a955b9d20afb73a00720a9a94515c13bfe311a45f559e2f3d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031880809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12ca777d5ff3d6067db721ed0c76aa586bf3de39bf6228c5adae013d9b60b07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:04:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:04:46 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:04:47 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:04:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76826e8396384b1bdb2b83b989aee2883dd62de287f1e238dd3a711d795a6a`  
		Last Modified: Tue, 10 Mar 2026 22:05:20 GMT  
		Size: 49.6 MB (49594220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc8ce314d9187a52079c88b370fe8d18f50a93196a0a89ce58e601334cc6606`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc11bc12b276b5c8f9968699f940b0f3568e1b18169516c2d317fe3e4099ab49`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c58a5adc07cf31f9b97cf2b43afc8670ca7f8ecea49bfa464043869bc5063`  
		Last Modified: Tue, 10 Mar 2026 22:04:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
