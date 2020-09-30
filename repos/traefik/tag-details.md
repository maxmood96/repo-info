<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.26`](#traefik1726)
-	[`traefik:1.7.26-alpine`](#traefik1726-alpine)
-	[`traefik:1.7.26-windowsservercore-1809`](#traefik1726-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.3`](#traefik23)
-	[`traefik:2.3.1`](#traefik231)
-	[`traefik:2.3.1-windowsservercore-1809`](#traefik231-windowsservercore-1809)
-	[`traefik:2.3-windowsservercore-1809`](#traefik23-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:picodon`](#traefikpicodon)
-	[`traefik:picodon-windowsservercore-1809`](#traefikpicodon-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.26`](#traefikv1726)
-	[`traefik:v1.7.26-alpine`](#traefikv1726-alpine)
-	[`traefik:v1.7.26-windowsservercore-1809`](#traefikv1726-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.3`](#traefikv23)
-	[`traefik:v2.3.1`](#traefikv231)
-	[`traefik:v2.3.1-windowsservercore-1809`](#traefikv231-windowsservercore-1809)
-	[`traefik:v2.3-windowsservercore-1809`](#traefikv23-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:17067dcaa6b2fca1cf7b4aff8aee13ca55cb43a13e47645598567f9bd09ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3517b63d7a9cd49b7237882fb7c260589b58163c4082d3a37de55a0d93311718
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21585385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab7ee8304c003a86093c588d645758bfed1ac563263e12516c798014a4fc10`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:20:43 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Wed, 29 Jul 2020 00:20:44 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:44 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:20:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:20:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8bcf82fc850436ad04fd66371e38f7611fe76a22b78f47f57ddb8908aa3d6001`  
		Last Modified: Wed, 29 Jul 2020 00:21:33 GMT  
		Size: 21.1 MB (21126327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:200bc13e0e03c532ea237fcc9f0c4f22416b91512a21c11cff0ecfa61a75d1f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20232026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47b44829bfc497b7e5f3a9777a71f42e165db80fee23dcdb4de56014db3334e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 28 Jul 2020 23:56:22 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Tue, 28 Jul 2020 23:56:25 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:56:26 GMT
VOLUME [/tmp]
# Tue, 28 Jul 2020 23:56:27 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Jul 2020 23:56:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ba63f15824a6daa3f73b57bd9fb04ea01b471f646b703dd08620f13e22d9c`  
		Last Modified: Tue, 28 Jul 2020 23:57:53 GMT  
		Size: 19.8 MB (19772940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d46ed499e4b8c1c9dffea750abe7ad35fba0c431165a394e10283810d33b8d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b691bd363853ce10cedfbe29ea1e8d1e88d7e8eb01da6a3e1baa469c745a1302`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:00:50 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Wed, 29 Jul 2020 00:00:51 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:00:51 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:00:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:00:53 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d477ed11470c756d1112d559be2ea65e2bbdcc367345ed45d17401a98474e`  
		Last Modified: Wed, 29 Jul 2020 00:02:17 GMT  
		Size: 19.5 MB (19492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.26`

```console
$ docker pull traefik@sha256:17067dcaa6b2fca1cf7b4aff8aee13ca55cb43a13e47645598567f9bd09ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.26` - linux; amd64

```console
$ docker pull traefik@sha256:3517b63d7a9cd49b7237882fb7c260589b58163c4082d3a37de55a0d93311718
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21585385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab7ee8304c003a86093c588d645758bfed1ac563263e12516c798014a4fc10`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:20:43 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Wed, 29 Jul 2020 00:20:44 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:44 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:20:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:20:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8bcf82fc850436ad04fd66371e38f7611fe76a22b78f47f57ddb8908aa3d6001`  
		Last Modified: Wed, 29 Jul 2020 00:21:33 GMT  
		Size: 21.1 MB (21126327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.26` - linux; arm variant v6

```console
$ docker pull traefik@sha256:200bc13e0e03c532ea237fcc9f0c4f22416b91512a21c11cff0ecfa61a75d1f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20232026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47b44829bfc497b7e5f3a9777a71f42e165db80fee23dcdb4de56014db3334e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 28 Jul 2020 23:56:22 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Tue, 28 Jul 2020 23:56:25 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:56:26 GMT
VOLUME [/tmp]
# Tue, 28 Jul 2020 23:56:27 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Jul 2020 23:56:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ba63f15824a6daa3f73b57bd9fb04ea01b471f646b703dd08620f13e22d9c`  
		Last Modified: Tue, 28 Jul 2020 23:57:53 GMT  
		Size: 19.8 MB (19772940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.26` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d46ed499e4b8c1c9dffea750abe7ad35fba0c431165a394e10283810d33b8d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b691bd363853ce10cedfbe29ea1e8d1e88d7e8eb01da6a3e1baa469c745a1302`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:00:50 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Wed, 29 Jul 2020 00:00:51 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:00:51 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:00:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:00:53 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d477ed11470c756d1112d559be2ea65e2bbdcc367345ed45d17401a98474e`  
		Last Modified: Wed, 29 Jul 2020 00:02:17 GMT  
		Size: 19.5 MB (19492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.26-alpine`

```console
$ docker pull traefik@sha256:0da45cd2c37ec826012e0f2d8a3a4ac0a7be4240a4942a6e40e3aae0f6fb205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.26-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3cbe9e62ef26a9ac17b25702754dfbf56dd346850170be90eabd370f24190ef1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24634355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f69007d987e4ed093711f4f306b52ce63b1c19f5ffacd49a1aea1f717e527`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jul 2020 00:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jul 2020 00:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jul 2020 00:20:25 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jul 2020 00:20:26 GMT
CMD ["traefik"]
# Wed, 29 Jul 2020 00:20:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb03716fa366c58de14b0fc81a50daf51f39175c928558e3e82017b5999f233`  
		Last Modified: Wed, 29 Jul 2020 00:21:23 GMT  
		Size: 21.1 MB (21126524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c61f1414a3fbacefede004c9c340def8b1c393630a1c2241a0c9196692c574`  
		Last Modified: Wed, 29 Jul 2020 00:21:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.26-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d77a05164ca7fbf64eb55feb97bd9e3d1dfaed181d23bc172d1602203b036b28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddfeb559adfb1011610755afdd099c865a8de51b045331d848b1a58077bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:51:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:51:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:51:48 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:51:52 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:51:55 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46db6761515f08f18c5396f51c8d5fd2ae1c385ff5c12113336ffb79684420`  
		Last Modified: Tue, 28 Jul 2020 23:57:37 GMT  
		Size: 19.8 MB (19772984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368cab0ca49479d26c28e4638f00e78884190c43adf25a35b647ffc70e1209f`  
		Last Modified: Tue, 28 Jul 2020 23:57:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.26-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7805105ced1b07c019cb3c420705bb105b1d8da381b76869db624e521af05592
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22913978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e0334e123554f38144482ac92954e0ed970de05727c2d7b6e371f0cda8f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:50:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:50:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:50:28 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:50:29 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:50:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9ba2c08e62ba40494711c8f4e4d32d3d297940e5c04ceaa0594de58ced1744`  
		Last Modified: Wed, 29 Jul 2020 00:02:01 GMT  
		Size: 19.5 MB (19493128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295e2c39b2f8f9a497a542502857a9b10a07977734f37c658f79d6e1a71c57b`  
		Last Modified: Wed, 29 Jul 2020 00:01:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.26-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7748a8d390b3a823799597c3f99116d22bf57ce78114fb97adb67b959ea91b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:1.7.26-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:6539da7d73380435d9f6f38e63c5ff973d88f80b38c09417b7d86723e44a7bbb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381526922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3b1b872cb048b6f3e1953bd97ddf91c9bff263377be6c1aec35af17bd5a347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:00:25 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 08 Sep 2020 20:00:29 GMT
EXPOSE 80
# Tue, 08 Sep 2020 20:00:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 08 Sep 2020 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161157bf7aee194faba8fb8c83b02c05417ca71b3b51ad565ef7220da3ae03c`  
		Last Modified: Tue, 08 Sep 2020 20:03:24 GMT  
		Size: 30.3 MB (30250121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e9f96df13dda9a1e8b837a36603457f53d342e67af86dad22e3bf0c2733d3`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5096b888e43211ea03b1d602bd3435d00ccd2a0204243f2d1e29e321da717f`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c72e13f4d30bccf8dac73850256f6b6bff614348bf9758c492305bd0eeccde`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:0da45cd2c37ec826012e0f2d8a3a4ac0a7be4240a4942a6e40e3aae0f6fb205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3cbe9e62ef26a9ac17b25702754dfbf56dd346850170be90eabd370f24190ef1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24634355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f69007d987e4ed093711f4f306b52ce63b1c19f5ffacd49a1aea1f717e527`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jul 2020 00:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jul 2020 00:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jul 2020 00:20:25 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jul 2020 00:20:26 GMT
CMD ["traefik"]
# Wed, 29 Jul 2020 00:20:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb03716fa366c58de14b0fc81a50daf51f39175c928558e3e82017b5999f233`  
		Last Modified: Wed, 29 Jul 2020 00:21:23 GMT  
		Size: 21.1 MB (21126524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c61f1414a3fbacefede004c9c340def8b1c393630a1c2241a0c9196692c574`  
		Last Modified: Wed, 29 Jul 2020 00:21:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d77a05164ca7fbf64eb55feb97bd9e3d1dfaed181d23bc172d1602203b036b28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddfeb559adfb1011610755afdd099c865a8de51b045331d848b1a58077bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:51:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:51:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:51:48 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:51:52 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:51:55 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46db6761515f08f18c5396f51c8d5fd2ae1c385ff5c12113336ffb79684420`  
		Last Modified: Tue, 28 Jul 2020 23:57:37 GMT  
		Size: 19.8 MB (19772984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368cab0ca49479d26c28e4638f00e78884190c43adf25a35b647ffc70e1209f`  
		Last Modified: Tue, 28 Jul 2020 23:57:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7805105ced1b07c019cb3c420705bb105b1d8da381b76869db624e521af05592
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22913978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e0334e123554f38144482ac92954e0ed970de05727c2d7b6e371f0cda8f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:50:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:50:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:50:28 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:50:29 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:50:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9ba2c08e62ba40494711c8f4e4d32d3d297940e5c04ceaa0594de58ced1744`  
		Last Modified: Wed, 29 Jul 2020 00:02:01 GMT  
		Size: 19.5 MB (19493128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295e2c39b2f8f9a497a542502857a9b10a07977734f37c658f79d6e1a71c57b`  
		Last Modified: Wed, 29 Jul 2020 00:01:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7748a8d390b3a823799597c3f99116d22bf57ce78114fb97adb67b959ea91b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:6539da7d73380435d9f6f38e63c5ff973d88f80b38c09417b7d86723e44a7bbb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381526922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3b1b872cb048b6f3e1953bd97ddf91c9bff263377be6c1aec35af17bd5a347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:00:25 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 08 Sep 2020 20:00:29 GMT
EXPOSE 80
# Tue, 08 Sep 2020 20:00:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 08 Sep 2020 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161157bf7aee194faba8fb8c83b02c05417ca71b3b51ad565ef7220da3ae03c`  
		Last Modified: Tue, 08 Sep 2020 20:03:24 GMT  
		Size: 30.3 MB (30250121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e9f96df13dda9a1e8b837a36603457f53d342e67af86dad22e3bf0c2733d3`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5096b888e43211ea03b1d602bd3435d00ccd2a0204243f2d1e29e321da717f`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c72e13f4d30bccf8dac73850256f6b6bff614348bf9758c492305bd0eeccde`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.3` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3.1`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.3.1` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:2.3.1-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:2.3-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:17067dcaa6b2fca1cf7b4aff8aee13ca55cb43a13e47645598567f9bd09ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:3517b63d7a9cd49b7237882fb7c260589b58163c4082d3a37de55a0d93311718
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21585385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab7ee8304c003a86093c588d645758bfed1ac563263e12516c798014a4fc10`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:20:43 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Wed, 29 Jul 2020 00:20:44 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:44 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:20:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:20:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8bcf82fc850436ad04fd66371e38f7611fe76a22b78f47f57ddb8908aa3d6001`  
		Last Modified: Wed, 29 Jul 2020 00:21:33 GMT  
		Size: 21.1 MB (21126327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:200bc13e0e03c532ea237fcc9f0c4f22416b91512a21c11cff0ecfa61a75d1f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20232026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47b44829bfc497b7e5f3a9777a71f42e165db80fee23dcdb4de56014db3334e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 28 Jul 2020 23:56:22 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Tue, 28 Jul 2020 23:56:25 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:56:26 GMT
VOLUME [/tmp]
# Tue, 28 Jul 2020 23:56:27 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Jul 2020 23:56:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ba63f15824a6daa3f73b57bd9fb04ea01b471f646b703dd08620f13e22d9c`  
		Last Modified: Tue, 28 Jul 2020 23:57:53 GMT  
		Size: 19.8 MB (19772940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d46ed499e4b8c1c9dffea750abe7ad35fba0c431165a394e10283810d33b8d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b691bd363853ce10cedfbe29ea1e8d1e88d7e8eb01da6a3e1baa469c745a1302`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:00:50 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Wed, 29 Jul 2020 00:00:51 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:00:51 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:00:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:00:53 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d477ed11470c756d1112d559be2ea65e2bbdcc367345ed45d17401a98474e`  
		Last Modified: Wed, 29 Jul 2020 00:02:17 GMT  
		Size: 19.5 MB (19492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:0da45cd2c37ec826012e0f2d8a3a4ac0a7be4240a4942a6e40e3aae0f6fb205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3cbe9e62ef26a9ac17b25702754dfbf56dd346850170be90eabd370f24190ef1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24634355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f69007d987e4ed093711f4f306b52ce63b1c19f5ffacd49a1aea1f717e527`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jul 2020 00:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jul 2020 00:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jul 2020 00:20:25 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jul 2020 00:20:26 GMT
CMD ["traefik"]
# Wed, 29 Jul 2020 00:20:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb03716fa366c58de14b0fc81a50daf51f39175c928558e3e82017b5999f233`  
		Last Modified: Wed, 29 Jul 2020 00:21:23 GMT  
		Size: 21.1 MB (21126524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c61f1414a3fbacefede004c9c340def8b1c393630a1c2241a0c9196692c574`  
		Last Modified: Wed, 29 Jul 2020 00:21:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d77a05164ca7fbf64eb55feb97bd9e3d1dfaed181d23bc172d1602203b036b28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddfeb559adfb1011610755afdd099c865a8de51b045331d848b1a58077bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:51:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:51:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:51:48 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:51:52 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:51:55 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46db6761515f08f18c5396f51c8d5fd2ae1c385ff5c12113336ffb79684420`  
		Last Modified: Tue, 28 Jul 2020 23:57:37 GMT  
		Size: 19.8 MB (19772984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368cab0ca49479d26c28e4638f00e78884190c43adf25a35b647ffc70e1209f`  
		Last Modified: Tue, 28 Jul 2020 23:57:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7805105ced1b07c019cb3c420705bb105b1d8da381b76869db624e521af05592
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22913978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e0334e123554f38144482ac92954e0ed970de05727c2d7b6e371f0cda8f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:50:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:50:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:50:28 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:50:29 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:50:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9ba2c08e62ba40494711c8f4e4d32d3d297940e5c04ceaa0594de58ced1744`  
		Last Modified: Wed, 29 Jul 2020 00:02:01 GMT  
		Size: 19.5 MB (19493128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295e2c39b2f8f9a497a542502857a9b10a07977734f37c658f79d6e1a71c57b`  
		Last Modified: Wed, 29 Jul 2020 00:01:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7748a8d390b3a823799597c3f99116d22bf57ce78114fb97adb67b959ea91b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:6539da7d73380435d9f6f38e63c5ff973d88f80b38c09417b7d86723e44a7bbb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381526922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3b1b872cb048b6f3e1953bd97ddf91c9bff263377be6c1aec35af17bd5a347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:00:25 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 08 Sep 2020 20:00:29 GMT
EXPOSE 80
# Tue, 08 Sep 2020 20:00:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 08 Sep 2020 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161157bf7aee194faba8fb8c83b02c05417ca71b3b51ad565ef7220da3ae03c`  
		Last Modified: Tue, 08 Sep 2020 20:03:24 GMT  
		Size: 30.3 MB (30250121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e9f96df13dda9a1e8b837a36603457f53d342e67af86dad22e3bf0c2733d3`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5096b888e43211ea03b1d602bd3435d00ccd2a0204243f2d1e29e321da717f`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c72e13f4d30bccf8dac73850256f6b6bff614348bf9758c492305bd0eeccde`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:picodon`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:picodon` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:picodon` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:picodon` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:picodon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:picodon-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:17067dcaa6b2fca1cf7b4aff8aee13ca55cb43a13e47645598567f9bd09ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3517b63d7a9cd49b7237882fb7c260589b58163c4082d3a37de55a0d93311718
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21585385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab7ee8304c003a86093c588d645758bfed1ac563263e12516c798014a4fc10`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:20:43 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Wed, 29 Jul 2020 00:20:44 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:44 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:20:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:20:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8bcf82fc850436ad04fd66371e38f7611fe76a22b78f47f57ddb8908aa3d6001`  
		Last Modified: Wed, 29 Jul 2020 00:21:33 GMT  
		Size: 21.1 MB (21126327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:200bc13e0e03c532ea237fcc9f0c4f22416b91512a21c11cff0ecfa61a75d1f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20232026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47b44829bfc497b7e5f3a9777a71f42e165db80fee23dcdb4de56014db3334e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 28 Jul 2020 23:56:22 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Tue, 28 Jul 2020 23:56:25 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:56:26 GMT
VOLUME [/tmp]
# Tue, 28 Jul 2020 23:56:27 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Jul 2020 23:56:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ba63f15824a6daa3f73b57bd9fb04ea01b471f646b703dd08620f13e22d9c`  
		Last Modified: Tue, 28 Jul 2020 23:57:53 GMT  
		Size: 19.8 MB (19772940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d46ed499e4b8c1c9dffea750abe7ad35fba0c431165a394e10283810d33b8d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b691bd363853ce10cedfbe29ea1e8d1e88d7e8eb01da6a3e1baa469c745a1302`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:00:50 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Wed, 29 Jul 2020 00:00:51 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:00:51 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:00:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:00:53 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d477ed11470c756d1112d559be2ea65e2bbdcc367345ed45d17401a98474e`  
		Last Modified: Wed, 29 Jul 2020 00:02:17 GMT  
		Size: 19.5 MB (19492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.26`

```console
$ docker pull traefik@sha256:17067dcaa6b2fca1cf7b4aff8aee13ca55cb43a13e47645598567f9bd09ec128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.26` - linux; amd64

```console
$ docker pull traefik@sha256:3517b63d7a9cd49b7237882fb7c260589b58163c4082d3a37de55a0d93311718
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21585385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab7ee8304c003a86093c588d645758bfed1ac563263e12516c798014a4fc10`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:20:43 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Wed, 29 Jul 2020 00:20:44 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:44 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:20:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:20:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8bcf82fc850436ad04fd66371e38f7611fe76a22b78f47f57ddb8908aa3d6001`  
		Last Modified: Wed, 29 Jul 2020 00:21:33 GMT  
		Size: 21.1 MB (21126327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.26` - linux; arm variant v6

```console
$ docker pull traefik@sha256:200bc13e0e03c532ea237fcc9f0c4f22416b91512a21c11cff0ecfa61a75d1f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20232026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47b44829bfc497b7e5f3a9777a71f42e165db80fee23dcdb4de56014db3334e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 28 Jul 2020 23:56:22 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Tue, 28 Jul 2020 23:56:25 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:56:26 GMT
VOLUME [/tmp]
# Tue, 28 Jul 2020 23:56:27 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Jul 2020 23:56:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ba63f15824a6daa3f73b57bd9fb04ea01b471f646b703dd08620f13e22d9c`  
		Last Modified: Tue, 28 Jul 2020 23:57:53 GMT  
		Size: 19.8 MB (19772940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.26` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d46ed499e4b8c1c9dffea750abe7ad35fba0c431165a394e10283810d33b8d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b691bd363853ce10cedfbe29ea1e8d1e88d7e8eb01da6a3e1baa469c745a1302`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 29 Jul 2020 00:00:50 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Wed, 29 Jul 2020 00:00:51 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:00:51 GMT
VOLUME [/tmp]
# Wed, 29 Jul 2020 00:00:52 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jul 2020 00:00:53 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d477ed11470c756d1112d559be2ea65e2bbdcc367345ed45d17401a98474e`  
		Last Modified: Wed, 29 Jul 2020 00:02:17 GMT  
		Size: 19.5 MB (19492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.26-alpine`

```console
$ docker pull traefik@sha256:0da45cd2c37ec826012e0f2d8a3a4ac0a7be4240a4942a6e40e3aae0f6fb205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.26-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3cbe9e62ef26a9ac17b25702754dfbf56dd346850170be90eabd370f24190ef1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24634355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f69007d987e4ed093711f4f306b52ce63b1c19f5ffacd49a1aea1f717e527`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jul 2020 00:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jul 2020 00:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jul 2020 00:20:25 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jul 2020 00:20:26 GMT
CMD ["traefik"]
# Wed, 29 Jul 2020 00:20:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb03716fa366c58de14b0fc81a50daf51f39175c928558e3e82017b5999f233`  
		Last Modified: Wed, 29 Jul 2020 00:21:23 GMT  
		Size: 21.1 MB (21126524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c61f1414a3fbacefede004c9c340def8b1c393630a1c2241a0c9196692c574`  
		Last Modified: Wed, 29 Jul 2020 00:21:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.26-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d77a05164ca7fbf64eb55feb97bd9e3d1dfaed181d23bc172d1602203b036b28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddfeb559adfb1011610755afdd099c865a8de51b045331d848b1a58077bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:51:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:51:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:51:48 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:51:52 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:51:55 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46db6761515f08f18c5396f51c8d5fd2ae1c385ff5c12113336ffb79684420`  
		Last Modified: Tue, 28 Jul 2020 23:57:37 GMT  
		Size: 19.8 MB (19772984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368cab0ca49479d26c28e4638f00e78884190c43adf25a35b647ffc70e1209f`  
		Last Modified: Tue, 28 Jul 2020 23:57:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.26-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7805105ced1b07c019cb3c420705bb105b1d8da381b76869db624e521af05592
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22913978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e0334e123554f38144482ac92954e0ed970de05727c2d7b6e371f0cda8f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:50:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:50:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:50:28 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:50:29 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:50:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9ba2c08e62ba40494711c8f4e4d32d3d297940e5c04ceaa0594de58ced1744`  
		Last Modified: Wed, 29 Jul 2020 00:02:01 GMT  
		Size: 19.5 MB (19493128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295e2c39b2f8f9a497a542502857a9b10a07977734f37c658f79d6e1a71c57b`  
		Last Modified: Wed, 29 Jul 2020 00:01:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.26-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7748a8d390b3a823799597c3f99116d22bf57ce78114fb97adb67b959ea91b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:v1.7.26-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:6539da7d73380435d9f6f38e63c5ff973d88f80b38c09417b7d86723e44a7bbb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381526922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3b1b872cb048b6f3e1953bd97ddf91c9bff263377be6c1aec35af17bd5a347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:00:25 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 08 Sep 2020 20:00:29 GMT
EXPOSE 80
# Tue, 08 Sep 2020 20:00:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 08 Sep 2020 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161157bf7aee194faba8fb8c83b02c05417ca71b3b51ad565ef7220da3ae03c`  
		Last Modified: Tue, 08 Sep 2020 20:03:24 GMT  
		Size: 30.3 MB (30250121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e9f96df13dda9a1e8b837a36603457f53d342e67af86dad22e3bf0c2733d3`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5096b888e43211ea03b1d602bd3435d00ccd2a0204243f2d1e29e321da717f`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c72e13f4d30bccf8dac73850256f6b6bff614348bf9758c492305bd0eeccde`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:0da45cd2c37ec826012e0f2d8a3a4ac0a7be4240a4942a6e40e3aae0f6fb205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3cbe9e62ef26a9ac17b25702754dfbf56dd346850170be90eabd370f24190ef1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24634355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f69007d987e4ed093711f4f306b52ce63b1c19f5ffacd49a1aea1f717e527`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jul 2020 00:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jul 2020 00:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jul 2020 00:20:25 GMT
EXPOSE 80
# Wed, 29 Jul 2020 00:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jul 2020 00:20:26 GMT
CMD ["traefik"]
# Wed, 29 Jul 2020 00:20:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb03716fa366c58de14b0fc81a50daf51f39175c928558e3e82017b5999f233`  
		Last Modified: Wed, 29 Jul 2020 00:21:23 GMT  
		Size: 21.1 MB (21126524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c61f1414a3fbacefede004c9c340def8b1c393630a1c2241a0c9196692c574`  
		Last Modified: Wed, 29 Jul 2020 00:21:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d77a05164ca7fbf64eb55feb97bd9e3d1dfaed181d23bc172d1602203b036b28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23091373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddfeb559adfb1011610755afdd099c865a8de51b045331d848b1a58077bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:51:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:51:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:51:48 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:51:52 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:51:55 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46db6761515f08f18c5396f51c8d5fd2ae1c385ff5c12113336ffb79684420`  
		Last Modified: Tue, 28 Jul 2020 23:57:37 GMT  
		Size: 19.8 MB (19772984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368cab0ca49479d26c28e4638f00e78884190c43adf25a35b647ffc70e1209f`  
		Last Modified: Tue, 28 Jul 2020 23:57:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7805105ced1b07c019cb3c420705bb105b1d8da381b76869db624e521af05592
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22913978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6548e0334e123554f38144482ac92954e0ed970de05727c2d7b6e371f0cda8f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 28 Jul 2020 23:50:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 28 Jul 2020 23:50:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 28 Jul 2020 23:50:28 GMT
EXPOSE 80
# Tue, 28 Jul 2020 23:50:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Jul 2020 23:50:29 GMT
CMD ["traefik"]
# Tue, 28 Jul 2020 23:50:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9ba2c08e62ba40494711c8f4e4d32d3d297940e5c04ceaa0594de58ced1744`  
		Last Modified: Wed, 29 Jul 2020 00:02:01 GMT  
		Size: 19.5 MB (19493128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295e2c39b2f8f9a497a542502857a9b10a07977734f37c658f79d6e1a71c57b`  
		Last Modified: Wed, 29 Jul 2020 00:01:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7748a8d390b3a823799597c3f99116d22bf57ce78114fb97adb67b959ea91b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:6539da7d73380435d9f6f38e63c5ff973d88f80b38c09417b7d86723e44a7bbb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381526922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3b1b872cb048b6f3e1953bd97ddf91c9bff263377be6c1aec35af17bd5a347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:00:25 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.26/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 08 Sep 2020 20:00:29 GMT
EXPOSE 80
# Tue, 08 Sep 2020 20:00:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 08 Sep 2020 20:00:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161157bf7aee194faba8fb8c83b02c05417ca71b3b51ad565ef7220da3ae03c`  
		Last Modified: Tue, 08 Sep 2020 20:03:24 GMT  
		Size: 30.3 MB (30250121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e9f96df13dda9a1e8b837a36603457f53d342e67af86dad22e3bf0c2733d3`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5096b888e43211ea03b1d602bd3435d00ccd2a0204243f2d1e29e321da717f`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c72e13f4d30bccf8dac73850256f6b6bff614348bf9758c492305bd0eeccde`  
		Last Modified: Tue, 08 Sep 2020 20:02:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.3` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3.1`

```console
$ docker pull traefik@sha256:71dc633dd4241ef34076cf3ab01ddb73ee19744328ffd0726fffad857908055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.3.1` - linux; amd64

```console
$ docker pull traefik@sha256:0d52e99b9368467d8ceb094512c0bb6433640a0ec0ca3ad7480a8e5ee4735210
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28379033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3f0281f41e2971ef15020097b1121131936f33ffe2fe51c45f0dd41307d1ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:33:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:33:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:33:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:33:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:33:47 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:33:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8f3d0f88f7612029a50d959dce6df31db9c97804b448eae69a5424e83fb2a`  
		Last Modified: Wed, 30 Sep 2020 00:34:12 GMT  
		Size: 24.9 MB (24871201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c62b1b917cd7bf31e78e480ada93af7311405a50e060e3940d2694c7c1622`  
		Last Modified: Wed, 30 Sep 2020 00:34:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:77efeef61ae68f7655d77ad8f1a00b4ec5846ff00734301c14eef5307c78c420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3988c678784ee736a1f4d380f4e56249e68df7fedda3e0f09ebd4ec97088a905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:56:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:56:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:56:02 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:56:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:56:05 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:56:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65722359773ef006639913726e6f2270f66d5fa38c995a3c3841888bb577c478`  
		Last Modified: Wed, 30 Sep 2020 00:56:41 GMT  
		Size: 23.2 MB (23162088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b449ef6c04ffbcb48a76c292f1d2b138382f3ccdd0cef5a07e91ac0903fecf`  
		Last Modified: Wed, 30 Sep 2020 00:56:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0135bc094f4411d6cd55cffd999b9309067ed15f1e3067a68baed005f67fafdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26104342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e7746ec5ab03964eb553e486422eb47b9083ab25ce42d5e6bab55d9914a38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 30 Sep 2020 00:51:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 30 Sep 2020 00:51:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 30 Sep 2020 00:51:47 GMT
EXPOSE 80
# Wed, 30 Sep 2020 00:51:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Sep 2020 00:51:49 GMT
CMD ["traefik"]
# Wed, 30 Sep 2020 00:51:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107cb7a583f27d3552a316d27d581830ef9c601629b2134fc5281d60862467f`  
		Last Modified: Wed, 30 Sep 2020 00:52:30 GMT  
		Size: 22.7 MB (22683492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5009a074bab7e448e97b37549bb6705af3d6895db74acfd4b3e518dcccc6b592`  
		Last Modified: Wed, 30 Sep 2020 00:52:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:v2.3.1-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:v2.3-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cb304280cbe507eafd7920f4b80306f3151837b8a60c0c2e0f799a0ba1239e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull traefik@sha256:97a0e71e68783984b2d1cb3eef61272320e5c433b57727ca0ddb8f0ae1cca2e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2385663898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d73fbf8524ab8cb6df34938b8b0a7dd767d660d4302d99f761288ed97161e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 30 Sep 2020 01:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.1/traefik_v2.3.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 30 Sep 2020 01:17:37 GMT
EXPOSE 80
# Wed, 30 Sep 2020 01:17:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 30 Sep 2020 01:17:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1fd4e6a50b0ffc66121e6c4458ac569afa32220d376b8dee78a54afdea3f04`  
		Last Modified: Wed, 30 Sep 2020 01:18:21 GMT  
		Size: 34.4 MB (34387102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0147705163f048eb7010f9b1f3d9d2935ffb29b8ed03495d41ca1d8743b287`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e310db912dce00d88f8404bf2c994f89213ec10cf37a39a40943834c4b2d0575`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00372149856d2b440437fb779f341f7b0c9a73b7264edc18f7066b758c1584`  
		Last Modified: Wed, 30 Sep 2020 01:18:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
