<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.24`](#traefik1724)
-	[`traefik:1.7.24-alpine`](#traefik1724-alpine)
-	[`traefik:1.7.24-windowsservercore-1809`](#traefik1724-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.2`](#traefik22)
-	[`traefik:2.2.0`](#traefik220)
-	[`traefik:2.2.0-windowsservercore-1809`](#traefik220-windowsservercore-1809)
-	[`traefik:2.2-windowsservercore-1809`](#traefik22-windowsservercore-1809)
-	[`traefik:chevrotin`](#traefikchevrotin)
-	[`traefik:chevrotin-windowsservercore-1809`](#traefikchevrotin-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.24`](#traefikv1724)
-	[`traefik:v1.7.24-alpine`](#traefikv1724-alpine)
-	[`traefik:v1.7.24-windowsservercore-1809`](#traefikv1724-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.2`](#traefikv22)
-	[`traefik:v2.2.0`](#traefikv220)
-	[`traefik:v2.2.0-windowsservercore-1809`](#traefikv220-windowsservercore-1809)
-	[`traefik:v2.2-windowsservercore-1809`](#traefikv22-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:47bec236a121a07703e27fc3e18c201ae0241cff1038ea2faf5d05bf5ea82286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:bec5a86cd327d82a50fe89aae5c57d49a13bb9c7fe82fcdd7c886adf09645801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100389fa48aa58f1587f27467ac7f319ca8724b7bbad55ee09ada0de310a3bf4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 22:24:07 GMT
COPY file:1f3cec74af68ac254dc1c90001edd0f7a71f8e42168f4523b5b170d518e50e2a in / 
# Wed, 25 Mar 2020 22:24:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:24:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 22:24:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 22:24:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6f9aa7cec283ff91d23b1d8e88e428fd21f67593d121f450a42173fe6443f190`  
		Last Modified: Wed, 25 Mar 2020 22:24:49 GMT  
		Size: 21.1 MB (21119254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1733e40d59ca54506c6b3859245878b29270da0d17eaa5b10322bc83cf5749bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2ff4474d538ce68e1599c24ef3227b9087dbfa625a1049a3172fe56a021b9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:50:06 GMT
COPY file:5fc84f7de0956e9c09bc8249cedc256b1ebfbbdf7a970a1b03cbc35342bc98d8 in / 
# Wed, 25 Mar 2020 21:50:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:50:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:50:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:50:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:cc2e8d91f8cdcad6fef81a6606a958dc4fa4ffe856944124f101909ef0e2a6de`  
		Last Modified: Wed, 25 Mar 2020 21:51:04 GMT  
		Size: 19.8 MB (19771060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7f26aa867bbfa1637f66f2faee17fd66549e441185789b64aa07f0326e75f321
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b0a67ae19f09c258a8a530bf8f7315c03f0157c72a093a495d017a4d8032a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:44:21 GMT
COPY file:0347658f660b1b9c0951c6a64bfc0f8a407487940ca58f7d6da08472f61358db in / 
# Wed, 25 Mar 2020 21:44:21 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:22 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:44:23 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:44:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e41d3d1eaac6c67b9dab999e93238a86c8df48b874e4225dd36534ce81905c58`  
		Last Modified: Wed, 25 Mar 2020 21:45:23 GMT  
		Size: 19.5 MB (19491184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.24`

```console
$ docker pull traefik@sha256:47bec236a121a07703e27fc3e18c201ae0241cff1038ea2faf5d05bf5ea82286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.24` - linux; amd64

```console
$ docker pull traefik@sha256:bec5a86cd327d82a50fe89aae5c57d49a13bb9c7fe82fcdd7c886adf09645801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100389fa48aa58f1587f27467ac7f319ca8724b7bbad55ee09ada0de310a3bf4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 22:24:07 GMT
COPY file:1f3cec74af68ac254dc1c90001edd0f7a71f8e42168f4523b5b170d518e50e2a in / 
# Wed, 25 Mar 2020 22:24:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:24:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 22:24:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 22:24:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6f9aa7cec283ff91d23b1d8e88e428fd21f67593d121f450a42173fe6443f190`  
		Last Modified: Wed, 25 Mar 2020 22:24:49 GMT  
		Size: 21.1 MB (21119254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.24` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1733e40d59ca54506c6b3859245878b29270da0d17eaa5b10322bc83cf5749bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2ff4474d538ce68e1599c24ef3227b9087dbfa625a1049a3172fe56a021b9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:50:06 GMT
COPY file:5fc84f7de0956e9c09bc8249cedc256b1ebfbbdf7a970a1b03cbc35342bc98d8 in / 
# Wed, 25 Mar 2020 21:50:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:50:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:50:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:50:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:cc2e8d91f8cdcad6fef81a6606a958dc4fa4ffe856944124f101909ef0e2a6de`  
		Last Modified: Wed, 25 Mar 2020 21:51:04 GMT  
		Size: 19.8 MB (19771060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.24` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7f26aa867bbfa1637f66f2faee17fd66549e441185789b64aa07f0326e75f321
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b0a67ae19f09c258a8a530bf8f7315c03f0157c72a093a495d017a4d8032a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:44:21 GMT
COPY file:0347658f660b1b9c0951c6a64bfc0f8a407487940ca58f7d6da08472f61358db in / 
# Wed, 25 Mar 2020 21:44:21 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:22 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:44:23 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:44:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e41d3d1eaac6c67b9dab999e93238a86c8df48b874e4225dd36534ce81905c58`  
		Last Modified: Wed, 25 Mar 2020 21:45:23 GMT  
		Size: 19.5 MB (19491184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.24-alpine`

```console
$ docker pull traefik@sha256:73a1d2140bcc56820ffc6431e2c558abc468ef533735be6b5914ee1fdf91cfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.24-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:178c67d6e375ce45264f1a47eef709bca9928ac85badaa8f0d877059d5f37b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4204cec7f48d0cc16d69e25ac8a29074a4782bc92622e55ec94c3b11f5b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:45 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:45 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b9cb6e408627ad0a100994d33c802c10828d8373fb7234572e0235fca9d7294c`  
		Last Modified: Wed, 25 Mar 2020 22:24:39 GMT  
		Size: 21.1 MB (21119525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c0f262e2748518c0df991fbe02ea98c1eb9fc9a355c8eb8ca0c4cd4b43b55`  
		Last Modified: Wed, 25 Mar 2020 22:24:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.24-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:17b4d2c074c9b3191e3317f2050b04e141652c4ab344af8838051efb27356dac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23089627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e6ab20ddb1e5c3d6eecb2000b7f52b5ca9028ea29b44f95efb3203c49659d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:59 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:37:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:37:01 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:37:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:389a57d2621ef39458c942b4e2bbe4470db7345a13124310e33afe4bb39bded9`  
		Last Modified: Thu, 23 Apr 2020 22:39:50 GMT  
		Size: 19.8 MB (19771237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c2431ddb4c9874cbbc1879aca65157542c05ce67bb2c2525f0773fe3d32af`  
		Last Modified: Thu, 23 Apr 2020 22:39:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.24-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2960a1bff52c4e20800f297ac9491661804f276e4c167c5f477cae56e45bf482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cc83f1529223ab41bc828bcbd1d0b3937e49b4786ab5851376c284cac448b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:44:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:44:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:44:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:44:08 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46883925a5415d0997e2373210f823fdb48428220d78047fe8ff251f7fc6810`  
		Last Modified: Wed, 25 Mar 2020 21:45:06 GMT  
		Size: 19.5 MB (19491362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800e005e5decf1b215e0d6adfd8871dafad512432f8e624b6e59c927639d73`  
		Last Modified: Wed, 25 Mar 2020 21:44:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.24-windowsservercore-1809`

```console
$ docker pull traefik@sha256:61137451597c958da8f15329d611daf9d9c1353a5a27b74704c3cc7bc362c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:1.7.24-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:4b4169ec77160535d649346347a778e1d6612ef6057d697ffbad275da229e55b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296496615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0578d45a372d7bb11fa88819963bbcb5dfafd0df505b06ca8bd64f03b9d1ec40`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:20:23 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Apr 2020 21:20:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:20:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:20:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b8ad3eb3871fb6c5e9344ca021c3494d9fcd12fa3b6c11137c89e3c1c71f0`  
		Last Modified: Wed, 15 Apr 2020 21:21:24 GMT  
		Size: 25.8 MB (25784800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2381bf9e2009120c65afacda51f1bb70ae0771110f3e4404c8e54ec35bfc5`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cc1e0bfd64f984598cc75b1c5ed3e88963171b13f8521f7dc2584f60c9df9`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204d9c77ffdfdab86ea3b3e0b57721f679dd3972752d8db98d6376c2f09d2bf`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:73a1d2140bcc56820ffc6431e2c558abc468ef533735be6b5914ee1fdf91cfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:178c67d6e375ce45264f1a47eef709bca9928ac85badaa8f0d877059d5f37b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4204cec7f48d0cc16d69e25ac8a29074a4782bc92622e55ec94c3b11f5b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:45 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:45 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b9cb6e408627ad0a100994d33c802c10828d8373fb7234572e0235fca9d7294c`  
		Last Modified: Wed, 25 Mar 2020 22:24:39 GMT  
		Size: 21.1 MB (21119525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c0f262e2748518c0df991fbe02ea98c1eb9fc9a355c8eb8ca0c4cd4b43b55`  
		Last Modified: Wed, 25 Mar 2020 22:24:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:17b4d2c074c9b3191e3317f2050b04e141652c4ab344af8838051efb27356dac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23089627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e6ab20ddb1e5c3d6eecb2000b7f52b5ca9028ea29b44f95efb3203c49659d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:59 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:37:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:37:01 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:37:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:389a57d2621ef39458c942b4e2bbe4470db7345a13124310e33afe4bb39bded9`  
		Last Modified: Thu, 23 Apr 2020 22:39:50 GMT  
		Size: 19.8 MB (19771237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c2431ddb4c9874cbbc1879aca65157542c05ce67bb2c2525f0773fe3d32af`  
		Last Modified: Thu, 23 Apr 2020 22:39:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2960a1bff52c4e20800f297ac9491661804f276e4c167c5f477cae56e45bf482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cc83f1529223ab41bc828bcbd1d0b3937e49b4786ab5851376c284cac448b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:44:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:44:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:44:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:44:08 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46883925a5415d0997e2373210f823fdb48428220d78047fe8ff251f7fc6810`  
		Last Modified: Wed, 25 Mar 2020 21:45:06 GMT  
		Size: 19.5 MB (19491362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800e005e5decf1b215e0d6adfd8871dafad512432f8e624b6e59c927639d73`  
		Last Modified: Wed, 25 Mar 2020 21:44:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:61137451597c958da8f15329d611daf9d9c1353a5a27b74704c3cc7bc362c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:4b4169ec77160535d649346347a778e1d6612ef6057d697ffbad275da229e55b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296496615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0578d45a372d7bb11fa88819963bbcb5dfafd0df505b06ca8bd64f03b9d1ec40`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:20:23 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Apr 2020 21:20:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:20:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:20:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b8ad3eb3871fb6c5e9344ca021c3494d9fcd12fa3b6c11137c89e3c1c71f0`  
		Last Modified: Wed, 15 Apr 2020 21:21:24 GMT  
		Size: 25.8 MB (25784800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2381bf9e2009120c65afacda51f1bb70ae0771110f3e4404c8e54ec35bfc5`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cc1e0bfd64f984598cc75b1c5ed3e88963171b13f8521f7dc2584f60c9df9`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204d9c77ffdfdab86ea3b3e0b57721f679dd3972752d8db98d6376c2f09d2bf`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2.0` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:2.2.0-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:2.2-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:47bec236a121a07703e27fc3e18c201ae0241cff1038ea2faf5d05bf5ea82286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:bec5a86cd327d82a50fe89aae5c57d49a13bb9c7fe82fcdd7c886adf09645801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100389fa48aa58f1587f27467ac7f319ca8724b7bbad55ee09ada0de310a3bf4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 22:24:07 GMT
COPY file:1f3cec74af68ac254dc1c90001edd0f7a71f8e42168f4523b5b170d518e50e2a in / 
# Wed, 25 Mar 2020 22:24:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:24:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 22:24:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 22:24:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6f9aa7cec283ff91d23b1d8e88e428fd21f67593d121f450a42173fe6443f190`  
		Last Modified: Wed, 25 Mar 2020 22:24:49 GMT  
		Size: 21.1 MB (21119254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1733e40d59ca54506c6b3859245878b29270da0d17eaa5b10322bc83cf5749bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2ff4474d538ce68e1599c24ef3227b9087dbfa625a1049a3172fe56a021b9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:50:06 GMT
COPY file:5fc84f7de0956e9c09bc8249cedc256b1ebfbbdf7a970a1b03cbc35342bc98d8 in / 
# Wed, 25 Mar 2020 21:50:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:50:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:50:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:50:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:cc2e8d91f8cdcad6fef81a6606a958dc4fa4ffe856944124f101909ef0e2a6de`  
		Last Modified: Wed, 25 Mar 2020 21:51:04 GMT  
		Size: 19.8 MB (19771060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7f26aa867bbfa1637f66f2faee17fd66549e441185789b64aa07f0326e75f321
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b0a67ae19f09c258a8a530bf8f7315c03f0157c72a093a495d017a4d8032a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:44:21 GMT
COPY file:0347658f660b1b9c0951c6a64bfc0f8a407487940ca58f7d6da08472f61358db in / 
# Wed, 25 Mar 2020 21:44:21 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:22 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:44:23 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:44:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e41d3d1eaac6c67b9dab999e93238a86c8df48b874e4225dd36534ce81905c58`  
		Last Modified: Wed, 25 Mar 2020 21:45:23 GMT  
		Size: 19.5 MB (19491184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:73a1d2140bcc56820ffc6431e2c558abc468ef533735be6b5914ee1fdf91cfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:178c67d6e375ce45264f1a47eef709bca9928ac85badaa8f0d877059d5f37b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4204cec7f48d0cc16d69e25ac8a29074a4782bc92622e55ec94c3b11f5b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:45 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:45 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b9cb6e408627ad0a100994d33c802c10828d8373fb7234572e0235fca9d7294c`  
		Last Modified: Wed, 25 Mar 2020 22:24:39 GMT  
		Size: 21.1 MB (21119525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c0f262e2748518c0df991fbe02ea98c1eb9fc9a355c8eb8ca0c4cd4b43b55`  
		Last Modified: Wed, 25 Mar 2020 22:24:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:17b4d2c074c9b3191e3317f2050b04e141652c4ab344af8838051efb27356dac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23089627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e6ab20ddb1e5c3d6eecb2000b7f52b5ca9028ea29b44f95efb3203c49659d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:59 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:37:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:37:01 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:37:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:389a57d2621ef39458c942b4e2bbe4470db7345a13124310e33afe4bb39bded9`  
		Last Modified: Thu, 23 Apr 2020 22:39:50 GMT  
		Size: 19.8 MB (19771237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c2431ddb4c9874cbbc1879aca65157542c05ce67bb2c2525f0773fe3d32af`  
		Last Modified: Thu, 23 Apr 2020 22:39:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2960a1bff52c4e20800f297ac9491661804f276e4c167c5f477cae56e45bf482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cc83f1529223ab41bc828bcbd1d0b3937e49b4786ab5851376c284cac448b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:44:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:44:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:44:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:44:08 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46883925a5415d0997e2373210f823fdb48428220d78047fe8ff251f7fc6810`  
		Last Modified: Wed, 25 Mar 2020 21:45:06 GMT  
		Size: 19.5 MB (19491362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800e005e5decf1b215e0d6adfd8871dafad512432f8e624b6e59c927639d73`  
		Last Modified: Wed, 25 Mar 2020 21:44:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:61137451597c958da8f15329d611daf9d9c1353a5a27b74704c3cc7bc362c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:4b4169ec77160535d649346347a778e1d6612ef6057d697ffbad275da229e55b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296496615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0578d45a372d7bb11fa88819963bbcb5dfafd0df505b06ca8bd64f03b9d1ec40`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:20:23 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Apr 2020 21:20:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:20:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:20:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b8ad3eb3871fb6c5e9344ca021c3494d9fcd12fa3b6c11137c89e3c1c71f0`  
		Last Modified: Wed, 15 Apr 2020 21:21:24 GMT  
		Size: 25.8 MB (25784800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2381bf9e2009120c65afacda51f1bb70ae0771110f3e4404c8e54ec35bfc5`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cc1e0bfd64f984598cc75b1c5ed3e88963171b13f8521f7dc2584f60c9df9`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204d9c77ffdfdab86ea3b3e0b57721f679dd3972752d8db98d6376c2f09d2bf`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:47bec236a121a07703e27fc3e18c201ae0241cff1038ea2faf5d05bf5ea82286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:bec5a86cd327d82a50fe89aae5c57d49a13bb9c7fe82fcdd7c886adf09645801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100389fa48aa58f1587f27467ac7f319ca8724b7bbad55ee09ada0de310a3bf4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 22:24:07 GMT
COPY file:1f3cec74af68ac254dc1c90001edd0f7a71f8e42168f4523b5b170d518e50e2a in / 
# Wed, 25 Mar 2020 22:24:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:24:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 22:24:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 22:24:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6f9aa7cec283ff91d23b1d8e88e428fd21f67593d121f450a42173fe6443f190`  
		Last Modified: Wed, 25 Mar 2020 22:24:49 GMT  
		Size: 21.1 MB (21119254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1733e40d59ca54506c6b3859245878b29270da0d17eaa5b10322bc83cf5749bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2ff4474d538ce68e1599c24ef3227b9087dbfa625a1049a3172fe56a021b9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:50:06 GMT
COPY file:5fc84f7de0956e9c09bc8249cedc256b1ebfbbdf7a970a1b03cbc35342bc98d8 in / 
# Wed, 25 Mar 2020 21:50:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:50:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:50:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:50:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:cc2e8d91f8cdcad6fef81a6606a958dc4fa4ffe856944124f101909ef0e2a6de`  
		Last Modified: Wed, 25 Mar 2020 21:51:04 GMT  
		Size: 19.8 MB (19771060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7f26aa867bbfa1637f66f2faee17fd66549e441185789b64aa07f0326e75f321
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b0a67ae19f09c258a8a530bf8f7315c03f0157c72a093a495d017a4d8032a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:44:21 GMT
COPY file:0347658f660b1b9c0951c6a64bfc0f8a407487940ca58f7d6da08472f61358db in / 
# Wed, 25 Mar 2020 21:44:21 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:22 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:44:23 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:44:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e41d3d1eaac6c67b9dab999e93238a86c8df48b874e4225dd36534ce81905c58`  
		Last Modified: Wed, 25 Mar 2020 21:45:23 GMT  
		Size: 19.5 MB (19491184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.24`

```console
$ docker pull traefik@sha256:47bec236a121a07703e27fc3e18c201ae0241cff1038ea2faf5d05bf5ea82286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.24` - linux; amd64

```console
$ docker pull traefik@sha256:bec5a86cd327d82a50fe89aae5c57d49a13bb9c7fe82fcdd7c886adf09645801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100389fa48aa58f1587f27467ac7f319ca8724b7bbad55ee09ada0de310a3bf4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 22:24:07 GMT
COPY file:1f3cec74af68ac254dc1c90001edd0f7a71f8e42168f4523b5b170d518e50e2a in / 
# Wed, 25 Mar 2020 22:24:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:24:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 22:24:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 22:24:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6f9aa7cec283ff91d23b1d8e88e428fd21f67593d121f450a42173fe6443f190`  
		Last Modified: Wed, 25 Mar 2020 22:24:49 GMT  
		Size: 21.1 MB (21119254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.24` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1733e40d59ca54506c6b3859245878b29270da0d17eaa5b10322bc83cf5749bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2ff4474d538ce68e1599c24ef3227b9087dbfa625a1049a3172fe56a021b9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:50:06 GMT
COPY file:5fc84f7de0956e9c09bc8249cedc256b1ebfbbdf7a970a1b03cbc35342bc98d8 in / 
# Wed, 25 Mar 2020 21:50:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:50:07 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:50:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:50:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:cc2e8d91f8cdcad6fef81a6606a958dc4fa4ffe856944124f101909ef0e2a6de`  
		Last Modified: Wed, 25 Mar 2020 21:51:04 GMT  
		Size: 19.8 MB (19771060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.24` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7f26aa867bbfa1637f66f2faee17fd66549e441185789b64aa07f0326e75f321
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b0a67ae19f09c258a8a530bf8f7315c03f0157c72a093a495d017a4d8032a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 25 Mar 2020 21:44:21 GMT
COPY file:0347658f660b1b9c0951c6a64bfc0f8a407487940ca58f7d6da08472f61358db in / 
# Wed, 25 Mar 2020 21:44:21 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:22 GMT
VOLUME [/tmp]
# Wed, 25 Mar 2020 21:44:23 GMT
ENTRYPOINT ["/traefik"]
# Wed, 25 Mar 2020 21:44:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:e41d3d1eaac6c67b9dab999e93238a86c8df48b874e4225dd36534ce81905c58`  
		Last Modified: Wed, 25 Mar 2020 21:45:23 GMT  
		Size: 19.5 MB (19491184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.24-alpine`

```console
$ docker pull traefik@sha256:73a1d2140bcc56820ffc6431e2c558abc468ef533735be6b5914ee1fdf91cfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.24-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:178c67d6e375ce45264f1a47eef709bca9928ac85badaa8f0d877059d5f37b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4204cec7f48d0cc16d69e25ac8a29074a4782bc92622e55ec94c3b11f5b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:45 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:45 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b9cb6e408627ad0a100994d33c802c10828d8373fb7234572e0235fca9d7294c`  
		Last Modified: Wed, 25 Mar 2020 22:24:39 GMT  
		Size: 21.1 MB (21119525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c0f262e2748518c0df991fbe02ea98c1eb9fc9a355c8eb8ca0c4cd4b43b55`  
		Last Modified: Wed, 25 Mar 2020 22:24:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.24-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:17b4d2c074c9b3191e3317f2050b04e141652c4ab344af8838051efb27356dac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23089627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e6ab20ddb1e5c3d6eecb2000b7f52b5ca9028ea29b44f95efb3203c49659d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:59 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:37:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:37:01 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:37:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:389a57d2621ef39458c942b4e2bbe4470db7345a13124310e33afe4bb39bded9`  
		Last Modified: Thu, 23 Apr 2020 22:39:50 GMT  
		Size: 19.8 MB (19771237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c2431ddb4c9874cbbc1879aca65157542c05ce67bb2c2525f0773fe3d32af`  
		Last Modified: Thu, 23 Apr 2020 22:39:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.24-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2960a1bff52c4e20800f297ac9491661804f276e4c167c5f477cae56e45bf482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cc83f1529223ab41bc828bcbd1d0b3937e49b4786ab5851376c284cac448b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:44:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:44:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:44:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:44:08 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46883925a5415d0997e2373210f823fdb48428220d78047fe8ff251f7fc6810`  
		Last Modified: Wed, 25 Mar 2020 21:45:06 GMT  
		Size: 19.5 MB (19491362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800e005e5decf1b215e0d6adfd8871dafad512432f8e624b6e59c927639d73`  
		Last Modified: Wed, 25 Mar 2020 21:44:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.24-windowsservercore-1809`

```console
$ docker pull traefik@sha256:61137451597c958da8f15329d611daf9d9c1353a5a27b74704c3cc7bc362c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:v1.7.24-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:4b4169ec77160535d649346347a778e1d6612ef6057d697ffbad275da229e55b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296496615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0578d45a372d7bb11fa88819963bbcb5dfafd0df505b06ca8bd64f03b9d1ec40`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:20:23 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Apr 2020 21:20:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:20:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:20:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b8ad3eb3871fb6c5e9344ca021c3494d9fcd12fa3b6c11137c89e3c1c71f0`  
		Last Modified: Wed, 15 Apr 2020 21:21:24 GMT  
		Size: 25.8 MB (25784800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2381bf9e2009120c65afacda51f1bb70ae0771110f3e4404c8e54ec35bfc5`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cc1e0bfd64f984598cc75b1c5ed3e88963171b13f8521f7dc2584f60c9df9`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204d9c77ffdfdab86ea3b3e0b57721f679dd3972752d8db98d6376c2f09d2bf`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:73a1d2140bcc56820ffc6431e2c558abc468ef533735be6b5914ee1fdf91cfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:178c67d6e375ce45264f1a47eef709bca9928ac85badaa8f0d877059d5f37b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4204cec7f48d0cc16d69e25ac8a29074a4782bc92622e55ec94c3b11f5b479`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:45 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:45 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b9cb6e408627ad0a100994d33c802c10828d8373fb7234572e0235fca9d7294c`  
		Last Modified: Wed, 25 Mar 2020 22:24:39 GMT  
		Size: 21.1 MB (21119525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5c0f262e2748518c0df991fbe02ea98c1eb9fc9a355c8eb8ca0c4cd4b43b55`  
		Last Modified: Wed, 25 Mar 2020 22:24:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:17b4d2c074c9b3191e3317f2050b04e141652c4ab344af8838051efb27356dac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23089627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e6ab20ddb1e5c3d6eecb2000b7f52b5ca9028ea29b44f95efb3203c49659d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:59 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:37:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:37:01 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:37:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:389a57d2621ef39458c942b4e2bbe4470db7345a13124310e33afe4bb39bded9`  
		Last Modified: Thu, 23 Apr 2020 22:39:50 GMT  
		Size: 19.8 MB (19771237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433c2431ddb4c9874cbbc1879aca65157542c05ce67bb2c2525f0773fe3d32af`  
		Last Modified: Thu, 23 Apr 2020 22:39:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2960a1bff52c4e20800f297ac9491661804f276e4c167c5f477cae56e45bf482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cc83f1529223ab41bc828bcbd1d0b3937e49b4786ab5851376c284cac448b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:44:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:44:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:44:07 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:44:08 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46883925a5415d0997e2373210f823fdb48428220d78047fe8ff251f7fc6810`  
		Last Modified: Wed, 25 Mar 2020 21:45:06 GMT  
		Size: 19.5 MB (19491362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800e005e5decf1b215e0d6adfd8871dafad512432f8e624b6e59c927639d73`  
		Last Modified: Wed, 25 Mar 2020 21:44:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:61137451597c958da8f15329d611daf9d9c1353a5a27b74704c3cc7bc362c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:4b4169ec77160535d649346347a778e1d6612ef6057d697ffbad275da229e55b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296496615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0578d45a372d7bb11fa88819963bbcb5dfafd0df505b06ca8bd64f03b9d1ec40`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:20:23 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Apr 2020 21:20:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:20:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:20:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b8ad3eb3871fb6c5e9344ca021c3494d9fcd12fa3b6c11137c89e3c1c71f0`  
		Last Modified: Wed, 15 Apr 2020 21:21:24 GMT  
		Size: 25.8 MB (25784800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2381bf9e2009120c65afacda51f1bb70ae0771110f3e4404c8e54ec35bfc5`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cc1e0bfd64f984598cc75b1c5ed3e88963171b13f8521f7dc2584f60c9df9`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204d9c77ffdfdab86ea3b3e0b57721f679dd3972752d8db98d6376c2f09d2bf`  
		Last Modified: Wed, 15 Apr 2020 21:21:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0`

```console
$ docker pull traefik@sha256:11a9684c70d92f36e7a845128d6e7ea472554852b2fbc14b6bc704e49efcc361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2.0` - linux; amd64

```console
$ docker pull traefik@sha256:14591144dc8a5dc71dea7ac160683f5578bfbc9cf97aeb042270f843c68e0b17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24783196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085ead62a4d4b06c34090d14b0f0b516d44777c7b9d71d36f09410f0aef9e5f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 22:23:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 22:23:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 22:23:38 GMT
EXPOSE 80
# Wed, 25 Mar 2020 22:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 22:23:38 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 22:23:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dc367a6045f5900ec7708f21ef9df2d7ad7483e36d85979057667e0b3866bdb6`  
		Last Modified: Wed, 25 Mar 2020 22:24:27 GMT  
		Size: 21.3 MB (21285429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff697159d0030e6aa732f628239bba97a20cfba5cc1c0de77e822a794efedd5c`  
		Last Modified: Wed, 25 Mar 2020 22:24:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c62920492c0306093ceb6f6c68e9d3160f01da9e50ccb3a46def877b8dc10f48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd5cbce915b15d4a61e495965bfe06d53d54d997a57b4e947307ad6ecf5beb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Apr 2020 22:36:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Apr 2020 22:36:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Apr 2020 22:36:41 GMT
EXPOSE 80
# Thu, 23 Apr 2020 22:36:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 22:36:43 GMT
CMD ["traefik"]
# Thu, 23 Apr 2020 22:36:44 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:47de4efdca0fea17f0e06d3dbf01b9fb6ddacceb0e536e3346d5dfbc53173b7a`  
		Last Modified: Thu, 23 Apr 2020 22:39:30 GMT  
		Size: 20.0 MB (19988878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c90c2a0da73caa9c34384ef417269697a38010e34e03bcd43d69ef0889053`  
		Last Modified: Thu, 23 Apr 2020 22:39:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6d0a99e202bc3f732000a78b696281369b771234893fff22106471f3d65daffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23053503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0e36d477b886f5ede8ae4753d1cef2acd7570659836ba0f4ab2e743d55bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 25 Mar 2020 21:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 25 Mar 2020 21:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 25 Mar 2020 21:43:55 GMT
EXPOSE 80
# Wed, 25 Mar 2020 21:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Mar 2020 21:43:56 GMT
CMD ["traefik"]
# Wed, 25 Mar 2020 21:43:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b612f6b713c999a6de7f98b8c222af24cf379ecb710e67b5c5c51d55510f28`  
		Last Modified: Wed, 25 Mar 2020 21:44:44 GMT  
		Size: 19.6 MB (19633812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ff5f94664c57720083b9b43ff6fe9b9d232b33ea28f07dfc57140fac200f6`  
		Last Modified: Wed, 25 Mar 2020 21:44:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:v2.2.0-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:v2.2-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:5cd37215ff336d5088132aa1b7ab5181672cc9cfb98449c8939d9e76527d5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull traefik@sha256:27294c1a1d580b0163e45a21d41436ddd407923adfa55fc5cc9d66a045b4778a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296630581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e41d46f735bd1ea7414451f7b43be56d2226358fd157fd26845bf4f22c8e3b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 21:19:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0/traefik_v2.2.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 15 Apr 2020 21:19:27 GMT
EXPOSE 80
# Wed, 15 Apr 2020 21:19:29 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Apr 2020 21:19:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6882ac7e421413d744527f8e3436836a9975061deb9f09982b57422ab7b015`  
		Last Modified: Wed, 15 Apr 2020 21:20:58 GMT  
		Size: 25.9 MB (25918816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423691ba5eccfd282fbcfaa475cc5068b4ab4eb2a5e9a33af84dfa9024b11b00`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a00a51e357ead2b0d9cc5279dbfe48f31b56c62a5204963e430445265270f8`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d82edeef8498bbfccea22d382d39fae344616a8f745e704f914ddb6cd3e0d6`  
		Last Modified: Wed, 15 Apr 2020 21:20:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
