<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.10`](#traefik210)
-	[`traefik:2.10-windowsservercore-1809`](#traefik210-windowsservercore-1809)
-	[`traefik:2.10.6`](#traefik2106)
-	[`traefik:2.10.6-windowsservercore-1809`](#traefik2106-windowsservercore-1809)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0.0-beta4`](#traefik300-beta4)
-	[`traefik:3.0.0-beta4-windowsservercore-1809`](#traefik300-beta4-windowsservercore-1809)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:saintmarcelin`](#traefiksaintmarcelin)
-	[`traefik:saintmarcelin-windowsservercore-1809`](#traefiksaintmarcelin-windowsservercore-1809)
-	[`traefik:v2.10`](#traefikv210)
-	[`traefik:v2.10-windowsservercore-1809`](#traefikv210-windowsservercore-1809)
-	[`traefik:v2.10.6`](#traefikv2106)
-	[`traefik:v2.10.6-windowsservercore-1809`](#traefikv2106-windowsservercore-1809)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0.0-beta4`](#traefikv300-beta4)
-	[`traefik:v3.0.0-beta4-windowsservercore-1809`](#traefikv300-beta4-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:2.10`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:2.10-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.6`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10.6` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.6` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:2.10.6-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:9afeb3c0c8e227ba7558a779bc438a9f36924e672a961f8f25f3ae229330f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:3bfc7a31d9e84d367dc1e0ef8bdca7d1be8a9e145dbd12d69c95b2f8a622cab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ead60b3eadbd783a07fda234ce3a79c6df478ebc53eb1f5eb9253de44c12dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:20 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:20 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76dc727ba30d26f38eb96088b126a33484c942b203bac645d4c2a43b6b44d6`  
		Last Modified: Wed, 29 Nov 2023 06:31:45 GMT  
		Size: 40.2 MB (40152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cacff58c809b575df8a81247796438d3d67dd458b327a246925d7823eedeb9`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e44e7ba4e35cddd5ecc8c7150c975e4e82c847667d6d5e8d609b08246e5eb237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb704fb8a06f6a5afa8ff00b4e7ccec3f7a9ae4dcb8796ec11492a47f397e930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:08:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:08:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:08:53 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:08:53 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:08:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412c44da4875fd3379a0bd4c39f450227ccb72340ba0becb081b45561ffabb1`  
		Last Modified: Wed, 29 Nov 2023 06:09:19 GMT  
		Size: 37.9 MB (37910923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c037012508121a9b38d1c9119f72cbdadf57cf0b85e3846b96550b9f84b6c8`  
		Last Modified: Wed, 29 Nov 2023 06:09:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69e08717095a1cebe8116d725fe05875ac9ceb9fee7210ea95ebb3447ed807ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41118821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf0dc42a3d884d0e3ab81570521c10ff3ff142360557d6366094b4f43bacac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:19 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:19 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e07a049aa343f7c511494842e7d2a810402edc88e2a9a0440ad9d25c03813f`  
		Last Modified: Wed, 29 Nov 2023 05:46:42 GMT  
		Size: 37.2 MB (37162104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692567c97c9e3c418dda0f98b329619afc566883971f8654389f37509023e6bf`  
		Last Modified: Wed, 29 Nov 2023 05:46:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:c0cacfc13537e3e300c438622b3f4f3d968b8acc064b1279af34f468464050cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42933408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49a44fc7d35b2e9c02a3d2d3ff65a2052b7ac11b6b3bfa116c5eabeb6d8f3d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:45:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:05 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:05 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404ca1a348f82a1bfe6d8b39b3c42a238f2c9403145bb90d9a7af5443cfd1b`  
		Last Modified: Wed, 29 Nov 2023 00:47:32 GMT  
		Size: 39.1 MB (39095092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211580b30f098dab76d62b8918df76e1c68707987440c7d112557c5780b9d2`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:19630807862f87484e67cb4ee380dc6b4c9d23b693e339472b48d45e98a6695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:2ac02e64d356daa1dc8fd1301b6f2a67b6e5681094cab384fcde2008bec02b5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099063656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6022b519d40f6afa656a268503f5487de25ab4599c5fe32953f7385e93caa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:32:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:32:54 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:32:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:32:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577447714f894136f8dcad02f5144f013700f52a7e4a8b77322663ae827843d`  
		Last Modified: Thu, 16 Nov 2023 08:35:07 GMT  
		Size: 41.6 MB (41626426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61adfc07856bba95f19fddcd43601f7dd9190e96e276d19c73bae90e35447f22`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215667b5b3d0976317192c1b9badaec9fe636ab5d80c144142c473f59478d4a`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163722bd41e08e30b2a76118757ac999944507ea8852fc449f7f1bccb147e0e`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta4`

```console
$ docker pull traefik@sha256:9afeb3c0c8e227ba7558a779bc438a9f36924e672a961f8f25f3ae229330f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0.0-beta4` - linux; amd64

```console
$ docker pull traefik@sha256:3bfc7a31d9e84d367dc1e0ef8bdca7d1be8a9e145dbd12d69c95b2f8a622cab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ead60b3eadbd783a07fda234ce3a79c6df478ebc53eb1f5eb9253de44c12dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:20 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:20 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76dc727ba30d26f38eb96088b126a33484c942b203bac645d4c2a43b6b44d6`  
		Last Modified: Wed, 29 Nov 2023 06:31:45 GMT  
		Size: 40.2 MB (40152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cacff58c809b575df8a81247796438d3d67dd458b327a246925d7823eedeb9`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e44e7ba4e35cddd5ecc8c7150c975e4e82c847667d6d5e8d609b08246e5eb237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb704fb8a06f6a5afa8ff00b4e7ccec3f7a9ae4dcb8796ec11492a47f397e930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:08:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:08:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:08:53 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:08:53 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:08:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412c44da4875fd3379a0bd4c39f450227ccb72340ba0becb081b45561ffabb1`  
		Last Modified: Wed, 29 Nov 2023 06:09:19 GMT  
		Size: 37.9 MB (37910923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c037012508121a9b38d1c9119f72cbdadf57cf0b85e3846b96550b9f84b6c8`  
		Last Modified: Wed, 29 Nov 2023 06:09:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69e08717095a1cebe8116d725fe05875ac9ceb9fee7210ea95ebb3447ed807ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41118821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf0dc42a3d884d0e3ab81570521c10ff3ff142360557d6366094b4f43bacac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:19 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:19 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e07a049aa343f7c511494842e7d2a810402edc88e2a9a0440ad9d25c03813f`  
		Last Modified: Wed, 29 Nov 2023 05:46:42 GMT  
		Size: 37.2 MB (37162104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692567c97c9e3c418dda0f98b329619afc566883971f8654389f37509023e6bf`  
		Last Modified: Wed, 29 Nov 2023 05:46:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta4` - linux; s390x

```console
$ docker pull traefik@sha256:c0cacfc13537e3e300c438622b3f4f3d968b8acc064b1279af34f468464050cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42933408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49a44fc7d35b2e9c02a3d2d3ff65a2052b7ac11b6b3bfa116c5eabeb6d8f3d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:45:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:05 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:05 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404ca1a348f82a1bfe6d8b39b3c42a238f2c9403145bb90d9a7af5443cfd1b`  
		Last Modified: Wed, 29 Nov 2023 00:47:32 GMT  
		Size: 39.1 MB (39095092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211580b30f098dab76d62b8918df76e1c68707987440c7d112557c5780b9d2`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:19630807862f87484e67cb4ee380dc6b4c9d23b693e339472b48d45e98a6695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:3.0.0-beta4-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:2ac02e64d356daa1dc8fd1301b6f2a67b6e5681094cab384fcde2008bec02b5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099063656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6022b519d40f6afa656a268503f5487de25ab4599c5fe32953f7385e93caa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:32:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:32:54 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:32:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:32:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577447714f894136f8dcad02f5144f013700f52a7e4a8b77322663ae827843d`  
		Last Modified: Thu, 16 Nov 2023 08:35:07 GMT  
		Size: 41.6 MB (41626426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61adfc07856bba95f19fddcd43601f7dd9190e96e276d19c73bae90e35447f22`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215667b5b3d0976317192c1b9badaec9fe636ab5d80c144142c473f59478d4a`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163722bd41e08e30b2a76118757ac999944507ea8852fc449f7f1bccb147e0e`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:9afeb3c0c8e227ba7558a779bc438a9f36924e672a961f8f25f3ae229330f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:3bfc7a31d9e84d367dc1e0ef8bdca7d1be8a9e145dbd12d69c95b2f8a622cab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ead60b3eadbd783a07fda234ce3a79c6df478ebc53eb1f5eb9253de44c12dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:20 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:20 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76dc727ba30d26f38eb96088b126a33484c942b203bac645d4c2a43b6b44d6`  
		Last Modified: Wed, 29 Nov 2023 06:31:45 GMT  
		Size: 40.2 MB (40152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cacff58c809b575df8a81247796438d3d67dd458b327a246925d7823eedeb9`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e44e7ba4e35cddd5ecc8c7150c975e4e82c847667d6d5e8d609b08246e5eb237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb704fb8a06f6a5afa8ff00b4e7ccec3f7a9ae4dcb8796ec11492a47f397e930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:08:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:08:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:08:53 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:08:53 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:08:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412c44da4875fd3379a0bd4c39f450227ccb72340ba0becb081b45561ffabb1`  
		Last Modified: Wed, 29 Nov 2023 06:09:19 GMT  
		Size: 37.9 MB (37910923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c037012508121a9b38d1c9119f72cbdadf57cf0b85e3846b96550b9f84b6c8`  
		Last Modified: Wed, 29 Nov 2023 06:09:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69e08717095a1cebe8116d725fe05875ac9ceb9fee7210ea95ebb3447ed807ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41118821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf0dc42a3d884d0e3ab81570521c10ff3ff142360557d6366094b4f43bacac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:19 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:19 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e07a049aa343f7c511494842e7d2a810402edc88e2a9a0440ad9d25c03813f`  
		Last Modified: Wed, 29 Nov 2023 05:46:42 GMT  
		Size: 37.2 MB (37162104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692567c97c9e3c418dda0f98b329619afc566883971f8654389f37509023e6bf`  
		Last Modified: Wed, 29 Nov 2023 05:46:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:c0cacfc13537e3e300c438622b3f4f3d968b8acc064b1279af34f468464050cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42933408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49a44fc7d35b2e9c02a3d2d3ff65a2052b7ac11b6b3bfa116c5eabeb6d8f3d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:45:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:05 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:05 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404ca1a348f82a1bfe6d8b39b3c42a238f2c9403145bb90d9a7af5443cfd1b`  
		Last Modified: Wed, 29 Nov 2023 00:47:32 GMT  
		Size: 39.1 MB (39095092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211580b30f098dab76d62b8918df76e1c68707987440c7d112557c5780b9d2`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:19630807862f87484e67cb4ee380dc6b4c9d23b693e339472b48d45e98a6695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:2ac02e64d356daa1dc8fd1301b6f2a67b6e5681094cab384fcde2008bec02b5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099063656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6022b519d40f6afa656a268503f5487de25ab4599c5fe32953f7385e93caa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:32:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:32:54 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:32:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:32:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577447714f894136f8dcad02f5144f013700f52a7e4a8b77322663ae827843d`  
		Last Modified: Thu, 16 Nov 2023 08:35:07 GMT  
		Size: 41.6 MB (41626426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61adfc07856bba95f19fddcd43601f7dd9190e96e276d19c73bae90e35447f22`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215667b5b3d0976317192c1b9badaec9fe636ab5d80c144142c473f59478d4a`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163722bd41e08e30b2a76118757ac999944507ea8852fc449f7f1bccb147e0e`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:saintmarcelin` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:saintmarcelin-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:v2.10-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.6`

```console
$ docker pull traefik@sha256:5f99d9c100d5e9e7ff7f88f5312ae3fe47c28a4a81993f2c876975ed70f0cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10.6` - linux; amd64

```console
$ docker pull traefik@sha256:b24c16c9e07f7966fa7053dc1f5cbab55a52d7ebc27b1b47f06ffbf6e74300c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43229578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cdefb2f44dc58b68182898241a11cdd0d1f42e8f4f0b751c3d65a9afb197af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:27 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:28 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7e7be3ff2eb024c7b69ac4a43c4a4bd889658719c1d44a047a23093de50d0`  
		Last Modified: Wed, 29 Nov 2023 06:32:05 GMT  
		Size: 39.2 MB (39204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eedc6a01b11648a3ef09decd0f5fe7dc77d79f1f423fbf694e5e72bf0aad727`  
		Last Modified: Wed, 29 Nov 2023 06:31:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ee4c9390ec239d494e291a1c287e0446ef7c3bc65bf44f8149129be679fb0ea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40819799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb69008e6b5ca4b2e9f8fac574fc302587f6484159604be6b60b67ef18c6b12d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:09:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:09:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:09:00 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:09:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:09:00 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c2cd2ed2db68cde60fea11fadd614e21b54715f4b187d262a44adaaeea0ba`  
		Last Modified: Wed, 29 Nov 2023 06:09:41 GMT  
		Size: 37.1 MB (37051415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb4d81d2128391f399b4a113650a73713d9043fe0bd8610d60416461a8f08d`  
		Last Modified: Wed, 29 Nov 2023 06:09:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fb2b2d4ba7fa84d4df30aa7f39d24d990da97c8a89edc95fae0a13db29c5eacc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40217109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6cf9d511ec323b99dc8a36da0d4ecee3682321b430cd66db33b7524584039a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:25 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:25 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95059fa99e09dbde33cb526d541164644a28542b49d664a19f2b9a31249481df`  
		Last Modified: Wed, 29 Nov 2023 05:47:01 GMT  
		Size: 36.3 MB (36260392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0095e4c4a053c89641ac5307d800208b58cd7675ac891d827f18addb52c9d870`  
		Last Modified: Wed, 29 Nov 2023 05:46:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.6` - linux; s390x

```console
$ docker pull traefik@sha256:1f73a129ceb164fcee414c47e2eeb8166b950ef30728bb86a4142d2fcba75360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42050681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43753aaf21fdf5d7a44475c270504fe5cd018c9a10995cc3bc63defd17ed8661`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:46:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:30 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:30 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0bf7a3ef99bf94af2497d00978f85d1009602ec9ec764aa643647e5e5bc653`  
		Last Modified: Wed, 29 Nov 2023 00:47:50 GMT  
		Size: 38.2 MB (38212366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bd88c0a01deb2371f3822ce3181d55c12b4f33668758d93f9de2a85e812fe4`  
		Last Modified: Wed, 29 Nov 2023 00:47:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:v2.10.6-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:9afeb3c0c8e227ba7558a779bc438a9f36924e672a961f8f25f3ae229330f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:3bfc7a31d9e84d367dc1e0ef8bdca7d1be8a9e145dbd12d69c95b2f8a622cab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ead60b3eadbd783a07fda234ce3a79c6df478ebc53eb1f5eb9253de44c12dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:20 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:20 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76dc727ba30d26f38eb96088b126a33484c942b203bac645d4c2a43b6b44d6`  
		Last Modified: Wed, 29 Nov 2023 06:31:45 GMT  
		Size: 40.2 MB (40152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cacff58c809b575df8a81247796438d3d67dd458b327a246925d7823eedeb9`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e44e7ba4e35cddd5ecc8c7150c975e4e82c847667d6d5e8d609b08246e5eb237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb704fb8a06f6a5afa8ff00b4e7ccec3f7a9ae4dcb8796ec11492a47f397e930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:08:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:08:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:08:53 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:08:53 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:08:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412c44da4875fd3379a0bd4c39f450227ccb72340ba0becb081b45561ffabb1`  
		Last Modified: Wed, 29 Nov 2023 06:09:19 GMT  
		Size: 37.9 MB (37910923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c037012508121a9b38d1c9119f72cbdadf57cf0b85e3846b96550b9f84b6c8`  
		Last Modified: Wed, 29 Nov 2023 06:09:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69e08717095a1cebe8116d725fe05875ac9ceb9fee7210ea95ebb3447ed807ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41118821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf0dc42a3d884d0e3ab81570521c10ff3ff142360557d6366094b4f43bacac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:19 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:19 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e07a049aa343f7c511494842e7d2a810402edc88e2a9a0440ad9d25c03813f`  
		Last Modified: Wed, 29 Nov 2023 05:46:42 GMT  
		Size: 37.2 MB (37162104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692567c97c9e3c418dda0f98b329619afc566883971f8654389f37509023e6bf`  
		Last Modified: Wed, 29 Nov 2023 05:46:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:c0cacfc13537e3e300c438622b3f4f3d968b8acc064b1279af34f468464050cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42933408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49a44fc7d35b2e9c02a3d2d3ff65a2052b7ac11b6b3bfa116c5eabeb6d8f3d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:45:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:05 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:05 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404ca1a348f82a1bfe6d8b39b3c42a238f2c9403145bb90d9a7af5443cfd1b`  
		Last Modified: Wed, 29 Nov 2023 00:47:32 GMT  
		Size: 39.1 MB (39095092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211580b30f098dab76d62b8918df76e1c68707987440c7d112557c5780b9d2`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:19630807862f87484e67cb4ee380dc6b4c9d23b693e339472b48d45e98a6695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:2ac02e64d356daa1dc8fd1301b6f2a67b6e5681094cab384fcde2008bec02b5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099063656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6022b519d40f6afa656a268503f5487de25ab4599c5fe32953f7385e93caa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:32:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:32:54 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:32:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:32:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577447714f894136f8dcad02f5144f013700f52a7e4a8b77322663ae827843d`  
		Last Modified: Thu, 16 Nov 2023 08:35:07 GMT  
		Size: 41.6 MB (41626426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61adfc07856bba95f19fddcd43601f7dd9190e96e276d19c73bae90e35447f22`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215667b5b3d0976317192c1b9badaec9fe636ab5d80c144142c473f59478d4a`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163722bd41e08e30b2a76118757ac999944507ea8852fc449f7f1bccb147e0e`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta4`

```console
$ docker pull traefik@sha256:9afeb3c0c8e227ba7558a779bc438a9f36924e672a961f8f25f3ae229330f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0.0-beta4` - linux; amd64

```console
$ docker pull traefik@sha256:3bfc7a31d9e84d367dc1e0ef8bdca7d1be8a9e145dbd12d69c95b2f8a622cab4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ead60b3eadbd783a07fda234ce3a79c6df478ebc53eb1f5eb9253de44c12dcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:31:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:31:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:31:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:31:20 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:31:20 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:31:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550423c3d1314ff5c8a13904f583e11da40f2e6a9cb9178d6a9ddaf589a41779`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 622.3 KB (622306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76dc727ba30d26f38eb96088b126a33484c942b203bac645d4c2a43b6b44d6`  
		Last Modified: Wed, 29 Nov 2023 06:31:45 GMT  
		Size: 40.2 MB (40152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cacff58c809b575df8a81247796438d3d67dd458b327a246925d7823eedeb9`  
		Last Modified: Wed, 29 Nov 2023 06:31:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:e44e7ba4e35cddd5ecc8c7150c975e4e82c847667d6d5e8d609b08246e5eb237
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41679307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb704fb8a06f6a5afa8ff00b4e7ccec3f7a9ae4dcb8796ec11492a47f397e930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 06:08:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 06:08:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 06:08:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 06:08:53 GMT
EXPOSE 80
# Wed, 29 Nov 2023 06:08:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 06:08:53 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 06:08:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560ac1492fab77141400f65ad727f721927e8b6e900b4ac28c26f979bca126b`  
		Last Modified: Wed, 29 Nov 2023 06:09:13 GMT  
		Size: 622.7 KB (622724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412c44da4875fd3379a0bd4c39f450227ccb72340ba0becb081b45561ffabb1`  
		Last Modified: Wed, 29 Nov 2023 06:09:19 GMT  
		Size: 37.9 MB (37910923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c037012508121a9b38d1c9119f72cbdadf57cf0b85e3846b96550b9f84b6c8`  
		Last Modified: Wed, 29 Nov 2023 06:09:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69e08717095a1cebe8116d725fe05875ac9ceb9fee7210ea95ebb3447ed807ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41118821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf0dc42a3d884d0e3ab81570521c10ff3ff142360557d6366094b4f43bacac9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 05:46:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 05:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 05:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 05:46:19 GMT
EXPOSE 80
# Wed, 29 Nov 2023 05:46:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 05:46:19 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 05:46:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3e1d74d27dfa82cc4925dee376ed0ba2c7017bfbd86256a39cd43e067564f2`  
		Last Modified: Wed, 29 Nov 2023 05:46:38 GMT  
		Size: 624.5 KB (624518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e07a049aa343f7c511494842e7d2a810402edc88e2a9a0440ad9d25c03813f`  
		Last Modified: Wed, 29 Nov 2023 05:46:42 GMT  
		Size: 37.2 MB (37162104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692567c97c9e3c418dda0f98b329619afc566883971f8654389f37509023e6bf`  
		Last Modified: Wed, 29 Nov 2023 05:46:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta4` - linux; s390x

```console
$ docker pull traefik@sha256:c0cacfc13537e3e300c438622b3f4f3d968b8acc064b1279af34f468464050cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42933408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49a44fc7d35b2e9c02a3d2d3ff65a2052b7ac11b6b3bfa116c5eabeb6d8f3d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Wed, 29 Nov 2023 00:45:49 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Nov 2023 00:45:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Nov 2023 00:46:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Nov 2023 00:46:05 GMT
EXPOSE 80
# Wed, 29 Nov 2023 00:46:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Nov 2023 00:46:05 GMT
CMD ["traefik"]
# Wed, 29 Nov 2023 00:46:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef466f0f3a71ca493d3026cd1c1e85592db97303a55121345c9626424dd0d941`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 622.8 KB (622844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3404ca1a348f82a1bfe6d8b39b3c42a238f2c9403145bb90d9a7af5443cfd1b`  
		Last Modified: Wed, 29 Nov 2023 00:47:32 GMT  
		Size: 39.1 MB (39095092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211580b30f098dab76d62b8918df76e1c68707987440c7d112557c5780b9d2`  
		Last Modified: Wed, 29 Nov 2023 00:47:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:19630807862f87484e67cb4ee380dc6b4c9d23b693e339472b48d45e98a6695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:v3.0.0-beta4-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:2ac02e64d356daa1dc8fd1301b6f2a67b6e5681094cab384fcde2008bec02b5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099063656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6022b519d40f6afa656a268503f5487de25ab4599c5fe32953f7385e93caa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:32:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta4/traefik_v3.0.0-beta4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:32:54 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:32:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:32:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8577447714f894136f8dcad02f5144f013700f52a7e4a8b77322663ae827843d`  
		Last Modified: Thu, 16 Nov 2023 08:35:07 GMT  
		Size: 41.6 MB (41626426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61adfc07856bba95f19fddcd43601f7dd9190e96e276d19c73bae90e35447f22`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215667b5b3d0976317192c1b9badaec9fe636ab5d80c144142c473f59478d4a`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163722bd41e08e30b2a76118757ac999944507ea8852fc449f7f1bccb147e0e`  
		Last Modified: Thu, 16 Nov 2023 08:34:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
