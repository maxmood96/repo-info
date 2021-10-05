<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.31`](#traefik1731)
-	[`traefik:1.7.31-alpine`](#traefik1731-alpine)
-	[`traefik:1.7.31-windowsservercore-1809`](#traefik1731-windowsservercore-1809)
-	[`traefik:2.5`](#traefik25)
-	[`traefik:2.5-windowsservercore-1809`](#traefik25-windowsservercore-1809)
-	[`traefik:2.5.3`](#traefik253)
-	[`traefik:2.5.3-windowsservercore-1809`](#traefik253-windowsservercore-1809)
-	[`traefik:brie`](#traefikbrie)
-	[`traefik:brie-windowsservercore-1809`](#traefikbrie-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.31`](#traefikv1731)
-	[`traefik:v1.7.31-alpine`](#traefikv1731-alpine)
-	[`traefik:v1.7.31-windowsservercore-1809`](#traefikv1731-windowsservercore-1809)
-	[`traefik:v2.5`](#traefikv25)
-	[`traefik:v2.5-windowsservercore-1809`](#traefikv25-windowsservercore-1809)
-	[`traefik:v2.5.3`](#traefikv253)
-	[`traefik:v2.5.3-windowsservercore-1809`](#traefikv253-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:17ec589ebb0d75bbe61742911e5dec1a68d9957d7c48038a5a0a358c735d599a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:298922381e42974e1474ade0b532961b2edc760d3774b4456222817d1e8e384c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201a05093074172e604f0dc53b6dc3648e95fec6610d36f49f6aa02602662d5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 05 Oct 2021 00:02:44 GMT
COPY file:10848119ebd67ebb26ec33871e75e75b528afb4dffb89e242f4feca4019c3093 in / 
# Tue, 05 Oct 2021 00:02:45 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:46 GMT
VOLUME [/tmp]
# Tue, 05 Oct 2021 00:02:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:02:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada4a68136f6bd05b10da7bee212076d31c246cdcb1242cce64b1ef67c0d573`  
		Last Modified: Tue, 05 Oct 2021 00:05:09 GMT  
		Size: 20.0 MB (19979857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:36d54f6bf40b7deae0d97bc613093565077a1a31b9aa58667c80a6e91121343d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4423c30793a781d7f5cbb6dfb62ab5085f97914b59a3bbd4fbd1c34c2bdee1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY file:2afc08f94cbfa383acddc913141df64725fc71831a54c44b71019f36df84364c in / 
# Mon, 04 Oct 2021 23:44:24 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:24 GMT
VOLUME [/tmp]
# Mon, 04 Oct 2021 23:44:24 GMT
ENTRYPOINT ["/traefik"]
# Mon, 04 Oct 2021 23:44:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef9a8ab3b3f0f0e34c3c4acb9c07beca418533bcb7ef100f0aa56a951fc9e9`  
		Last Modified: Mon, 04 Oct 2021 23:45:39 GMT  
		Size: 19.5 MB (19518068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:6b832fb0bc93489b0aafbf3aabecb0c2c5288cf7118673e80b90eda1d28410eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:81038c31f0c7151418b10af58c252fb5e4d76c11a3d0b7a22aa66d61c3aadadc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21176792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d154c84159a4d96e8aedebfa3bce9d19fc139b450d3b4eee1bb46e4ab759a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:15:05 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 01 Sep 2021 06:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 01 Sep 2021 06:15:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 01 Sep 2021 06:15:16 GMT
EXPOSE 80
# Wed, 01 Sep 2021 06:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 06:15:17 GMT
CMD ["traefik"]
# Wed, 01 Sep 2021 06:15:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f794cbdc99470251c9539251dc8a5aba6a6f0d6b4fd07a519bf8d13a9d42bbec`  
		Last Modified: Wed, 01 Sep 2021 06:16:08 GMT  
		Size: 674.2 KB (674226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa68ae87a84c1bc651faa725d25b0c37abf9514b31398de8ec4113c983f7bd3c`  
		Last Modified: Wed, 01 Sep 2021 06:16:31 GMT  
		Size: 17.7 MB (17684891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6a80456e69fce8cd53394e12769c6b2757b1a318d8abd6eb0b1aa982e6791`  
		Last Modified: Wed, 01 Sep 2021 06:16:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f39845bff770219bdd5a8b6f84f21ee4b39134fad4a31e8a4a3c54f0cd8056f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6b253765bd18d5a529ad3c93327f907ab6c712f669a762c9806bb81dde006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Oct 2021 00:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Oct 2021 00:02:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Oct 2021 00:02:16 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:02:17 GMT
CMD ["traefik"]
# Tue, 05 Oct 2021 00:02:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d5f55b31f41aaac3372273955177ca7870585cbb870360b3d7dbf89f51266`  
		Last Modified: Tue, 05 Oct 2021 00:04:31 GMT  
		Size: 20.0 MB (19979916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e01da9fa02909dac56cbefbb8369298874c7eec6ffab823508744daa3900f5`  
		Last Modified: Tue, 05 Oct 2021 00:04:18 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2e12de8167c672b01390f08925e4d0c2358c030ba695c1056352ae3281d8505a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cdbea4a019b387ed0bcaa01580751374c1af2813d9561495c41b37f24d1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 04 Oct 2021 23:44:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 04 Oct 2021 23:44:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 04 Oct 2021 23:44:10 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Oct 2021 23:44:10 GMT
CMD ["traefik"]
# Mon, 04 Oct 2021 23:44:10 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bab87e61952bc1950c49311bd75a7fb2e2ea736191294f0eb6ff24c9bf0e3`  
		Last Modified: Mon, 04 Oct 2021 23:45:16 GMT  
		Size: 19.5 MB (19518028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd6503819a6bef01ca23b02b60ce103975ea1f188a9d8d025c3a29021dee79`  
		Last Modified: Mon, 04 Oct 2021 23:45:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1ec8a6971ea515c6e938ae4ef038d946e607c413f4a7793cb59e3fec70902d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:ab0698c8ee0db93af08da62353c6b314612343b2a9c7d9137d49ccbce9dc047e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708923892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff742be7b268a7e38f0f67b6f834a0650c65df642cb307e59b296bcf0c74ead6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 00:15:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 05 Oct 2021 00:15:22 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:15:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:15:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692bfe71d7ec563f28ecbd54c7b1ebc2c2c1cb8d54506cc7087afda6f8e9578`  
		Last Modified: Tue, 05 Oct 2021 00:16:01 GMT  
		Size: 22.2 MB (22220356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65addfc2b54f8fc5d623cb7bbfa9d8cb6c188caf2794d8f65ef04a635244c5e0`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1f22da3fdedf199c0ccfab0c55245e26e428715a6cfd70ac796d642970e56`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15bb35f7823dc2b058fe3fa77757b9f3dd32ed8c9340d960bd80261d3a3f23`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.31`

```console
$ docker pull traefik@sha256:536377b698b5caf61175360fe1f8af8c5641351a9f3319c5a094b890c540f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:298922381e42974e1474ade0b532961b2edc760d3774b4456222817d1e8e384c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201a05093074172e604f0dc53b6dc3648e95fec6610d36f49f6aa02602662d5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 05 Oct 2021 00:02:44 GMT
COPY file:10848119ebd67ebb26ec33871e75e75b528afb4dffb89e242f4feca4019c3093 in / 
# Tue, 05 Oct 2021 00:02:45 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:46 GMT
VOLUME [/tmp]
# Tue, 05 Oct 2021 00:02:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:02:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada4a68136f6bd05b10da7bee212076d31c246cdcb1242cce64b1ef67c0d573`  
		Last Modified: Tue, 05 Oct 2021 00:05:09 GMT  
		Size: 20.0 MB (19979857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:36d54f6bf40b7deae0d97bc613093565077a1a31b9aa58667c80a6e91121343d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4423c30793a781d7f5cbb6dfb62ab5085f97914b59a3bbd4fbd1c34c2bdee1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY file:2afc08f94cbfa383acddc913141df64725fc71831a54c44b71019f36df84364c in / 
# Mon, 04 Oct 2021 23:44:24 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:24 GMT
VOLUME [/tmp]
# Mon, 04 Oct 2021 23:44:24 GMT
ENTRYPOINT ["/traefik"]
# Mon, 04 Oct 2021 23:44:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef9a8ab3b3f0f0e34c3c4acb9c07beca418533bcb7ef100f0aa56a951fc9e9`  
		Last Modified: Mon, 04 Oct 2021 23:45:39 GMT  
		Size: 19.5 MB (19518068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.31-alpine`

```console
$ docker pull traefik@sha256:1824ec8b26cd6a410048018a93ce93c2fe0e10e7d21f92e5610efe96814c6dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.31-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f39845bff770219bdd5a8b6f84f21ee4b39134fad4a31e8a4a3c54f0cd8056f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6b253765bd18d5a529ad3c93327f907ab6c712f669a762c9806bb81dde006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Oct 2021 00:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Oct 2021 00:02:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Oct 2021 00:02:16 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:02:17 GMT
CMD ["traefik"]
# Tue, 05 Oct 2021 00:02:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d5f55b31f41aaac3372273955177ca7870585cbb870360b3d7dbf89f51266`  
		Last Modified: Tue, 05 Oct 2021 00:04:31 GMT  
		Size: 20.0 MB (19979916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e01da9fa02909dac56cbefbb8369298874c7eec6ffab823508744daa3900f5`  
		Last Modified: Tue, 05 Oct 2021 00:04:18 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.31-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2e12de8167c672b01390f08925e4d0c2358c030ba695c1056352ae3281d8505a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cdbea4a019b387ed0bcaa01580751374c1af2813d9561495c41b37f24d1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 04 Oct 2021 23:44:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 04 Oct 2021 23:44:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 04 Oct 2021 23:44:10 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Oct 2021 23:44:10 GMT
CMD ["traefik"]
# Mon, 04 Oct 2021 23:44:10 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bab87e61952bc1950c49311bd75a7fb2e2ea736191294f0eb6ff24c9bf0e3`  
		Last Modified: Mon, 04 Oct 2021 23:45:16 GMT  
		Size: 19.5 MB (19518028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd6503819a6bef01ca23b02b60ce103975ea1f188a9d8d025c3a29021dee79`  
		Last Modified: Mon, 04 Oct 2021 23:45:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.31-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1ec8a6971ea515c6e938ae4ef038d946e607c413f4a7793cb59e3fec70902d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:1.7.31-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:ab0698c8ee0db93af08da62353c6b314612343b2a9c7d9137d49ccbce9dc047e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708923892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff742be7b268a7e38f0f67b6f834a0650c65df642cb307e59b296bcf0c74ead6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 00:15:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 05 Oct 2021 00:15:22 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:15:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:15:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692bfe71d7ec563f28ecbd54c7b1ebc2c2c1cb8d54506cc7087afda6f8e9578`  
		Last Modified: Tue, 05 Oct 2021 00:16:01 GMT  
		Size: 22.2 MB (22220356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65addfc2b54f8fc5d623cb7bbfa9d8cb6c188caf2794d8f65ef04a635244c5e0`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1f22da3fdedf199c0ccfab0c55245e26e428715a6cfd70ac796d642970e56`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15bb35f7823dc2b058fe3fa77757b9f3dd32ed8c9340d960bd80261d3a3f23`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:2.5-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.3`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:2.5.3-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:brie` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:brie-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:17ec589ebb0d75bbe61742911e5dec1a68d9957d7c48038a5a0a358c735d599a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:298922381e42974e1474ade0b532961b2edc760d3774b4456222817d1e8e384c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201a05093074172e604f0dc53b6dc3648e95fec6610d36f49f6aa02602662d5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 05 Oct 2021 00:02:44 GMT
COPY file:10848119ebd67ebb26ec33871e75e75b528afb4dffb89e242f4feca4019c3093 in / 
# Tue, 05 Oct 2021 00:02:45 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:46 GMT
VOLUME [/tmp]
# Tue, 05 Oct 2021 00:02:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:02:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada4a68136f6bd05b10da7bee212076d31c246cdcb1242cce64b1ef67c0d573`  
		Last Modified: Tue, 05 Oct 2021 00:05:09 GMT  
		Size: 20.0 MB (19979857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:36d54f6bf40b7deae0d97bc613093565077a1a31b9aa58667c80a6e91121343d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4423c30793a781d7f5cbb6dfb62ab5085f97914b59a3bbd4fbd1c34c2bdee1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY file:2afc08f94cbfa383acddc913141df64725fc71831a54c44b71019f36df84364c in / 
# Mon, 04 Oct 2021 23:44:24 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:24 GMT
VOLUME [/tmp]
# Mon, 04 Oct 2021 23:44:24 GMT
ENTRYPOINT ["/traefik"]
# Mon, 04 Oct 2021 23:44:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef9a8ab3b3f0f0e34c3c4acb9c07beca418533bcb7ef100f0aa56a951fc9e9`  
		Last Modified: Mon, 04 Oct 2021 23:45:39 GMT  
		Size: 19.5 MB (19518068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:6b832fb0bc93489b0aafbf3aabecb0c2c5288cf7118673e80b90eda1d28410eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:81038c31f0c7151418b10af58c252fb5e4d76c11a3d0b7a22aa66d61c3aadadc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21176792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d154c84159a4d96e8aedebfa3bce9d19fc139b450d3b4eee1bb46e4ab759a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:15:05 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 01 Sep 2021 06:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 01 Sep 2021 06:15:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 01 Sep 2021 06:15:16 GMT
EXPOSE 80
# Wed, 01 Sep 2021 06:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 06:15:17 GMT
CMD ["traefik"]
# Wed, 01 Sep 2021 06:15:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f794cbdc99470251c9539251dc8a5aba6a6f0d6b4fd07a519bf8d13a9d42bbec`  
		Last Modified: Wed, 01 Sep 2021 06:16:08 GMT  
		Size: 674.2 KB (674226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa68ae87a84c1bc651faa725d25b0c37abf9514b31398de8ec4113c983f7bd3c`  
		Last Modified: Wed, 01 Sep 2021 06:16:31 GMT  
		Size: 17.7 MB (17684891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6a80456e69fce8cd53394e12769c6b2757b1a318d8abd6eb0b1aa982e6791`  
		Last Modified: Wed, 01 Sep 2021 06:16:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f39845bff770219bdd5a8b6f84f21ee4b39134fad4a31e8a4a3c54f0cd8056f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6b253765bd18d5a529ad3c93327f907ab6c712f669a762c9806bb81dde006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Oct 2021 00:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Oct 2021 00:02:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Oct 2021 00:02:16 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:02:17 GMT
CMD ["traefik"]
# Tue, 05 Oct 2021 00:02:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d5f55b31f41aaac3372273955177ca7870585cbb870360b3d7dbf89f51266`  
		Last Modified: Tue, 05 Oct 2021 00:04:31 GMT  
		Size: 20.0 MB (19979916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e01da9fa02909dac56cbefbb8369298874c7eec6ffab823508744daa3900f5`  
		Last Modified: Tue, 05 Oct 2021 00:04:18 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2e12de8167c672b01390f08925e4d0c2358c030ba695c1056352ae3281d8505a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cdbea4a019b387ed0bcaa01580751374c1af2813d9561495c41b37f24d1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 04 Oct 2021 23:44:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 04 Oct 2021 23:44:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 04 Oct 2021 23:44:10 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Oct 2021 23:44:10 GMT
CMD ["traefik"]
# Mon, 04 Oct 2021 23:44:10 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bab87e61952bc1950c49311bd75a7fb2e2ea736191294f0eb6ff24c9bf0e3`  
		Last Modified: Mon, 04 Oct 2021 23:45:16 GMT  
		Size: 19.5 MB (19518028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd6503819a6bef01ca23b02b60ce103975ea1f188a9d8d025c3a29021dee79`  
		Last Modified: Mon, 04 Oct 2021 23:45:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1ec8a6971ea515c6e938ae4ef038d946e607c413f4a7793cb59e3fec70902d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:ab0698c8ee0db93af08da62353c6b314612343b2a9c7d9137d49ccbce9dc047e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708923892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff742be7b268a7e38f0f67b6f834a0650c65df642cb307e59b296bcf0c74ead6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 00:15:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 05 Oct 2021 00:15:22 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:15:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:15:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692bfe71d7ec563f28ecbd54c7b1ebc2c2c1cb8d54506cc7087afda6f8e9578`  
		Last Modified: Tue, 05 Oct 2021 00:16:01 GMT  
		Size: 22.2 MB (22220356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65addfc2b54f8fc5d623cb7bbfa9d8cb6c188caf2794d8f65ef04a635244c5e0`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1f22da3fdedf199c0ccfab0c55245e26e428715a6cfd70ac796d642970e56`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15bb35f7823dc2b058fe3fa77757b9f3dd32ed8c9340d960bd80261d3a3f23`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:17ec589ebb0d75bbe61742911e5dec1a68d9957d7c48038a5a0a358c735d599a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:298922381e42974e1474ade0b532961b2edc760d3774b4456222817d1e8e384c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201a05093074172e604f0dc53b6dc3648e95fec6610d36f49f6aa02602662d5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 05 Oct 2021 00:02:44 GMT
COPY file:10848119ebd67ebb26ec33871e75e75b528afb4dffb89e242f4feca4019c3093 in / 
# Tue, 05 Oct 2021 00:02:45 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:46 GMT
VOLUME [/tmp]
# Tue, 05 Oct 2021 00:02:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:02:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada4a68136f6bd05b10da7bee212076d31c246cdcb1242cce64b1ef67c0d573`  
		Last Modified: Tue, 05 Oct 2021 00:05:09 GMT  
		Size: 20.0 MB (19979857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:36d54f6bf40b7deae0d97bc613093565077a1a31b9aa58667c80a6e91121343d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4423c30793a781d7f5cbb6dfb62ab5085f97914b59a3bbd4fbd1c34c2bdee1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY file:2afc08f94cbfa383acddc913141df64725fc71831a54c44b71019f36df84364c in / 
# Mon, 04 Oct 2021 23:44:24 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:24 GMT
VOLUME [/tmp]
# Mon, 04 Oct 2021 23:44:24 GMT
ENTRYPOINT ["/traefik"]
# Mon, 04 Oct 2021 23:44:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef9a8ab3b3f0f0e34c3c4acb9c07beca418533bcb7ef100f0aa56a951fc9e9`  
		Last Modified: Mon, 04 Oct 2021 23:45:39 GMT  
		Size: 19.5 MB (19518068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:6b832fb0bc93489b0aafbf3aabecb0c2c5288cf7118673e80b90eda1d28410eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:81038c31f0c7151418b10af58c252fb5e4d76c11a3d0b7a22aa66d61c3aadadc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21176792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d154c84159a4d96e8aedebfa3bce9d19fc139b450d3b4eee1bb46e4ab759a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:15:05 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 01 Sep 2021 06:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 01 Sep 2021 06:15:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 01 Sep 2021 06:15:16 GMT
EXPOSE 80
# Wed, 01 Sep 2021 06:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 06:15:17 GMT
CMD ["traefik"]
# Wed, 01 Sep 2021 06:15:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f794cbdc99470251c9539251dc8a5aba6a6f0d6b4fd07a519bf8d13a9d42bbec`  
		Last Modified: Wed, 01 Sep 2021 06:16:08 GMT  
		Size: 674.2 KB (674226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa68ae87a84c1bc651faa725d25b0c37abf9514b31398de8ec4113c983f7bd3c`  
		Last Modified: Wed, 01 Sep 2021 06:16:31 GMT  
		Size: 17.7 MB (17684891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6a80456e69fce8cd53394e12769c6b2757b1a318d8abd6eb0b1aa982e6791`  
		Last Modified: Wed, 01 Sep 2021 06:16:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f39845bff770219bdd5a8b6f84f21ee4b39134fad4a31e8a4a3c54f0cd8056f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6b253765bd18d5a529ad3c93327f907ab6c712f669a762c9806bb81dde006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Oct 2021 00:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Oct 2021 00:02:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Oct 2021 00:02:16 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:02:17 GMT
CMD ["traefik"]
# Tue, 05 Oct 2021 00:02:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d5f55b31f41aaac3372273955177ca7870585cbb870360b3d7dbf89f51266`  
		Last Modified: Tue, 05 Oct 2021 00:04:31 GMT  
		Size: 20.0 MB (19979916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e01da9fa02909dac56cbefbb8369298874c7eec6ffab823508744daa3900f5`  
		Last Modified: Tue, 05 Oct 2021 00:04:18 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2e12de8167c672b01390f08925e4d0c2358c030ba695c1056352ae3281d8505a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cdbea4a019b387ed0bcaa01580751374c1af2813d9561495c41b37f24d1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 04 Oct 2021 23:44:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 04 Oct 2021 23:44:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 04 Oct 2021 23:44:10 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Oct 2021 23:44:10 GMT
CMD ["traefik"]
# Mon, 04 Oct 2021 23:44:10 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bab87e61952bc1950c49311bd75a7fb2e2ea736191294f0eb6ff24c9bf0e3`  
		Last Modified: Mon, 04 Oct 2021 23:45:16 GMT  
		Size: 19.5 MB (19518028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd6503819a6bef01ca23b02b60ce103975ea1f188a9d8d025c3a29021dee79`  
		Last Modified: Mon, 04 Oct 2021 23:45:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1ec8a6971ea515c6e938ae4ef038d946e607c413f4a7793cb59e3fec70902d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:ab0698c8ee0db93af08da62353c6b314612343b2a9c7d9137d49ccbce9dc047e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708923892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff742be7b268a7e38f0f67b6f834a0650c65df642cb307e59b296bcf0c74ead6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 00:15:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 05 Oct 2021 00:15:22 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:15:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:15:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692bfe71d7ec563f28ecbd54c7b1ebc2c2c1cb8d54506cc7087afda6f8e9578`  
		Last Modified: Tue, 05 Oct 2021 00:16:01 GMT  
		Size: 22.2 MB (22220356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65addfc2b54f8fc5d623cb7bbfa9d8cb6c188caf2794d8f65ef04a635244c5e0`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1f22da3fdedf199c0ccfab0c55245e26e428715a6cfd70ac796d642970e56`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15bb35f7823dc2b058fe3fa77757b9f3dd32ed8c9340d960bd80261d3a3f23`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.31`

```console
$ docker pull traefik@sha256:536377b698b5caf61175360fe1f8af8c5641351a9f3319c5a094b890c540f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:298922381e42974e1474ade0b532961b2edc760d3774b4456222817d1e8e384c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20411133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201a05093074172e604f0dc53b6dc3648e95fec6610d36f49f6aa02602662d5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 05 Oct 2021 00:02:44 GMT
COPY file:10848119ebd67ebb26ec33871e75e75b528afb4dffb89e242f4feca4019c3093 in / 
# Tue, 05 Oct 2021 00:02:45 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:46 GMT
VOLUME [/tmp]
# Tue, 05 Oct 2021 00:02:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:02:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada4a68136f6bd05b10da7bee212076d31c246cdcb1242cce64b1ef67c0d573`  
		Last Modified: Tue, 05 Oct 2021 00:05:09 GMT  
		Size: 20.0 MB (19979857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:36d54f6bf40b7deae0d97bc613093565077a1a31b9aa58667c80a6e91121343d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19949342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4423c30793a781d7f5cbb6dfb62ab5085f97914b59a3bbd4fbd1c34c2bdee1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY file:2afc08f94cbfa383acddc913141df64725fc71831a54c44b71019f36df84364c in / 
# Mon, 04 Oct 2021 23:44:24 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:24 GMT
VOLUME [/tmp]
# Mon, 04 Oct 2021 23:44:24 GMT
ENTRYPOINT ["/traefik"]
# Mon, 04 Oct 2021 23:44:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef9a8ab3b3f0f0e34c3c4acb9c07beca418533bcb7ef100f0aa56a951fc9e9`  
		Last Modified: Mon, 04 Oct 2021 23:45:39 GMT  
		Size: 19.5 MB (19518068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.31-alpine`

```console
$ docker pull traefik@sha256:1824ec8b26cd6a410048018a93ce93c2fe0e10e7d21f92e5610efe96814c6dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.31-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8f39845bff770219bdd5a8b6f84f21ee4b39134fad4a31e8a4a3c54f0cd8056f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6b253765bd18d5a529ad3c93327f907ab6c712f669a762c9806bb81dde006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Oct 2021 00:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Oct 2021 00:02:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Oct 2021 00:02:16 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:02:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:02:17 GMT
CMD ["traefik"]
# Tue, 05 Oct 2021 00:02:17 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d5f55b31f41aaac3372273955177ca7870585cbb870360b3d7dbf89f51266`  
		Last Modified: Tue, 05 Oct 2021 00:04:31 GMT  
		Size: 20.0 MB (19979916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e01da9fa02909dac56cbefbb8369298874c7eec6ffab823508744daa3900f5`  
		Last Modified: Tue, 05 Oct 2021 00:04:18 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.31-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2e12de8167c672b01390f08925e4d0c2358c030ba695c1056352ae3281d8505a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22889081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cdbea4a019b387ed0bcaa01580751374c1af2813d9561495c41b37f24d1d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 04 Oct 2021 23:44:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 04 Oct 2021 23:44:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 04 Oct 2021 23:44:10 GMT
EXPOSE 80
# Mon, 04 Oct 2021 23:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Oct 2021 23:44:10 GMT
CMD ["traefik"]
# Mon, 04 Oct 2021 23:44:10 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bab87e61952bc1950c49311bd75a7fb2e2ea736191294f0eb6ff24c9bf0e3`  
		Last Modified: Mon, 04 Oct 2021 23:45:16 GMT  
		Size: 19.5 MB (19518028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd6503819a6bef01ca23b02b60ce103975ea1f188a9d8d025c3a29021dee79`  
		Last Modified: Mon, 04 Oct 2021 23:45:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.31-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1ec8a6971ea515c6e938ae4ef038d946e607c413f4a7793cb59e3fec70902d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:v1.7.31-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:ab0698c8ee0db93af08da62353c6b314612343b2a9c7d9137d49ccbce9dc047e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708923892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff742be7b268a7e38f0f67b6f834a0650c65df642cb307e59b296bcf0c74ead6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 00:15:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.31/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 05 Oct 2021 00:15:22 GMT
EXPOSE 80
# Tue, 05 Oct 2021 00:15:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 Oct 2021 00:15:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692bfe71d7ec563f28ecbd54c7b1ebc2c2c1cb8d54506cc7087afda6f8e9578`  
		Last Modified: Tue, 05 Oct 2021 00:16:01 GMT  
		Size: 22.2 MB (22220356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65addfc2b54f8fc5d623cb7bbfa9d8cb6c188caf2794d8f65ef04a635244c5e0`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1f22da3fdedf199c0ccfab0c55245e26e428715a6cfd70ac796d642970e56`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15bb35f7823dc2b058fe3fa77757b9f3dd32ed8c9340d960bd80261d3a3f23`  
		Last Modified: Tue, 05 Oct 2021 00:15:54 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:v2.5-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.3`

```console
$ docker pull traefik@sha256:f40028d9771cb29a35392b4cbdd655625596a319b915061e306c503059d0b6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:b3f4abc5706a00dc886b8b8483dbadf691314d6000f7f2f8736bfe9158cfddbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29057668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d933d21fd8a09022ca5cf067fb195fbfccf0f5c2b5d750d2d1d6eb562b6a8b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:28:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:33:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:33:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:33:57 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:33:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5295d3cd66d0f8651338b81063a408fcc2c70d810c92e5cb435c467a1939d60`  
		Last Modified: Thu, 02 Sep 2021 17:29:12 GMT  
		Size: 656.4 KB (656356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a291a928e2c186dfda0482997e46082d5f3f59ece15af68d716daaece906a`  
		Last Modified: Mon, 20 Sep 2021 22:34:29 GMT  
		Size: 25.6 MB (25586499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367d83d5091433850e079372929625c34f7297930b7c5853c4af8740df8c470`  
		Last Modified: Mon, 20 Sep 2021 22:34:24 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e12c0a18cae5675bbc0c133f445b96489fbf6617c66ebf254aa4499b5e4bce04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27303193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f235df3e981ae502eea1719af18b8fdf666ff7adf6602fd7522a02428fe2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 18:16:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 23:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 23:02:05 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 23:02:06 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:02:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 23:02:06 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 23:02:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac532a93bbc80e8fcf54dcb6ef0229a94aa4f2c94f0e9afec75226cfd91451c`  
		Last Modified: Thu, 02 Sep 2021 18:17:59 GMT  
		Size: 662.0 KB (661991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06452c3a5e8e127597025204daab5d7e08fd26a9604e469bffead7c88192f263`  
		Last Modified: Mon, 20 Sep 2021 23:04:10 GMT  
		Size: 24.0 MB (24013387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c9059e1c58be06e68f3ff3d92f20dc6295e8bbd7a588693346718bf872ee57`  
		Last Modified: Mon, 20 Sep 2021 23:03:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:642ea446082cd3cd29a00d89447be819f0e1226e0c2643cb5ecfc9259c2d85e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26720590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026ae4c43ba7bf101b11c8a12d09e3a0bc6858ac98433c5b9c0133b379b6c36b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 02 Sep 2021 17:46:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Sep 2021 22:44:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Sep 2021 22:44:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Sep 2021 22:44:58 GMT
EXPOSE 80
# Mon, 20 Sep 2021 22:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Sep 2021 22:44:58 GMT
CMD ["traefik"]
# Mon, 20 Sep 2021 22:44:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b5f395e28da206554aa30d5732a9b9a134cb909215e47a12301afbb1dba15`  
		Last Modified: Thu, 02 Sep 2021 17:47:55 GMT  
		Size: 658.9 KB (658858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef03ca17e72ecae6b44198d22bbcbf2a29c03bfdc2e63a0083dc77967bbd8b9`  
		Last Modified: Mon, 20 Sep 2021 22:45:57 GMT  
		Size: 23.3 MB (23349537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267983b7cc1765fa911ad76ce5d7d6c3ff57cf87ae52ff4a8cf79bd810aa8ce3`  
		Last Modified: Mon, 20 Sep 2021 22:45:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:v2.5.3-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:f477c676d05e5445ca0a7dfd08f2b46de13a95d760f27704cc2352970b7c1e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull traefik@sha256:83ba3ec6a46a9674e26043fe76cad156bf41d997f816b29a2744dbee81f998c2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712907530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ed3ac6db10312765b3172f418f0b2e08d33e8a0427fd1521e61911c3353dbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Sep 2021 23:09:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.3/traefik_v2.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 20 Sep 2021 23:09:35 GMT
EXPOSE 80
# Mon, 20 Sep 2021 23:09:36 GMT
ENTRYPOINT ["/traefik"]
# Mon, 20 Sep 2021 23:09:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ade23375ad0841426448992a4f25970f6534b0cb39834cecbdab93bed1ef17`  
		Last Modified: Mon, 20 Sep 2021 23:10:38 GMT  
		Size: 26.2 MB (26204294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf980003c9648a4ed498899b26dd4fcd5fd3ec2e195a6c9c977a5c8696c4f8`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28328bfa6a8a6ec8758c589337295e05e5b6ed23e701cc6c77d3132e962505e7`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408aeb13ffb205eebfce6da260fffa9bc5949eee4ca3e5d208a2e097d290933`  
		Last Modified: Mon, 20 Sep 2021 23:10:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
