## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:bdc976c74f549c7f0ba5976ba250f34a1fd90f6b370c5e43f94df538b719275b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:8fa8c4faa799bf8f632fe4af56768e3e1f302bf2d63fc1cd7c7752a36ee364a3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8378e05f99d815e7131d19af5863e997f0b35d694fe4e6298995a8342b4aca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2020 06:13:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Jan 2020 06:13:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Jan 2020 06:13:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Jan 2020 06:13:11 GMT
EXPOSE 80
# Fri, 24 Jan 2020 06:13:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:13:11 GMT
CMD ["traefik"]
# Fri, 24 Jan 2020 06:13:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520ea16e7f6377da620429123e1719b05706a467405f9f0e316903e8e1e3115`  
		Last Modified: Fri, 24 Jan 2020 06:13:50 GMT  
		Size: 694.5 KB (694516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5fe297ffea46a9bc6c4835ba3be1f448489b318393b4e21359be110bfbb8c6`  
		Last Modified: Fri, 24 Jan 2020 06:14:27 GMT  
		Size: 23.5 MB (23546270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b709b3720f84d639406bffe2c590c3ca2a41f646204f2dbb712a92bbd372b778`  
		Last Modified: Fri, 24 Jan 2020 06:14:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:738e9b119aaf9d93111c4d106999b761a2aec49107bfcdf56659cb8cb00e3b78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25354129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040affe79b0c33f1032773cecdc51b55c3ad16d32129fe19eac901be8b2beca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Feb 2020 23:19:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.21/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Feb 2020 23:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Feb 2020 23:19:43 GMT
EXPOSE 80
# Thu, 20 Feb 2020 23:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Feb 2020 23:19:45 GMT
CMD ["traefik"]
# Thu, 20 Feb 2020 23:19:46 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a045f3facd048d78ccec1317c0b8d3aa5e1b76f175b643f80c704ec2aa89f8`  
		Last Modified: Thu, 06 Feb 2020 22:51:40 GMT  
		Size: 698.0 KB (698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ef1f9c32d2768d6e21333dea037ba6488a6807bd873790b98d6cbeaa676f20`  
		Last Modified: Thu, 20 Feb 2020 23:25:05 GMT  
		Size: 22.0 MB (22038187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f3959c6f98920f7c6ed79674d03674c30925a6bbe11e2da8f02bcf50ad80da`  
		Last Modified: Thu, 20 Feb 2020 23:24:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bc9357d03ae91ec11cbfcef34dd85c5512e93dd993220f29e9bcb109ad4e87f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25177947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a43d99f6d8b4cb18362432e9aa459ab4828fc64e8f04f8ca504243af319ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Feb 2020 01:08:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.21/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Feb 2020 01:08:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Feb 2020 01:08:28 GMT
EXPOSE 80
# Fri, 21 Feb 2020 01:08:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Feb 2020 01:08:29 GMT
CMD ["traefik"]
# Fri, 21 Feb 2020 01:08:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5c788179332343fbcbc8b97673406752232ca36894176cc87ece20ee279754`  
		Last Modified: Thu, 06 Feb 2020 22:47:56 GMT  
		Size: 696.0 KB (696043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1520ccdb72fc9797850dc1b3891af53fac1a5ab24ff927bd75ff769495a11df`  
		Last Modified: Fri, 21 Feb 2020 01:09:31 GMT  
		Size: 21.8 MB (21758461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b783ed4bba2358b372561bbb9084fea69e6f888bd146459d201471a16c238afc`  
		Last Modified: Fri, 21 Feb 2020 01:09:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
