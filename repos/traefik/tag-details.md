<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.29`](#traefik1729)
-	[`traefik:1.7.29-alpine`](#traefik1729-alpine)
-	[`traefik:1.7.29-windowsservercore-1809`](#traefik1729-windowsservercore-1809)
-	[`traefik:2.4`](#traefik24)
-	[`traefik:2.4-windowsservercore-1809`](#traefik24-windowsservercore-1809)
-	[`traefik:2.4.8`](#traefik248)
-	[`traefik:2.4.8-windowsservercore-1809`](#traefik248-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:livarot`](#traefiklivarot)
-	[`traefik:livarot-windowsservercore-1809`](#traefiklivarot-windowsservercore-1809)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.29`](#traefikv1729)
-	[`traefik:v1.7.29-alpine`](#traefikv1729-alpine)
-	[`traefik:v1.7.29-windowsservercore-1809`](#traefikv1729-windowsservercore-1809)
-	[`traefik:v2.4`](#traefikv24)
-	[`traefik:v2.4-windowsservercore-1809`](#traefikv24-windowsservercore-1809)
-	[`traefik:v2.4.8`](#traefikv248)
-	[`traefik:v2.4.8-windowsservercore-1809`](#traefikv248-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:94c2b89f6667bca386b57fd572b048601445428447d724ee7c1272e30181c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3c057f09e959886ea9a31b610d62224d3397c982e5bc271e97ad7afde2e839dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21187529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1422bb98369138568f428c2dc8902f013ad0d5aa804024e34ce15370ed641252`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:21:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:21:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:21:30 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:21:30 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:21:30 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d27a0058cb738689b17633dbbafc3a09a9b6c19258cb08c2160b6b8389566`  
		Last Modified: Mon, 29 Mar 2021 20:22:07 GMT  
		Size: 17.7 MB (17697632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8698815445b8d9b9f28cbb616b4c814731a54ebd5ffa8dd7bef1a670b3d7f53`  
		Last Modified: Mon, 29 Mar 2021 20:22:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:09c15b6388be2b761a923b7d9c694c749593aea99ab535421b476bb8565b3e5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d09cafb85f6ee87bd05a47ebc48cc1f775dac7e4c6b31d25a8886f2ea2ae0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:04:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:04:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:04:31 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:04:32 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:04:33 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b267a61f2fe2efe3a182df5f6d260b3a6301ae8cb20c3bfebdeb55c4906edf`  
		Last Modified: Mon, 29 Mar 2021 20:07:35 GMT  
		Size: 16.5 MB (16517348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365ccc7815b33c58bf61ed670d5503002118e1c336678092f3aeeb32a64775e`  
		Last Modified: Mon, 29 Mar 2021 20:07:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6c8af591fd76d63e6ca5c222d5a29f55cae2b79c608d25a74b1eb84dfc22be65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19500238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03a47a11cf7e215dfcf630380031a09f7985bf27be0709627815e67dea785f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 19:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 19:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 19:43:55 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 19:43:56 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 19:43:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb0f53f3b7fe97ae8e0e647bc25bf37402ca812328bd459ce17ceca0401c15`  
		Last Modified: Mon, 29 Mar 2021 19:53:06 GMT  
		Size: 16.1 MB (16098458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412e008edc66153391ee9989d451e4be607c808124486b69248ba2f9c5de058`  
		Last Modified: Mon, 29 Mar 2021 19:53:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6eecb378641177fca09f19127265ab91271448ef60a5268ee68987276ccfe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:cf4582a473eb76ed41b990dfa297cc4d3bbd7f591095247d8d8594c00fbb78d4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0972d358793f50271670241e2fe9aec32fe3650e7d8910e0b096f62563a41e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Mar 2021 20:16:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 29 Mar 2021 20:16:26 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:16:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:16:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530c2cf8b93172ab27963511ee3d2f36f94cc25e63ec870d1d91d56e05dd9722`  
		Last Modified: Mon, 29 Mar 2021 20:17:16 GMT  
		Size: 27.4 MB (27397196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be393dbe8be8c7a56d7d6fe4c431c56dd54a387bb81f572283ee86e3015dcb51`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d019fc76e3913da39f4402716b57bfa0395c64227907a2eb2b81878148ff7`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d834588bef160f62373a77ce715af11b673c3e1673def36b2dcc290eb522870a`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.29`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.29` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.29-alpine`

```console
$ docker pull traefik@sha256:94c2b89f6667bca386b57fd572b048601445428447d724ee7c1272e30181c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.29-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3c057f09e959886ea9a31b610d62224d3397c982e5bc271e97ad7afde2e839dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21187529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1422bb98369138568f428c2dc8902f013ad0d5aa804024e34ce15370ed641252`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:21:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:21:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:21:30 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:21:30 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:21:30 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d27a0058cb738689b17633dbbafc3a09a9b6c19258cb08c2160b6b8389566`  
		Last Modified: Mon, 29 Mar 2021 20:22:07 GMT  
		Size: 17.7 MB (17697632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8698815445b8d9b9f28cbb616b4c814731a54ebd5ffa8dd7bef1a670b3d7f53`  
		Last Modified: Mon, 29 Mar 2021 20:22:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.29-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:09c15b6388be2b761a923b7d9c694c749593aea99ab535421b476bb8565b3e5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d09cafb85f6ee87bd05a47ebc48cc1f775dac7e4c6b31d25a8886f2ea2ae0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:04:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:04:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:04:31 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:04:32 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:04:33 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b267a61f2fe2efe3a182df5f6d260b3a6301ae8cb20c3bfebdeb55c4906edf`  
		Last Modified: Mon, 29 Mar 2021 20:07:35 GMT  
		Size: 16.5 MB (16517348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365ccc7815b33c58bf61ed670d5503002118e1c336678092f3aeeb32a64775e`  
		Last Modified: Mon, 29 Mar 2021 20:07:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.29-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6c8af591fd76d63e6ca5c222d5a29f55cae2b79c608d25a74b1eb84dfc22be65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19500238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03a47a11cf7e215dfcf630380031a09f7985bf27be0709627815e67dea785f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 19:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 19:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 19:43:55 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 19:43:56 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 19:43:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb0f53f3b7fe97ae8e0e647bc25bf37402ca812328bd459ce17ceca0401c15`  
		Last Modified: Mon, 29 Mar 2021 19:53:06 GMT  
		Size: 16.1 MB (16098458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412e008edc66153391ee9989d451e4be607c808124486b69248ba2f9c5de058`  
		Last Modified: Mon, 29 Mar 2021 19:53:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.29-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6eecb378641177fca09f19127265ab91271448ef60a5268ee68987276ccfe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:1.7.29-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:cf4582a473eb76ed41b990dfa297cc4d3bbd7f591095247d8d8594c00fbb78d4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0972d358793f50271670241e2fe9aec32fe3650e7d8910e0b096f62563a41e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Mar 2021 20:16:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 29 Mar 2021 20:16:26 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:16:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:16:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530c2cf8b93172ab27963511ee3d2f36f94cc25e63ec870d1d91d56e05dd9722`  
		Last Modified: Mon, 29 Mar 2021 20:17:16 GMT  
		Size: 27.4 MB (27397196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be393dbe8be8c7a56d7d6fe4c431c56dd54a387bb81f572283ee86e3015dcb51`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d019fc76e3913da39f4402716b57bfa0395c64227907a2eb2b81878148ff7`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d834588bef160f62373a77ce715af11b673c3e1673def36b2dcc290eb522870a`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:2.4-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.8`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4.8` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:2.4.8-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:livarot` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot-windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:livarot-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:94c2b89f6667bca386b57fd572b048601445428447d724ee7c1272e30181c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3c057f09e959886ea9a31b610d62224d3397c982e5bc271e97ad7afde2e839dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21187529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1422bb98369138568f428c2dc8902f013ad0d5aa804024e34ce15370ed641252`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:21:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:21:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:21:30 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:21:30 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:21:30 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d27a0058cb738689b17633dbbafc3a09a9b6c19258cb08c2160b6b8389566`  
		Last Modified: Mon, 29 Mar 2021 20:22:07 GMT  
		Size: 17.7 MB (17697632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8698815445b8d9b9f28cbb616b4c814731a54ebd5ffa8dd7bef1a670b3d7f53`  
		Last Modified: Mon, 29 Mar 2021 20:22:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:09c15b6388be2b761a923b7d9c694c749593aea99ab535421b476bb8565b3e5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d09cafb85f6ee87bd05a47ebc48cc1f775dac7e4c6b31d25a8886f2ea2ae0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:04:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:04:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:04:31 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:04:32 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:04:33 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b267a61f2fe2efe3a182df5f6d260b3a6301ae8cb20c3bfebdeb55c4906edf`  
		Last Modified: Mon, 29 Mar 2021 20:07:35 GMT  
		Size: 16.5 MB (16517348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365ccc7815b33c58bf61ed670d5503002118e1c336678092f3aeeb32a64775e`  
		Last Modified: Mon, 29 Mar 2021 20:07:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6c8af591fd76d63e6ca5c222d5a29f55cae2b79c608d25a74b1eb84dfc22be65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19500238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03a47a11cf7e215dfcf630380031a09f7985bf27be0709627815e67dea785f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 19:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 19:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 19:43:55 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 19:43:56 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 19:43:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb0f53f3b7fe97ae8e0e647bc25bf37402ca812328bd459ce17ceca0401c15`  
		Last Modified: Mon, 29 Mar 2021 19:53:06 GMT  
		Size: 16.1 MB (16098458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412e008edc66153391ee9989d451e4be607c808124486b69248ba2f9c5de058`  
		Last Modified: Mon, 29 Mar 2021 19:53:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6eecb378641177fca09f19127265ab91271448ef60a5268ee68987276ccfe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:cf4582a473eb76ed41b990dfa297cc4d3bbd7f591095247d8d8594c00fbb78d4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0972d358793f50271670241e2fe9aec32fe3650e7d8910e0b096f62563a41e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Mar 2021 20:16:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 29 Mar 2021 20:16:26 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:16:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:16:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530c2cf8b93172ab27963511ee3d2f36f94cc25e63ec870d1d91d56e05dd9722`  
		Last Modified: Mon, 29 Mar 2021 20:17:16 GMT  
		Size: 27.4 MB (27397196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be393dbe8be8c7a56d7d6fe4c431c56dd54a387bb81f572283ee86e3015dcb51`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d019fc76e3913da39f4402716b57bfa0395c64227907a2eb2b81878148ff7`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d834588bef160f62373a77ce715af11b673c3e1673def36b2dcc290eb522870a`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:94c2b89f6667bca386b57fd572b048601445428447d724ee7c1272e30181c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3c057f09e959886ea9a31b610d62224d3397c982e5bc271e97ad7afde2e839dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21187529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1422bb98369138568f428c2dc8902f013ad0d5aa804024e34ce15370ed641252`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:21:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:21:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:21:30 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:21:30 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:21:30 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d27a0058cb738689b17633dbbafc3a09a9b6c19258cb08c2160b6b8389566`  
		Last Modified: Mon, 29 Mar 2021 20:22:07 GMT  
		Size: 17.7 MB (17697632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8698815445b8d9b9f28cbb616b4c814731a54ebd5ffa8dd7bef1a670b3d7f53`  
		Last Modified: Mon, 29 Mar 2021 20:22:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:09c15b6388be2b761a923b7d9c694c749593aea99ab535421b476bb8565b3e5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d09cafb85f6ee87bd05a47ebc48cc1f775dac7e4c6b31d25a8886f2ea2ae0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:04:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:04:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:04:31 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:04:32 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:04:33 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b267a61f2fe2efe3a182df5f6d260b3a6301ae8cb20c3bfebdeb55c4906edf`  
		Last Modified: Mon, 29 Mar 2021 20:07:35 GMT  
		Size: 16.5 MB (16517348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365ccc7815b33c58bf61ed670d5503002118e1c336678092f3aeeb32a64775e`  
		Last Modified: Mon, 29 Mar 2021 20:07:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6c8af591fd76d63e6ca5c222d5a29f55cae2b79c608d25a74b1eb84dfc22be65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19500238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03a47a11cf7e215dfcf630380031a09f7985bf27be0709627815e67dea785f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 19:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 19:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 19:43:55 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 19:43:56 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 19:43:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb0f53f3b7fe97ae8e0e647bc25bf37402ca812328bd459ce17ceca0401c15`  
		Last Modified: Mon, 29 Mar 2021 19:53:06 GMT  
		Size: 16.1 MB (16098458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412e008edc66153391ee9989d451e4be607c808124486b69248ba2f9c5de058`  
		Last Modified: Mon, 29 Mar 2021 19:53:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6eecb378641177fca09f19127265ab91271448ef60a5268ee68987276ccfe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:cf4582a473eb76ed41b990dfa297cc4d3bbd7f591095247d8d8594c00fbb78d4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0972d358793f50271670241e2fe9aec32fe3650e7d8910e0b096f62563a41e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Mar 2021 20:16:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 29 Mar 2021 20:16:26 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:16:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:16:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530c2cf8b93172ab27963511ee3d2f36f94cc25e63ec870d1d91d56e05dd9722`  
		Last Modified: Mon, 29 Mar 2021 20:17:16 GMT  
		Size: 27.4 MB (27397196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be393dbe8be8c7a56d7d6fe4c431c56dd54a387bb81f572283ee86e3015dcb51`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d019fc76e3913da39f4402716b57bfa0395c64227907a2eb2b81878148ff7`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d834588bef160f62373a77ce715af11b673c3e1673def36b2dcc290eb522870a`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.29`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.29` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.29-alpine`

```console
$ docker pull traefik@sha256:94c2b89f6667bca386b57fd572b048601445428447d724ee7c1272e30181c6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.29-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:3c057f09e959886ea9a31b610d62224d3397c982e5bc271e97ad7afde2e839dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21187529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1422bb98369138568f428c2dc8902f013ad0d5aa804024e34ce15370ed641252`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:21:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:21:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:21:30 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:21:30 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:21:30 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d27a0058cb738689b17633dbbafc3a09a9b6c19258cb08c2160b6b8389566`  
		Last Modified: Mon, 29 Mar 2021 20:22:07 GMT  
		Size: 17.7 MB (17697632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8698815445b8d9b9f28cbb616b4c814731a54ebd5ffa8dd7bef1a670b3d7f53`  
		Last Modified: Mon, 29 Mar 2021 20:22:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.29-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:09c15b6388be2b761a923b7d9c694c749593aea99ab535421b476bb8565b3e5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d09cafb85f6ee87bd05a47ebc48cc1f775dac7e4c6b31d25a8886f2ea2ae0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 20:04:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 20:04:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 20:04:31 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 20:04:32 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 20:04:33 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b267a61f2fe2efe3a182df5f6d260b3a6301ae8cb20c3bfebdeb55c4906edf`  
		Last Modified: Mon, 29 Mar 2021 20:07:35 GMT  
		Size: 16.5 MB (16517348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365ccc7815b33c58bf61ed670d5503002118e1c336678092f3aeeb32a64775e`  
		Last Modified: Mon, 29 Mar 2021 20:07:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.29-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6c8af591fd76d63e6ca5c222d5a29f55cae2b79c608d25a74b1eb84dfc22be65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19500238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03a47a11cf7e215dfcf630380031a09f7985bf27be0709627815e67dea785f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 29 Mar 2021 19:43:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 29 Mar 2021 19:43:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 29 Mar 2021 19:43:55 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:43:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Mar 2021 19:43:56 GMT
CMD ["traefik"]
# Mon, 29 Mar 2021 19:43:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb0f53f3b7fe97ae8e0e647bc25bf37402ca812328bd459ce17ceca0401c15`  
		Last Modified: Mon, 29 Mar 2021 19:53:06 GMT  
		Size: 16.1 MB (16098458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412e008edc66153391ee9989d451e4be607c808124486b69248ba2f9c5de058`  
		Last Modified: Mon, 29 Mar 2021 19:53:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.29-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6eecb378641177fca09f19127265ab91271448ef60a5268ee68987276ccfe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:v1.7.29-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:cf4582a473eb76ed41b990dfa297cc4d3bbd7f591095247d8d8594c00fbb78d4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0972d358793f50271670241e2fe9aec32fe3650e7d8910e0b096f62563a41e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Mar 2021 20:16:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.29/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 29 Mar 2021 20:16:26 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:16:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:16:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530c2cf8b93172ab27963511ee3d2f36f94cc25e63ec870d1d91d56e05dd9722`  
		Last Modified: Mon, 29 Mar 2021 20:17:16 GMT  
		Size: 27.4 MB (27397196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be393dbe8be8c7a56d7d6fe4c431c56dd54a387bb81f572283ee86e3015dcb51`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d019fc76e3913da39f4402716b57bfa0395c64227907a2eb2b81878148ff7`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d834588bef160f62373a77ce715af11b673c3e1673def36b2dcc290eb522870a`  
		Last Modified: Mon, 29 Mar 2021 20:17:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:v2.4-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.8`

```console
$ docker pull traefik@sha256:2781953cc6d6445ec49ac487bc7d94f512ac4e413ca73611be36d63ceda42751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4.8` - linux; amd64

```console
$ docker pull traefik@sha256:297a4433372208769fb51168387ba56c048aa44113d4151be25e65dc158f916e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286716bfc172eecb6c7ed89847c944e0b0fed67fae2aba67fff284f6067df72c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:42:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 09:43:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 09:43:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 09:43:03 GMT
EXPOSE 80
# Fri, 26 Mar 2021 09:43:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 09:43:04 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 09:43:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f381c65aaaa0ed2d90609a1d94ca65fa057410a866389f0a380395c0f30dad9`  
		Last Modified: Fri, 26 Mar 2021 09:43:39 GMT  
		Size: 674.2 KB (674197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52a6f52c94839cba99c68125ffa1f8b521d969568b40f44ab87c7a2c0bd0876`  
		Last Modified: Fri, 26 Mar 2021 09:43:43 GMT  
		Size: 24.3 MB (24337518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb70c84da2b1068118347f8ae35e9bfa59c54684e205a6ef3159986776fc9f1`  
		Last Modified: Fri, 26 Mar 2021 09:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f5dafd50b571ddc6c6b8a9115fd2c8a4c5d84e09ae7db01625792506d980857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26025821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754212e4b35fda67d7a32a946ebd55e9a660513f12aca82a22c57bba32781b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 10:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 10:24:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 10:24:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 10:24:13 GMT
EXPOSE 80
# Fri, 26 Mar 2021 10:24:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 10:24:14 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 10:24:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7337eab7080efd44e620f96e74185d0ffeacba100c69045459249b2d3a3dd3`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 677.0 KB (677007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081d5433014b8e5186e1a9d24a8e4a4c298bb5d5f570b7677d84f77c76560541`  
		Last Modified: Fri, 26 Mar 2021 10:25:16 GMT  
		Size: 22.7 MB (22727118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e75eb7078a4331e9b051b8d5d92b8882769d692d7505a70754de8357dc195a9`  
		Last Modified: Fri, 26 Mar 2021 10:25:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:9bb3516baf888fa5c81008c445ff63804f556ff68fee752a8c17fc8a8150db78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25475525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1089720f9d91464f0161c603353bab15f2014e49e5228e134abae8bb3812600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:08:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 26 Mar 2021 08:08:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 26 Mar 2021 08:08:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 26 Mar 2021 08:08:09 GMT
EXPOSE 80
# Fri, 26 Mar 2021 08:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 08:08:11 GMT
CMD ["traefik"]
# Fri, 26 Mar 2021 08:08:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b107397c029a94008575072c0901eae0ac7977a9fe1fa05ed8e45757387f3be`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 675.5 KB (675534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf36803d5e7ca9b3042d1847d12ee10baacbcf8e84b0aad89b7d9267714e29`  
		Last Modified: Fri, 26 Mar 2021 08:11:47 GMT  
		Size: 22.1 MB (22073745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95742e6b158cadc348dddbb20aa9c7461bfe1441a1f5f3171117ac99538428`  
		Last Modified: Fri, 26 Mar 2021 08:11:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:v2.4.8-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:37b2b7f435939b597589efb591686eca5a0e6ae850d1c80ec0cb3f996c05d24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull traefik@sha256:9345ce86759b6cc6053762a836111a43408fa15fc5571fba77ea93b43deefa00
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495650153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005e85992474d2eb3b06c7502a58d38c633edde288a548518128cd3e938f79c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Mar 2021 01:16:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 24 Mar 2021 01:16:19 GMT
EXPOSE 80
# Wed, 24 Mar 2021 01:16:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 24 Mar 2021 01:16:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138871c226c89b2e75588935069c544f0c8ce5f68930fab95af0e4ca5a825d73`  
		Last Modified: Wed, 24 Mar 2021 01:17:09 GMT  
		Size: 34.1 MB (34109955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8574b4de7673b299ad666f81cd495bcfac5bf87fb33d4ef2781bdfcef30267`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb49e94abf40397ca09c966a1b4beb9579a20cb39ca8c9e17299ff206eb038e`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d3f9210f45b7cb7f4c1ea77897d4576fcff778e51504d060afb3b28f4ae94`  
		Last Modified: Wed, 24 Mar 2021 01:16:56 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
