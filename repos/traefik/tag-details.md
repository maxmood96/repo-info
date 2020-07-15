<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.25`](#traefik1725)
-	[`traefik:1.7.25-alpine`](#traefik1725-alpine)
-	[`traefik:1.7.25-windowsservercore-1809`](#traefik1725-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.2`](#traefik22)
-	[`traefik:2.2.5`](#traefik225)
-	[`traefik:2.2.5-windowsservercore-1809`](#traefik225-windowsservercore-1809)
-	[`traefik:2.2-windowsservercore-1809`](#traefik22-windowsservercore-1809)
-	[`traefik:2.3`](#traefik23)
-	[`traefik:2.3.0-rc2`](#traefik230-rc2)
-	[`traefik:2.3.0-rc2-windowsservercore-1809`](#traefik230-rc2-windowsservercore-1809)
-	[`traefik:2.3-windowsservercore-1809`](#traefik23-windowsservercore-1809)
-	[`traefik:chevrotin`](#traefikchevrotin)
-	[`traefik:chevrotin-windowsservercore-1809`](#traefikchevrotin-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:picodon`](#traefikpicodon)
-	[`traefik:picodon-windowsservercore-1809`](#traefikpicodon-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.25`](#traefikv1725)
-	[`traefik:v1.7.25-alpine`](#traefikv1725-alpine)
-	[`traefik:v1.7.25-windowsservercore-1809`](#traefikv1725-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.2`](#traefikv22)
-	[`traefik:v2.2.5`](#traefikv225)
-	[`traefik:v2.2.5-windowsservercore-1809`](#traefikv225-windowsservercore-1809)
-	[`traefik:v2.2-windowsservercore-1809`](#traefikv22-windowsservercore-1809)
-	[`traefik:v2.3`](#traefikv23)
-	[`traefik:v2.3.0-rc2`](#traefikv230-rc2)
-	[`traefik:v2.3.0-rc2-windowsservercore-1809`](#traefikv230-rc2-windowsservercore-1809)
-	[`traefik:v2.3-windowsservercore-1809`](#traefikv23-windowsservercore-1809)
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

## `traefik:1.7.25`

**does not exist** (yet?)

## `traefik:1.7.25-alpine`

**does not exist** (yet?)

## `traefik:1.7.25-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:d1fa651db4263209a207b221bcdeef6d1e969e40322c732666ebde42ae575dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:b577b9f4080e4ef05bee4f07f5d9aee2ae633a0a9625ccfb259a91a51496e3ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cf7f226483cf8ca1e19a0211591404d87c114a0460433db2fe23b2abf7384b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 17:33:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 17:33:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 17:33:39 GMT
EXPOSE 80
# Fri, 24 Apr 2020 17:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 17:33:40 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 17:33:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dbc48c2837a07f77334f15fed847d0310fbf620c555a33eed7a3e26b51948a87`  
		Last Modified: Fri, 24 Apr 2020 17:34:29 GMT  
		Size: 21.1 MB (21119551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6175123f5656afbcf94fb6f762724b1bd3f696ffeca9ca234c34f9ec1d6dfab`  
		Last Modified: Fri, 24 Apr 2020 17:34:25 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:58b5d2f623c63053b8a85c6b67a9a5d0f8d17b50fd43968eb064bc67739cf333
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22912220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6f782ec08f75c4c408f12f558daea37bf0136ac981565293da732a7ff753d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 12:14:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 12:15:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 12:15:00 GMT
EXPOSE 80
# Fri, 24 Apr 2020 12:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 12:15:02 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 12:15:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f2f2951777aa5ad9aa3787e0b88d017c3f2205f82636987318f26d9c14f7d494`  
		Last Modified: Fri, 24 Apr 2020 12:44:13 GMT  
		Size: 19.5 MB (19491370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde6fde915691a2d658b0bd77609f98105e33b8eab269515e05581ff4f7adaa4`  
		Last Modified: Fri, 24 Apr 2020 12:44:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eacafda7d2c278b363ac872f55010732694353005e2389acfc1ceb44075077e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:0a029fd9eed33b845a5e3310794a460ae84a181134d3907530d5ee1400471b67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319804976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548b1fbad1894614c6e1de2087dee68ef22dd882da81ae09c1289fe1a083a5a3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:43:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 10 Jun 2020 20:43:24 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:43:25 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:43:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59faa3247876c4be4c372d08763d6345d911c5aa3b1ba2fa4871e56b76458e`  
		Last Modified: Wed, 10 Jun 2020 20:44:33 GMT  
		Size: 25.9 MB (25886159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9281fc9a05026ec10cec5645e56b5a45e1009e632db41372276dde862cd65ef`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206aa039341a413a8754154d6b3f40205f7afad3021409a9f2c30726520b62fa`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f5428df4a8b754cead9e80fa6879d695a0a8ce92c161e9dd88e811d56a9251`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.5`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2.5` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:2.2.5-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:2.2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3`

**does not exist** (yet?)

## `traefik:2.3.0-rc2`

**does not exist** (yet?)

## `traefik:2.3.0-rc2-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:2.3-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
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
$ docker pull traefik@sha256:d1fa651db4263209a207b221bcdeef6d1e969e40322c732666ebde42ae575dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:b577b9f4080e4ef05bee4f07f5d9aee2ae633a0a9625ccfb259a91a51496e3ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cf7f226483cf8ca1e19a0211591404d87c114a0460433db2fe23b2abf7384b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 17:33:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 17:33:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 17:33:39 GMT
EXPOSE 80
# Fri, 24 Apr 2020 17:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 17:33:40 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 17:33:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dbc48c2837a07f77334f15fed847d0310fbf620c555a33eed7a3e26b51948a87`  
		Last Modified: Fri, 24 Apr 2020 17:34:29 GMT  
		Size: 21.1 MB (21119551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6175123f5656afbcf94fb6f762724b1bd3f696ffeca9ca234c34f9ec1d6dfab`  
		Last Modified: Fri, 24 Apr 2020 17:34:25 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:58b5d2f623c63053b8a85c6b67a9a5d0f8d17b50fd43968eb064bc67739cf333
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22912220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6f782ec08f75c4c408f12f558daea37bf0136ac981565293da732a7ff753d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 12:14:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 12:15:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 12:15:00 GMT
EXPOSE 80
# Fri, 24 Apr 2020 12:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 12:15:02 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 12:15:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f2f2951777aa5ad9aa3787e0b88d017c3f2205f82636987318f26d9c14f7d494`  
		Last Modified: Fri, 24 Apr 2020 12:44:13 GMT  
		Size: 19.5 MB (19491370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde6fde915691a2d658b0bd77609f98105e33b8eab269515e05581ff4f7adaa4`  
		Last Modified: Fri, 24 Apr 2020 12:44:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eacafda7d2c278b363ac872f55010732694353005e2389acfc1ceb44075077e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:0a029fd9eed33b845a5e3310794a460ae84a181134d3907530d5ee1400471b67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319804976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548b1fbad1894614c6e1de2087dee68ef22dd882da81ae09c1289fe1a083a5a3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:43:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 10 Jun 2020 20:43:24 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:43:25 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:43:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59faa3247876c4be4c372d08763d6345d911c5aa3b1ba2fa4871e56b76458e`  
		Last Modified: Wed, 10 Jun 2020 20:44:33 GMT  
		Size: 25.9 MB (25886159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9281fc9a05026ec10cec5645e56b5a45e1009e632db41372276dde862cd65ef`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206aa039341a413a8754154d6b3f40205f7afad3021409a9f2c30726520b62fa`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f5428df4a8b754cead9e80fa6879d695a0a8ce92c161e9dd88e811d56a9251`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:picodon`

**does not exist** (yet?)

## `traefik:picodon-windowsservercore-1809`

**does not exist** (yet?)

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

## `traefik:v1.7.25`

**does not exist** (yet?)

## `traefik:v1.7.25-alpine`

**does not exist** (yet?)

## `traefik:v1.7.25-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:d1fa651db4263209a207b221bcdeef6d1e969e40322c732666ebde42ae575dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:b577b9f4080e4ef05bee4f07f5d9aee2ae633a0a9625ccfb259a91a51496e3ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cf7f226483cf8ca1e19a0211591404d87c114a0460433db2fe23b2abf7384b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 17:33:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 17:33:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 17:33:39 GMT
EXPOSE 80
# Fri, 24 Apr 2020 17:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 17:33:40 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 17:33:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dbc48c2837a07f77334f15fed847d0310fbf620c555a33eed7a3e26b51948a87`  
		Last Modified: Fri, 24 Apr 2020 17:34:29 GMT  
		Size: 21.1 MB (21119551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6175123f5656afbcf94fb6f762724b1bd3f696ffeca9ca234c34f9ec1d6dfab`  
		Last Modified: Fri, 24 Apr 2020 17:34:25 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:58b5d2f623c63053b8a85c6b67a9a5d0f8d17b50fd43968eb064bc67739cf333
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22912220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6f782ec08f75c4c408f12f558daea37bf0136ac981565293da732a7ff753d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 24 Apr 2020 12:14:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 24 Apr 2020 12:15:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 24 Apr 2020 12:15:00 GMT
EXPOSE 80
# Fri, 24 Apr 2020 12:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 12:15:02 GMT
CMD ["traefik"]
# Fri, 24 Apr 2020 12:15:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f2f2951777aa5ad9aa3787e0b88d017c3f2205f82636987318f26d9c14f7d494`  
		Last Modified: Fri, 24 Apr 2020 12:44:13 GMT  
		Size: 19.5 MB (19491370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde6fde915691a2d658b0bd77609f98105e33b8eab269515e05581ff4f7adaa4`  
		Last Modified: Fri, 24 Apr 2020 12:44:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eacafda7d2c278b363ac872f55010732694353005e2389acfc1ceb44075077e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:0a029fd9eed33b845a5e3310794a460ae84a181134d3907530d5ee1400471b67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319804976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548b1fbad1894614c6e1de2087dee68ef22dd882da81ae09c1289fe1a083a5a3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:43:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.24/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 10 Jun 2020 20:43:24 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:43:25 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:43:26 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.24 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d59faa3247876c4be4c372d08763d6345d911c5aa3b1ba2fa4871e56b76458e`  
		Last Modified: Wed, 10 Jun 2020 20:44:33 GMT  
		Size: 25.9 MB (25886159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9281fc9a05026ec10cec5645e56b5a45e1009e632db41372276dde862cd65ef`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206aa039341a413a8754154d6b3f40205f7afad3021409a9f2c30726520b62fa`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f5428df4a8b754cead9e80fa6879d695a0a8ce92c161e9dd88e811d56a9251`  
		Last Modified: Wed, 10 Jun 2020 20:44:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.5`

```console
$ docker pull traefik@sha256:9e49ebc167440e6e0cb506ffe342c7fa61ed255a946a6d968122ae3a46012978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2.5` - linux; amd64

```console
$ docker pull traefik@sha256:77dc644c7c701e27750424a83af5c7e52105dd229922adcec65dec98b7008123
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25163851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb015db20553dd45a5b3eceb2045e7f4f943f6e69357143294ddfba7b22adc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:01:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:01:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:01:40 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:01:40 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:01:40 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:7037ca3ac554763c2864a5f5423699dde0df6d3e029602130a97b04156f7e46c`  
		Last Modified: Tue, 14 Jul 2020 04:01:53 GMT  
		Size: 21.7 MB (21656019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2369a894ee34fd0934aea9f37c5b4f24f9ac5cc1489cf082a6c4fff4c82749d`  
		Last Modified: Tue, 14 Jul 2020 04:01:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:603d646ce37684679684907467e9d96be8a0eae64f57095d2daed2ba35f2e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23659228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe892034196fad4559fa2f899a9e3703bf9f108d10c6ed084d380e8b33bd5d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:22:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:22:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:22:59 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:23:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:23:01 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:23:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bd6d8886bbe7ee1a95ea26ab3b8c5f8877bded3faffc88aa914b549b70b670e4`  
		Last Modified: Tue, 14 Jul 2020 04:23:21 GMT  
		Size: 20.3 MB (20340837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0887301a2ce228fd510cb7fb26321a4df68da285190c017ae84d6ecd12fbab`  
		Last Modified: Tue, 14 Jul 2020 04:23:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:849ce2b3103ddcb89e97bf5c25965ec060d079e39c8ae9f6c750813289f17db9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23418640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7eece475e447cdc9a438d8ab190233ae2443c3c249b457ae445918e3890efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Jul 2020 04:32:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Jul 2020 04:32:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Jul 2020 04:32:36 GMT
EXPOSE 80
# Tue, 14 Jul 2020 04:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Jul 2020 04:32:37 GMT
CMD ["traefik"]
# Tue, 14 Jul 2020 04:32:38 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a09c3f3693404973832851145d87a7cfd7038fdb6ebe7f41a9f1d4ecb120e248`  
		Last Modified: Tue, 14 Jul 2020 04:32:57 GMT  
		Size: 20.0 MB (19997790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b36ca36f6d60be8dcccf4e421254542bc8f414414d55fcb31d6f3eef9cb38b`  
		Last Modified: Tue, 14 Jul 2020 04:32:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:v2.2.5-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:v2.2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3`

**does not exist** (yet?)

## `traefik:v2.3.0-rc2`

**does not exist** (yet?)

## `traefik:v2.3.0-rc2-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:v2.3-windowsservercore-1809`

**does not exist** (yet?)

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:30ce49ddff8e974e13c8e48d51a6d5958cbb6f668794ed5f148e0fb8acacd64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:91a5bedffb34552d444e1b2142184b25ad8f007b5ff35938f6c853d9b9f8f654
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320333200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b19cd4c1c1822c1d20ad0ac34cb4cfa9b14b6e56800afbeeae50aae283f56`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jul 2020 02:59:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.5/traefik_v2.2.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jul 2020 02:59:43 GMT
EXPOSE 80
# Tue, 14 Jul 2020 02:59:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jul 2020 02:59:45 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e2f6c5068bce4ace2cd32c4ff2c07a3338b013be1feceb022b8d31426b854e`  
		Last Modified: Tue, 14 Jul 2020 03:00:34 GMT  
		Size: 26.4 MB (26414529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69362c6bdb94ac25bad51f862b64c41905b07ad5f628d55e9c6116a04a76e64e`  
		Last Modified: Tue, 14 Jul 2020 03:00:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfcd3e790c608a2ee40ce269a28fe848786bd4a67fc25567831ad9ac9b4d16`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459647495bba353e160a39cec2f6563459d3c243b3a46ac709ab4ce0fd4a0bb7`  
		Last Modified: Tue, 14 Jul 2020 03:00:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
