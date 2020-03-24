<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.23`](#traefik1723)
-	[`traefik:1.7.23-alpine`](#traefik1723-alpine)
-	[`traefik:1.7.23-windowsservercore-1809`](#traefik1723-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.1`](#traefik21)
-	[`traefik:2.1.9`](#traefik219)
-	[`traefik:2.1.9-windowsservercore-1809`](#traefik219-windowsservercore-1809)
-	[`traefik:2.1-windowsservercore-1809`](#traefik21-windowsservercore-1809)
-	[`traefik:2.2`](#traefik22)
-	[`traefik:2.2.0-rc4`](#traefik220-rc4)
-	[`traefik:2.2.0-rc4-windowsservercore-1809`](#traefik220-rc4-windowsservercore-1809)
-	[`traefik:2.2-windowsservercore-1809`](#traefik22-windowsservercore-1809)
-	[`traefik:cantal`](#traefikcantal)
-	[`traefik:cantal-windowsservercore-1809`](#traefikcantal-windowsservercore-1809)
-	[`traefik:chevrotin`](#traefikchevrotin)
-	[`traefik:chevrotin-windowsservercore-1809`](#traefikchevrotin-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.23`](#traefikv1723)
-	[`traefik:v1.7.23-alpine`](#traefikv1723-alpine)
-	[`traefik:v1.7.23-windowsservercore-1809`](#traefikv1723-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.1`](#traefikv21)
-	[`traefik:v2.1.9`](#traefikv219)
-	[`traefik:v2.1.9-windowsservercore-1809`](#traefikv219-windowsservercore-1809)
-	[`traefik:v2.1-windowsservercore-1809`](#traefikv21-windowsservercore-1809)
-	[`traefik:v2.2`](#traefikv22)
-	[`traefik:v2.2.0-rc4`](#traefikv220-rc4)
-	[`traefik:v2.2.0-rc4-windowsservercore-1809`](#traefikv220-rc4-windowsservercore-1809)
-	[`traefik:v2.2-windowsservercore-1809`](#traefikv22-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:832102bb57916159a57b5acaf1eceb5d480367aa506f22a3754f4953c780a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7c8f0d086f900f3a09806488797ee3647bda9865f897754615fd1ca35b7c49ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20229998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fe6f51fbf4d0331840200411166b0da455d49459c51b788e55b7e52a10bd1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 20 Feb 2020 23:23:27 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Thu, 20 Feb 2020 23:23:31 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:53:03 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Mon, 23 Mar 2020 20:53:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:53:05 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:53:05 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:23c1841b8c7860045db6b4a1e02a96e6232417f97062ae42483b8d4658a40d33`  
		Last Modified: Thu, 20 Feb 2020 23:25:15 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0787cb8098772b3249eecfe5cb7694c680eceff4feebcab8358baf7e26557`  
		Last Modified: Thu, 20 Feb 2020 23:25:16 GMT  
		Size: 327.4 KB (327383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b0e6504ad827f3c34e14261d76e63e89b9988ef4031958e598db64c37372f`  
		Last Modified: Mon, 23 Mar 2020 20:54:05 GMT  
		Size: 19.8 MB (19770934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:afca314e5ba44ec1a158ffd830f5b16319d26c7dcb102d3d42f5c41cfdd3ad06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1755811b0b875559f7551d42e614cc661c5c9d1ba8ab5fc9503dee93f2305a00`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 01:08:43 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 01:08:48 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:41:40 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Mon, 23 Mar 2020 20:41:41 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:42 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:41:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:41:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e3d3c9facd6ab3f42d5ef511674d7d138ad0107cf47a738ec1ec1c836be5178e`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 131.7 KB (131684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52950036377454e4b5c9b92233904cd5d12087bbce611bddcda397a500ea6bb`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 327.4 KB (327408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea729d3f9ac73412fec470a093c2acc65f5de44902296fb4ea5c620b4942e43`  
		Last Modified: Mon, 23 Mar 2020 20:42:41 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23`

```console
$ docker pull traefik@sha256:832102bb57916159a57b5acaf1eceb5d480367aa506f22a3754f4953c780a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.23` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7c8f0d086f900f3a09806488797ee3647bda9865f897754615fd1ca35b7c49ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20229998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fe6f51fbf4d0331840200411166b0da455d49459c51b788e55b7e52a10bd1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 20 Feb 2020 23:23:27 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Thu, 20 Feb 2020 23:23:31 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:53:03 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Mon, 23 Mar 2020 20:53:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:53:05 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:53:05 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:23c1841b8c7860045db6b4a1e02a96e6232417f97062ae42483b8d4658a40d33`  
		Last Modified: Thu, 20 Feb 2020 23:25:15 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0787cb8098772b3249eecfe5cb7694c680eceff4feebcab8358baf7e26557`  
		Last Modified: Thu, 20 Feb 2020 23:25:16 GMT  
		Size: 327.4 KB (327383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b0e6504ad827f3c34e14261d76e63e89b9988ef4031958e598db64c37372f`  
		Last Modified: Mon, 23 Mar 2020 20:54:05 GMT  
		Size: 19.8 MB (19770934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:afca314e5ba44ec1a158ffd830f5b16319d26c7dcb102d3d42f5c41cfdd3ad06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1755811b0b875559f7551d42e614cc661c5c9d1ba8ab5fc9503dee93f2305a00`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 01:08:43 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 01:08:48 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:41:40 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Mon, 23 Mar 2020 20:41:41 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:42 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:41:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:41:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e3d3c9facd6ab3f42d5ef511674d7d138ad0107cf47a738ec1ec1c836be5178e`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 131.7 KB (131684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52950036377454e4b5c9b92233904cd5d12087bbce611bddcda397a500ea6bb`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 327.4 KB (327408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea729d3f9ac73412fec470a093c2acc65f5de44902296fb4ea5c620b4942e43`  
		Last Modified: Mon, 23 Mar 2020 20:42:41 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23-alpine`

```console
$ docker pull traefik@sha256:32fdf7411f1466b11fa35fd2e43cccf49c23a6ce318b26165a21de85c7af3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.23-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84515ca43b5bb61c7a8bf5adeb39f83b5a9a50961f01dfa08fe183e68d3f2d53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f6b250eec70fc5d3bc0444fa227ef634055cb2c0033273482ce8644851f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:50:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:50:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:50:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:50:05 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:50:05 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a16d004c21c131b30571446272aefe69d87cc823e735fa5db708d08bcbd54cde`  
		Last Modified: Mon, 23 Mar 2020 20:53:49 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841588d2403981d6dba983f8cb88597ae135f98614df2d7755b64bad5608cb3c`  
		Last Modified: Mon, 23 Mar 2020 20:53:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:00e3a6ae1c753ff1f05125411e2c20515b22a03dee4795f4ebb3789476a263c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3bd4e0e517546cb0631ad9639ba6a802730d9549c2e84a2d587e9cc512927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:22 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:23 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fdf5ce55e7b5682e2579c7501e15582fd9fca2521cdc48e0dbc993bf5c5ec1e3`  
		Last Modified: Mon, 23 Mar 2020 20:42:25 GMT  
		Size: 19.5 MB (19491949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022a55108a218afdc8622c901a8e5a4911cbec5d5b272d9f6f88b24fd2a5298`  
		Last Modified: Mon, 23 Mar 2020 20:42:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:1.7.23-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:32fdf7411f1466b11fa35fd2e43cccf49c23a6ce318b26165a21de85c7af3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84515ca43b5bb61c7a8bf5adeb39f83b5a9a50961f01dfa08fe183e68d3f2d53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f6b250eec70fc5d3bc0444fa227ef634055cb2c0033273482ce8644851f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:50:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:50:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:50:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:50:05 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:50:05 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a16d004c21c131b30571446272aefe69d87cc823e735fa5db708d08bcbd54cde`  
		Last Modified: Mon, 23 Mar 2020 20:53:49 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841588d2403981d6dba983f8cb88597ae135f98614df2d7755b64bad5608cb3c`  
		Last Modified: Mon, 23 Mar 2020 20:53:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:00e3a6ae1c753ff1f05125411e2c20515b22a03dee4795f4ebb3789476a263c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3bd4e0e517546cb0631ad9639ba6a802730d9549c2e84a2d587e9cc512927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:22 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:23 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fdf5ce55e7b5682e2579c7501e15582fd9fca2521cdc48e0dbc993bf5c5ec1e3`  
		Last Modified: Mon, 23 Mar 2020 20:42:25 GMT  
		Size: 19.5 MB (19491949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022a55108a218afdc8622c901a8e5a4911cbec5d5b272d9f6f88b24fd2a5298`  
		Last Modified: Mon, 23 Mar 2020 20:42:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.9`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1.9` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.1.9-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2`

```console
$ docker pull traefik@sha256:82e6b2564636a00e857614f77dbc3bfc7ce5009f9e5a72c14a073445e61c1520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3f9230e23558384ec74667d3bb267a300a0620a5f6e405cada6dd5041c6dbaaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23304555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133c917280780e2eb70f42f1223f6652a4c727c1b412a3cc0294e83e252503a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 19 Mar 2020 23:23:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 19 Mar 2020 23:23:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 19 Mar 2020 23:23:30 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2020 23:23:32 GMT
CMD ["traefik"]
# Thu, 19 Mar 2020 23:23:33 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:10a7ce7075e3cb97febbff60365fb86b17a86c0294b17c66364899585f12e1c4`  
		Last Modified: Thu, 19 Mar 2020 23:24:36 GMT  
		Size: 20.0 MB (19988611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ec71b4885f6ba4c9d6f9c1ca43724c7dbc4609ba9d6f566fbfa8f604ad9c0`  
		Last Modified: Thu, 19 Mar 2020 23:24:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b8e90b0dfa530d3ccfe3571f7b4fa950820de68c5856468a2e1096c11289683b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21ca0460e4eb9c7f51c7bacdda2c7ab8eac9146c62e43216e7196d8d35e56f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 20 Mar 2020 01:07:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 20 Mar 2020 01:07:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 20 Mar 2020 01:07:53 GMT
EXPOSE 80
# Fri, 20 Mar 2020 01:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2020 01:08:05 GMT
CMD ["traefik"]
# Fri, 20 Mar 2020 01:08:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:45222051a4be92d7d44b388d03292f59f1af91178dedc7bf90a9a597cc018d1d`  
		Last Modified: Fri, 20 Mar 2020 01:09:54 GMT  
		Size: 19.6 MB (19632522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2aaf6eb4c73fcc17336c4f6603672d042551a0a0763019d9c93882805906ab`  
		Last Modified: Fri, 20 Mar 2020 01:09:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0-rc4`

```console
$ docker pull traefik@sha256:82e6b2564636a00e857614f77dbc3bfc7ce5009f9e5a72c14a073445e61c1520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2.0-rc4` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0-rc4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3f9230e23558384ec74667d3bb267a300a0620a5f6e405cada6dd5041c6dbaaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23304555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133c917280780e2eb70f42f1223f6652a4c727c1b412a3cc0294e83e252503a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 19 Mar 2020 23:23:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 19 Mar 2020 23:23:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 19 Mar 2020 23:23:30 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2020 23:23:32 GMT
CMD ["traefik"]
# Thu, 19 Mar 2020 23:23:33 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:10a7ce7075e3cb97febbff60365fb86b17a86c0294b17c66364899585f12e1c4`  
		Last Modified: Thu, 19 Mar 2020 23:24:36 GMT  
		Size: 20.0 MB (19988611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ec71b4885f6ba4c9d6f9c1ca43724c7dbc4609ba9d6f566fbfa8f604ad9c0`  
		Last Modified: Thu, 19 Mar 2020 23:24:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0-rc4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b8e90b0dfa530d3ccfe3571f7b4fa950820de68c5856468a2e1096c11289683b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21ca0460e4eb9c7f51c7bacdda2c7ab8eac9146c62e43216e7196d8d35e56f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 20 Mar 2020 01:07:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 20 Mar 2020 01:07:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 20 Mar 2020 01:07:53 GMT
EXPOSE 80
# Fri, 20 Mar 2020 01:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2020 01:08:05 GMT
CMD ["traefik"]
# Fri, 20 Mar 2020 01:08:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:45222051a4be92d7d44b388d03292f59f1af91178dedc7bf90a9a597cc018d1d`  
		Last Modified: Fri, 20 Mar 2020 01:09:54 GMT  
		Size: 19.6 MB (19632522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2aaf6eb4c73fcc17336c4f6603672d042551a0a0763019d9c93882805906ab`  
		Last Modified: Fri, 20 Mar 2020 01:09:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0-rc4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.2.0-rc4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:cantal` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:cantal-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:82e6b2564636a00e857614f77dbc3bfc7ce5009f9e5a72c14a073445e61c1520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3f9230e23558384ec74667d3bb267a300a0620a5f6e405cada6dd5041c6dbaaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23304555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133c917280780e2eb70f42f1223f6652a4c727c1b412a3cc0294e83e252503a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 19 Mar 2020 23:23:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 19 Mar 2020 23:23:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 19 Mar 2020 23:23:30 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2020 23:23:32 GMT
CMD ["traefik"]
# Thu, 19 Mar 2020 23:23:33 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:10a7ce7075e3cb97febbff60365fb86b17a86c0294b17c66364899585f12e1c4`  
		Last Modified: Thu, 19 Mar 2020 23:24:36 GMT  
		Size: 20.0 MB (19988611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ec71b4885f6ba4c9d6f9c1ca43724c7dbc4609ba9d6f566fbfa8f604ad9c0`  
		Last Modified: Thu, 19 Mar 2020 23:24:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b8e90b0dfa530d3ccfe3571f7b4fa950820de68c5856468a2e1096c11289683b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21ca0460e4eb9c7f51c7bacdda2c7ab8eac9146c62e43216e7196d8d35e56f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 20 Mar 2020 01:07:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 20 Mar 2020 01:07:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 20 Mar 2020 01:07:53 GMT
EXPOSE 80
# Fri, 20 Mar 2020 01:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2020 01:08:05 GMT
CMD ["traefik"]
# Fri, 20 Mar 2020 01:08:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:45222051a4be92d7d44b388d03292f59f1af91178dedc7bf90a9a597cc018d1d`  
		Last Modified: Fri, 20 Mar 2020 01:09:54 GMT  
		Size: 19.6 MB (19632522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2aaf6eb4c73fcc17336c4f6603672d042551a0a0763019d9c93882805906ab`  
		Last Modified: Fri, 20 Mar 2020 01:09:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:832102bb57916159a57b5acaf1eceb5d480367aa506f22a3754f4953c780a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7c8f0d086f900f3a09806488797ee3647bda9865f897754615fd1ca35b7c49ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20229998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fe6f51fbf4d0331840200411166b0da455d49459c51b788e55b7e52a10bd1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 20 Feb 2020 23:23:27 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Thu, 20 Feb 2020 23:23:31 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:53:03 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Mon, 23 Mar 2020 20:53:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:53:05 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:53:05 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:23c1841b8c7860045db6b4a1e02a96e6232417f97062ae42483b8d4658a40d33`  
		Last Modified: Thu, 20 Feb 2020 23:25:15 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0787cb8098772b3249eecfe5cb7694c680eceff4feebcab8358baf7e26557`  
		Last Modified: Thu, 20 Feb 2020 23:25:16 GMT  
		Size: 327.4 KB (327383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b0e6504ad827f3c34e14261d76e63e89b9988ef4031958e598db64c37372f`  
		Last Modified: Mon, 23 Mar 2020 20:54:05 GMT  
		Size: 19.8 MB (19770934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:afca314e5ba44ec1a158ffd830f5b16319d26c7dcb102d3d42f5c41cfdd3ad06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1755811b0b875559f7551d42e614cc661c5c9d1ba8ab5fc9503dee93f2305a00`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 01:08:43 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 01:08:48 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:41:40 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Mon, 23 Mar 2020 20:41:41 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:42 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:41:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:41:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e3d3c9facd6ab3f42d5ef511674d7d138ad0107cf47a738ec1ec1c836be5178e`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 131.7 KB (131684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52950036377454e4b5c9b92233904cd5d12087bbce611bddcda397a500ea6bb`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 327.4 KB (327408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea729d3f9ac73412fec470a093c2acc65f5de44902296fb4ea5c620b4942e43`  
		Last Modified: Mon, 23 Mar 2020 20:42:41 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:32fdf7411f1466b11fa35fd2e43cccf49c23a6ce318b26165a21de85c7af3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84515ca43b5bb61c7a8bf5adeb39f83b5a9a50961f01dfa08fe183e68d3f2d53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f6b250eec70fc5d3bc0444fa227ef634055cb2c0033273482ce8644851f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:50:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:50:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:50:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:50:05 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:50:05 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a16d004c21c131b30571446272aefe69d87cc823e735fa5db708d08bcbd54cde`  
		Last Modified: Mon, 23 Mar 2020 20:53:49 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841588d2403981d6dba983f8cb88597ae135f98614df2d7755b64bad5608cb3c`  
		Last Modified: Mon, 23 Mar 2020 20:53:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:00e3a6ae1c753ff1f05125411e2c20515b22a03dee4795f4ebb3789476a263c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3bd4e0e517546cb0631ad9639ba6a802730d9549c2e84a2d587e9cc512927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:22 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:23 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fdf5ce55e7b5682e2579c7501e15582fd9fca2521cdc48e0dbc993bf5c5ec1e3`  
		Last Modified: Mon, 23 Mar 2020 20:42:25 GMT  
		Size: 19.5 MB (19491949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022a55108a218afdc8622c901a8e5a4911cbec5d5b272d9f6f88b24fd2a5298`  
		Last Modified: Mon, 23 Mar 2020 20:42:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:832102bb57916159a57b5acaf1eceb5d480367aa506f22a3754f4953c780a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7c8f0d086f900f3a09806488797ee3647bda9865f897754615fd1ca35b7c49ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20229998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fe6f51fbf4d0331840200411166b0da455d49459c51b788e55b7e52a10bd1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 20 Feb 2020 23:23:27 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Thu, 20 Feb 2020 23:23:31 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:53:03 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Mon, 23 Mar 2020 20:53:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:53:05 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:53:05 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:23c1841b8c7860045db6b4a1e02a96e6232417f97062ae42483b8d4658a40d33`  
		Last Modified: Thu, 20 Feb 2020 23:25:15 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0787cb8098772b3249eecfe5cb7694c680eceff4feebcab8358baf7e26557`  
		Last Modified: Thu, 20 Feb 2020 23:25:16 GMT  
		Size: 327.4 KB (327383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b0e6504ad827f3c34e14261d76e63e89b9988ef4031958e598db64c37372f`  
		Last Modified: Mon, 23 Mar 2020 20:54:05 GMT  
		Size: 19.8 MB (19770934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:afca314e5ba44ec1a158ffd830f5b16319d26c7dcb102d3d42f5c41cfdd3ad06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1755811b0b875559f7551d42e614cc661c5c9d1ba8ab5fc9503dee93f2305a00`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 01:08:43 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 01:08:48 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:41:40 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Mon, 23 Mar 2020 20:41:41 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:42 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:41:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:41:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e3d3c9facd6ab3f42d5ef511674d7d138ad0107cf47a738ec1ec1c836be5178e`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 131.7 KB (131684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52950036377454e4b5c9b92233904cd5d12087bbce611bddcda397a500ea6bb`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 327.4 KB (327408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea729d3f9ac73412fec470a093c2acc65f5de44902296fb4ea5c620b4942e43`  
		Last Modified: Mon, 23 Mar 2020 20:42:41 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23`

```console
$ docker pull traefik@sha256:832102bb57916159a57b5acaf1eceb5d480367aa506f22a3754f4953c780a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.23` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7c8f0d086f900f3a09806488797ee3647bda9865f897754615fd1ca35b7c49ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20229998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667fe6f51fbf4d0331840200411166b0da455d49459c51b788e55b7e52a10bd1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 20 Feb 2020 23:23:27 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Thu, 20 Feb 2020 23:23:31 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:53:03 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Mon, 23 Mar 2020 20:53:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:53:05 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:53:05 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:23c1841b8c7860045db6b4a1e02a96e6232417f97062ae42483b8d4658a40d33`  
		Last Modified: Thu, 20 Feb 2020 23:25:15 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb0787cb8098772b3249eecfe5cb7694c680eceff4feebcab8358baf7e26557`  
		Last Modified: Thu, 20 Feb 2020 23:25:16 GMT  
		Size: 327.4 KB (327383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b0e6504ad827f3c34e14261d76e63e89b9988ef4031958e598db64c37372f`  
		Last Modified: Mon, 23 Mar 2020 20:54:05 GMT  
		Size: 19.8 MB (19770934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:afca314e5ba44ec1a158ffd830f5b16319d26c7dcb102d3d42f5c41cfdd3ad06
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1755811b0b875559f7551d42e614cc661c5c9d1ba8ab5fc9503dee93f2305a00`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 01:08:43 GMT
COPY file:f457e8adb6c53dc9a59d4eb315e663a1b1eda09623526a54957ad04390140125 in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 01:08:48 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:41:40 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Mon, 23 Mar 2020 20:41:41 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:42 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:41:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:41:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e3d3c9facd6ab3f42d5ef511674d7d138ad0107cf47a738ec1ec1c836be5178e`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 131.7 KB (131684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52950036377454e4b5c9b92233904cd5d12087bbce611bddcda397a500ea6bb`  
		Last Modified: Fri, 21 Feb 2020 01:09:42 GMT  
		Size: 327.4 KB (327408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea729d3f9ac73412fec470a093c2acc65f5de44902296fb4ea5c620b4942e43`  
		Last Modified: Mon, 23 Mar 2020 20:42:41 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23-alpine`

```console
$ docker pull traefik@sha256:32fdf7411f1466b11fa35fd2e43cccf49c23a6ce318b26165a21de85c7af3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.23-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84515ca43b5bb61c7a8bf5adeb39f83b5a9a50961f01dfa08fe183e68d3f2d53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f6b250eec70fc5d3bc0444fa227ef634055cb2c0033273482ce8644851f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:50:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:50:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:50:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:50:05 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:50:05 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a16d004c21c131b30571446272aefe69d87cc823e735fa5db708d08bcbd54cde`  
		Last Modified: Mon, 23 Mar 2020 20:53:49 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841588d2403981d6dba983f8cb88597ae135f98614df2d7755b64bad5608cb3c`  
		Last Modified: Mon, 23 Mar 2020 20:53:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:00e3a6ae1c753ff1f05125411e2c20515b22a03dee4795f4ebb3789476a263c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3bd4e0e517546cb0631ad9639ba6a802730d9549c2e84a2d587e9cc512927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:22 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:23 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fdf5ce55e7b5682e2579c7501e15582fd9fca2521cdc48e0dbc993bf5c5ec1e3`  
		Last Modified: Mon, 23 Mar 2020 20:42:25 GMT  
		Size: 19.5 MB (19491949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022a55108a218afdc8622c901a8e5a4911cbec5d5b272d9f6f88b24fd2a5298`  
		Last Modified: Mon, 23 Mar 2020 20:42:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v1.7.23-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:32fdf7411f1466b11fa35fd2e43cccf49c23a6ce318b26165a21de85c7af3128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84515ca43b5bb61c7a8bf5adeb39f83b5a9a50961f01dfa08fe183e68d3f2d53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23086930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52f6b250eec70fc5d3bc0444fa227ef634055cb2c0033273482ce8644851f1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:50:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:50:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:50:04 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:50:05 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:50:05 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a16d004c21c131b30571446272aefe69d87cc823e735fa5db708d08bcbd54cde`  
		Last Modified: Mon, 23 Mar 2020 20:53:49 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841588d2403981d6dba983f8cb88597ae135f98614df2d7755b64bad5608cb3c`  
		Last Modified: Mon, 23 Mar 2020 20:53:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:00e3a6ae1c753ff1f05125411e2c20515b22a03dee4795f4ebb3789476a263c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f3bd4e0e517546cb0631ad9639ba6a802730d9549c2e84a2d587e9cc512927`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:22 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:23 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fdf5ce55e7b5682e2579c7501e15582fd9fca2521cdc48e0dbc993bf5c5ec1e3`  
		Last Modified: Mon, 23 Mar 2020 20:42:25 GMT  
		Size: 19.5 MB (19491949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022a55108a218afdc8622c901a8e5a4911cbec5d5b272d9f6f88b24fd2a5298`  
		Last Modified: Mon, 23 Mar 2020 20:42:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.9`

```console
$ docker pull traefik@sha256:2c17c789b4913f29d1f64199cc3d9110f77fc3f7d6bafb306520d9e377efff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1.9` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec4c327312864f8227558d7efecbd0c352e38d5b738986c1d846a404e3592985
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21361223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88f992c0346c53120310162fe5138c219a20ef0e7f736c8ddcd69e51c5d948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:49:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:49:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:49:51 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:49:52 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:49:52 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:01867f22aa594add1352f241375571781740d5029daa2ceea01c4ff247a164d7`  
		Last Modified: Mon, 23 Mar 2020 20:53:31 GMT  
		Size: 18.0 MB (18045280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b5a2adc9ac9650a1a57c3389fa9734b24aa8bb54193d2500d1bc8d944a496`  
		Last Modified: Mon, 23 Mar 2020 20:53:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6f68eb837e74b488fee49ed5633ba5c19044375b42de7748c12929f521844647
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e602d94b202966202cd98d652c9dde92ca061c15ea97ae9e32d62f0f22c6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 20:41:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 20:41:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 20:41:10 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 20:41:11 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 20:41:12 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f21b1acf15c5b57d3750c77a44dabe3294b73af2f262d9bcd77bc5e3b317c10e`  
		Last Modified: Mon, 23 Mar 2020 20:42:07 GMT  
		Size: 17.7 MB (17747474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501418cfeac4145222b3f8b5bafbcf73d77b276cf7d07e152988b6fb646dd104`  
		Last Modified: Mon, 23 Mar 2020 20:42:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.1.9-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2`

```console
$ docker pull traefik@sha256:82e6b2564636a00e857614f77dbc3bfc7ce5009f9e5a72c14a073445e61c1520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3f9230e23558384ec74667d3bb267a300a0620a5f6e405cada6dd5041c6dbaaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23304555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133c917280780e2eb70f42f1223f6652a4c727c1b412a3cc0294e83e252503a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 19 Mar 2020 23:23:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 19 Mar 2020 23:23:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 19 Mar 2020 23:23:30 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2020 23:23:32 GMT
CMD ["traefik"]
# Thu, 19 Mar 2020 23:23:33 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:10a7ce7075e3cb97febbff60365fb86b17a86c0294b17c66364899585f12e1c4`  
		Last Modified: Thu, 19 Mar 2020 23:24:36 GMT  
		Size: 20.0 MB (19988611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ec71b4885f6ba4c9d6f9c1ca43724c7dbc4609ba9d6f566fbfa8f604ad9c0`  
		Last Modified: Thu, 19 Mar 2020 23:24:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b8e90b0dfa530d3ccfe3571f7b4fa950820de68c5856468a2e1096c11289683b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21ca0460e4eb9c7f51c7bacdda2c7ab8eac9146c62e43216e7196d8d35e56f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 20 Mar 2020 01:07:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 20 Mar 2020 01:07:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 20 Mar 2020 01:07:53 GMT
EXPOSE 80
# Fri, 20 Mar 2020 01:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2020 01:08:05 GMT
CMD ["traefik"]
# Fri, 20 Mar 2020 01:08:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:45222051a4be92d7d44b388d03292f59f1af91178dedc7bf90a9a597cc018d1d`  
		Last Modified: Fri, 20 Mar 2020 01:09:54 GMT  
		Size: 19.6 MB (19632522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2aaf6eb4c73fcc17336c4f6603672d042551a0a0763019d9c93882805906ab`  
		Last Modified: Fri, 20 Mar 2020 01:09:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0-rc4`

```console
$ docker pull traefik@sha256:82e6b2564636a00e857614f77dbc3bfc7ce5009f9e5a72c14a073445e61c1520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2.0-rc4` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0-rc4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3f9230e23558384ec74667d3bb267a300a0620a5f6e405cada6dd5041c6dbaaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23304555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a133c917280780e2eb70f42f1223f6652a4c727c1b412a3cc0294e83e252503a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:49:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 19 Mar 2020 23:23:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 19 Mar 2020 23:23:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 19 Mar 2020 23:23:30 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2020 23:23:32 GMT
CMD ["traefik"]
# Thu, 19 Mar 2020 23:23:33 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:10a7ce7075e3cb97febbff60365fb86b17a86c0294b17c66364899585f12e1c4`  
		Last Modified: Thu, 19 Mar 2020 23:24:36 GMT  
		Size: 20.0 MB (19988611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ec71b4885f6ba4c9d6f9c1ca43724c7dbc4609ba9d6f566fbfa8f604ad9c0`  
		Last Modified: Thu, 19 Mar 2020 23:24:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0-rc4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b8e90b0dfa530d3ccfe3571f7b4fa950820de68c5856468a2e1096c11289683b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21ca0460e4eb9c7f51c7bacdda2c7ab8eac9146c62e43216e7196d8d35e56f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Thu, 06 Feb 2020 22:44:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 20 Mar 2020 01:07:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 20 Mar 2020 01:07:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 20 Mar 2020 01:07:53 GMT
EXPOSE 80
# Fri, 20 Mar 2020 01:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2020 01:08:05 GMT
CMD ["traefik"]
# Fri, 20 Mar 2020 01:08:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:45222051a4be92d7d44b388d03292f59f1af91178dedc7bf90a9a597cc018d1d`  
		Last Modified: Fri, 20 Mar 2020 01:09:54 GMT  
		Size: 19.6 MB (19632522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2aaf6eb4c73fcc17336c4f6603672d042551a0a0763019d9c93882805906ab`  
		Last Modified: Fri, 20 Mar 2020 01:09:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0-rc4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.2.0-rc4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
