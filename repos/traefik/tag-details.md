<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.10`](#traefik210)
-	[`traefik:2.10-windowsservercore-1809`](#traefik210-windowsservercore-1809)
-	[`traefik:2.10.4`](#traefik2104)
-	[`traefik:2.10.4-windowsservercore-1809`](#traefik2104-windowsservercore-1809)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0.0-beta3`](#traefik300-beta3)
-	[`traefik:3.0.0-beta3-windowsservercore-1809`](#traefik300-beta3-windowsservercore-1809)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:saintmarcelin`](#traefiksaintmarcelin)
-	[`traefik:saintmarcelin-windowsservercore-1809`](#traefiksaintmarcelin-windowsservercore-1809)
-	[`traefik:v2.10`](#traefikv210)
-	[`traefik:v2.10-windowsservercore-1809`](#traefikv210-windowsservercore-1809)
-	[`traefik:v2.10.4`](#traefikv2104)
-	[`traefik:v2.10.4-windowsservercore-1809`](#traefikv2104-windowsservercore-1809)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0.0-beta3`](#traefikv300-beta3)
-	[`traefik:v3.0.0-beta3-windowsservercore-1809`](#traefikv300-beta3-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:2.10`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:2.10-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.4`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10.4` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:2.10.4-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:aab993a79d3d48c93f3dcd250ac3ef0aeb7b967ad73a317c8459b05ca7b07124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:db21af65fb9edaa04542efe69bb6ba74afa04231874b0240fcccb059547fbf24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42339283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2af65616272cb94e6157ff2c162b2949d831dfe72e5de461e32db2f458951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:28 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:28 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3fb410d5ad92d4b790c3aeff36ea3d4e6d1768c3d58cd9fadb8f574f8eb24a`  
		Last Modified: Wed, 09 Aug 2023 04:06:55 GMT  
		Size: 38.3 MB (38315021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25020b7f93004e310f3a03e903db4f1ba8ae45d9a5b5b3a594da55f18b0bc663`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:27d59eaf0a71f39755d29f3a8c8c7b7201f56d308c5798bd418370c1fcf5f2c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39835276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7abe214da586596b94490448c92c43ba2f265fc92b07be88fa5dc2278d1b01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:00 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:01 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703bd65860e0f9aa5ecded58786f3485cd7d4c971208e85e7b103c0ca67d9a0`  
		Last Modified: Fri, 29 Sep 2023 02:08:29 GMT  
		Size: 36.1 MB (36066901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13805ab706bdd42003ba6a623e50accab2364cd4fa0ff3f301ebb829cfbbea26`  
		Last Modified: Fri, 29 Sep 2023 02:08:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e55409b224d531f08d292ce5a7cb06f780e6d8d3f8c95a8a34ed4d07f38d667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39099261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbd4be29ca7d64655207995ea5252b5b6685dd95ede6bbe93e92a551cb2f59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:03 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:03 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da0a69e79037e30b0819ae2274df20430ea9bad7e4d8c097b1feadb24567ab`  
		Last Modified: Fri, 29 Sep 2023 02:24:25 GMT  
		Size: 35.1 MB (35142548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4ecaefb151e17955d4f6601aefdca3e6e6adf27c2858a8654f1642b6c5399`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:79ff1827a0fe4f8236b39ea8728144a7d9ad9c20443fab8bcaaa7421d2267ca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40951344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99842a54f239f3e13715141e6cfe726560cd79fee4167a72ff71c25219b5f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:18 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:18 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e08d6b62d3329493d6a6ead807303f1c265143bbda714fdef9382ae8c27a8d`  
		Last Modified: Fri, 29 Sep 2023 00:15:57 GMT  
		Size: 37.1 MB (37113034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7fa0850e9af9b35eca14f9c7eaaf6b8fcc591d1c20fca9d47ecaacb3e1b314`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:dab2b4b52465d429b1bf5b84ffa38c085ea1c00af3121846acd69ab445b4083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:dee2708e034f9398d1df57ca83b286b95a461705193b858a5b845bb5eec8a7b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29344f9d48c4d86ae52a026fbef4ef800a05ecf2a4fe72457d759dd3615d0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:33:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:33:50 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:33:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:33:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761997e52cfb63512b90853905a746fd9fd54e41674e2d4bcbb1cb8201dd8e6`  
		Last Modified: Wed, 13 Sep 2023 08:35:53 GMT  
		Size: 38.9 MB (38911475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68336a56fcbfa87a1c489e6104360ab265abb53897306e3d4b09b6a7649bcc28`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e209029cdcd07d20e5a87b03da02a4e8a0c69006f4837fb0d0eb73571be80d`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7cd492baf3537340fe6d001aa41f13f04e92943dc5fc877ffb6a51926b4db`  
		Last Modified: Wed, 13 Sep 2023 08:35:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta3`

```console
$ docker pull traefik@sha256:aab993a79d3d48c93f3dcd250ac3ef0aeb7b967ad73a317c8459b05ca7b07124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0.0-beta3` - linux; amd64

```console
$ docker pull traefik@sha256:db21af65fb9edaa04542efe69bb6ba74afa04231874b0240fcccb059547fbf24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42339283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2af65616272cb94e6157ff2c162b2949d831dfe72e5de461e32db2f458951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:28 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:28 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3fb410d5ad92d4b790c3aeff36ea3d4e6d1768c3d58cd9fadb8f574f8eb24a`  
		Last Modified: Wed, 09 Aug 2023 04:06:55 GMT  
		Size: 38.3 MB (38315021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25020b7f93004e310f3a03e903db4f1ba8ae45d9a5b5b3a594da55f18b0bc663`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:27d59eaf0a71f39755d29f3a8c8c7b7201f56d308c5798bd418370c1fcf5f2c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39835276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7abe214da586596b94490448c92c43ba2f265fc92b07be88fa5dc2278d1b01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:00 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:01 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703bd65860e0f9aa5ecded58786f3485cd7d4c971208e85e7b103c0ca67d9a0`  
		Last Modified: Fri, 29 Sep 2023 02:08:29 GMT  
		Size: 36.1 MB (36066901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13805ab706bdd42003ba6a623e50accab2364cd4fa0ff3f301ebb829cfbbea26`  
		Last Modified: Fri, 29 Sep 2023 02:08:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e55409b224d531f08d292ce5a7cb06f780e6d8d3f8c95a8a34ed4d07f38d667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39099261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbd4be29ca7d64655207995ea5252b5b6685dd95ede6bbe93e92a551cb2f59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:03 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:03 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da0a69e79037e30b0819ae2274df20430ea9bad7e4d8c097b1feadb24567ab`  
		Last Modified: Fri, 29 Sep 2023 02:24:25 GMT  
		Size: 35.1 MB (35142548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4ecaefb151e17955d4f6601aefdca3e6e6adf27c2858a8654f1642b6c5399`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; s390x

```console
$ docker pull traefik@sha256:79ff1827a0fe4f8236b39ea8728144a7d9ad9c20443fab8bcaaa7421d2267ca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40951344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99842a54f239f3e13715141e6cfe726560cd79fee4167a72ff71c25219b5f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:18 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:18 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e08d6b62d3329493d6a6ead807303f1c265143bbda714fdef9382ae8c27a8d`  
		Last Modified: Fri, 29 Sep 2023 00:15:57 GMT  
		Size: 37.1 MB (37113034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7fa0850e9af9b35eca14f9c7eaaf6b8fcc591d1c20fca9d47ecaacb3e1b314`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:dab2b4b52465d429b1bf5b84ffa38c085ea1c00af3121846acd69ab445b4083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:3.0.0-beta3-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:dee2708e034f9398d1df57ca83b286b95a461705193b858a5b845bb5eec8a7b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29344f9d48c4d86ae52a026fbef4ef800a05ecf2a4fe72457d759dd3615d0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:33:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:33:50 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:33:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:33:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761997e52cfb63512b90853905a746fd9fd54e41674e2d4bcbb1cb8201dd8e6`  
		Last Modified: Wed, 13 Sep 2023 08:35:53 GMT  
		Size: 38.9 MB (38911475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68336a56fcbfa87a1c489e6104360ab265abb53897306e3d4b09b6a7649bcc28`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e209029cdcd07d20e5a87b03da02a4e8a0c69006f4837fb0d0eb73571be80d`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7cd492baf3537340fe6d001aa41f13f04e92943dc5fc877ffb6a51926b4db`  
		Last Modified: Wed, 13 Sep 2023 08:35:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:aab993a79d3d48c93f3dcd250ac3ef0aeb7b967ad73a317c8459b05ca7b07124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:db21af65fb9edaa04542efe69bb6ba74afa04231874b0240fcccb059547fbf24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42339283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2af65616272cb94e6157ff2c162b2949d831dfe72e5de461e32db2f458951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:28 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:28 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3fb410d5ad92d4b790c3aeff36ea3d4e6d1768c3d58cd9fadb8f574f8eb24a`  
		Last Modified: Wed, 09 Aug 2023 04:06:55 GMT  
		Size: 38.3 MB (38315021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25020b7f93004e310f3a03e903db4f1ba8ae45d9a5b5b3a594da55f18b0bc663`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:27d59eaf0a71f39755d29f3a8c8c7b7201f56d308c5798bd418370c1fcf5f2c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39835276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7abe214da586596b94490448c92c43ba2f265fc92b07be88fa5dc2278d1b01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:00 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:01 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703bd65860e0f9aa5ecded58786f3485cd7d4c971208e85e7b103c0ca67d9a0`  
		Last Modified: Fri, 29 Sep 2023 02:08:29 GMT  
		Size: 36.1 MB (36066901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13805ab706bdd42003ba6a623e50accab2364cd4fa0ff3f301ebb829cfbbea26`  
		Last Modified: Fri, 29 Sep 2023 02:08:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e55409b224d531f08d292ce5a7cb06f780e6d8d3f8c95a8a34ed4d07f38d667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39099261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbd4be29ca7d64655207995ea5252b5b6685dd95ede6bbe93e92a551cb2f59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:03 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:03 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da0a69e79037e30b0819ae2274df20430ea9bad7e4d8c097b1feadb24567ab`  
		Last Modified: Fri, 29 Sep 2023 02:24:25 GMT  
		Size: 35.1 MB (35142548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4ecaefb151e17955d4f6601aefdca3e6e6adf27c2858a8654f1642b6c5399`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:79ff1827a0fe4f8236b39ea8728144a7d9ad9c20443fab8bcaaa7421d2267ca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40951344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99842a54f239f3e13715141e6cfe726560cd79fee4167a72ff71c25219b5f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:18 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:18 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e08d6b62d3329493d6a6ead807303f1c265143bbda714fdef9382ae8c27a8d`  
		Last Modified: Fri, 29 Sep 2023 00:15:57 GMT  
		Size: 37.1 MB (37113034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7fa0850e9af9b35eca14f9c7eaaf6b8fcc591d1c20fca9d47ecaacb3e1b314`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:dab2b4b52465d429b1bf5b84ffa38c085ea1c00af3121846acd69ab445b4083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:dee2708e034f9398d1df57ca83b286b95a461705193b858a5b845bb5eec8a7b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29344f9d48c4d86ae52a026fbef4ef800a05ecf2a4fe72457d759dd3615d0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:33:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:33:50 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:33:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:33:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761997e52cfb63512b90853905a746fd9fd54e41674e2d4bcbb1cb8201dd8e6`  
		Last Modified: Wed, 13 Sep 2023 08:35:53 GMT  
		Size: 38.9 MB (38911475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68336a56fcbfa87a1c489e6104360ab265abb53897306e3d4b09b6a7649bcc28`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e209029cdcd07d20e5a87b03da02a4e8a0c69006f4837fb0d0eb73571be80d`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7cd492baf3537340fe6d001aa41f13f04e92943dc5fc877ffb6a51926b4db`  
		Last Modified: Wed, 13 Sep 2023 08:35:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:saintmarcelin` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:saintmarcelin-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:v2.10-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.4`

```console
$ docker pull traefik@sha256:de4644233e610132df35dc0fb1c32b34278aec2d748addaa3de885791b13a409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10.4` - linux; amd64

```console
$ docker pull traefik@sha256:57b2516b7549c4f59531bb09311a54a05af237670676529249c3c0b8e58ad0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42384635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae1addee1b2f3bd2ff67edf06e8cf028e1ca44f99a6fbf51dfb0b2eec546949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:36 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:36 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1022d3e6eb6de11e14cfcea2b297e20657615293e82e4c1a28cc6888c3727fc6`  
		Last Modified: Wed, 09 Aug 2023 04:07:16 GMT  
		Size: 38.4 MB (38360374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9401db61432baa70472973f37408025b1240d1762e184bf6ab77f1ea68c85b`  
		Last Modified: Wed, 09 Aug 2023 04:07:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7636441edeadd5f2186db5f8ea8c2b96d2f086892e7c9c99e284e3b19b1f6256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39898270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e73974b343b759948be4635c5599da3c610d3a4ecbebeab61cdf6cc4f5f290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bad430cd8845b6f6a226b53f94c9770261c8d5c5155887c015576759be6a757`  
		Last Modified: Fri, 29 Sep 2023 02:08:53 GMT  
		Size: 36.1 MB (36129895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cc37f0b6ec1cd2a28c2cb1263b58b145220b880095f858b7af4516f249b65`  
		Last Modified: Fri, 29 Sep 2023 02:08:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:17dcbd2b25cbd839e09d2d86930a0c3b11eca59e6df261c4405ef180b6a1245e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39137651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724292bfe7cbfb4eaa6aa242e38929de0b027f52d11394cd83dbcb0bfcc74c67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:09 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:09 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee026b909a25350faab81b6e78c204eaf9cb642b9345649cf4b39c1874569ada`  
		Last Modified: Fri, 29 Sep 2023 02:24:42 GMT  
		Size: 35.2 MB (35180938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8835dc51169f9a4ff4d50f97261b8421d4a283fbce60150403aa663f6ec374`  
		Last Modified: Fri, 29 Sep 2023 02:24:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; s390x

```console
$ docker pull traefik@sha256:755c4c3891db8f6b955c25fe3e19442bd0792ca28459f10fc3005e79776683e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41034756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fb49ad4398f43080e4b15ecb86663f7b9d33fd3394c2dbe5b85a61eea53998`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:33 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:34 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc123c7bae83a141fb0dc9f96de9910cfa54eb022ebb63bc8d191aec93dc97c`  
		Last Modified: Fri, 29 Sep 2023 00:16:13 GMT  
		Size: 37.2 MB (37196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ddc7c72004c2240bdeb82301ae59b70bacbd4aa31b3c18768ba03db4a96b8b`  
		Last Modified: Fri, 29 Sep 2023 00:16:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:v2.10.4-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:aab993a79d3d48c93f3dcd250ac3ef0aeb7b967ad73a317c8459b05ca7b07124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:db21af65fb9edaa04542efe69bb6ba74afa04231874b0240fcccb059547fbf24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42339283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2af65616272cb94e6157ff2c162b2949d831dfe72e5de461e32db2f458951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:28 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:28 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3fb410d5ad92d4b790c3aeff36ea3d4e6d1768c3d58cd9fadb8f574f8eb24a`  
		Last Modified: Wed, 09 Aug 2023 04:06:55 GMT  
		Size: 38.3 MB (38315021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25020b7f93004e310f3a03e903db4f1ba8ae45d9a5b5b3a594da55f18b0bc663`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:27d59eaf0a71f39755d29f3a8c8c7b7201f56d308c5798bd418370c1fcf5f2c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39835276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7abe214da586596b94490448c92c43ba2f265fc92b07be88fa5dc2278d1b01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:00 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:01 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703bd65860e0f9aa5ecded58786f3485cd7d4c971208e85e7b103c0ca67d9a0`  
		Last Modified: Fri, 29 Sep 2023 02:08:29 GMT  
		Size: 36.1 MB (36066901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13805ab706bdd42003ba6a623e50accab2364cd4fa0ff3f301ebb829cfbbea26`  
		Last Modified: Fri, 29 Sep 2023 02:08:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e55409b224d531f08d292ce5a7cb06f780e6d8d3f8c95a8a34ed4d07f38d667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39099261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbd4be29ca7d64655207995ea5252b5b6685dd95ede6bbe93e92a551cb2f59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:03 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:03 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da0a69e79037e30b0819ae2274df20430ea9bad7e4d8c097b1feadb24567ab`  
		Last Modified: Fri, 29 Sep 2023 02:24:25 GMT  
		Size: 35.1 MB (35142548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4ecaefb151e17955d4f6601aefdca3e6e6adf27c2858a8654f1642b6c5399`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:79ff1827a0fe4f8236b39ea8728144a7d9ad9c20443fab8bcaaa7421d2267ca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40951344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99842a54f239f3e13715141e6cfe726560cd79fee4167a72ff71c25219b5f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:18 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:18 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e08d6b62d3329493d6a6ead807303f1c265143bbda714fdef9382ae8c27a8d`  
		Last Modified: Fri, 29 Sep 2023 00:15:57 GMT  
		Size: 37.1 MB (37113034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7fa0850e9af9b35eca14f9c7eaaf6b8fcc591d1c20fca9d47ecaacb3e1b314`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:dab2b4b52465d429b1bf5b84ffa38c085ea1c00af3121846acd69ab445b4083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:dee2708e034f9398d1df57ca83b286b95a461705193b858a5b845bb5eec8a7b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29344f9d48c4d86ae52a026fbef4ef800a05ecf2a4fe72457d759dd3615d0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:33:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:33:50 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:33:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:33:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761997e52cfb63512b90853905a746fd9fd54e41674e2d4bcbb1cb8201dd8e6`  
		Last Modified: Wed, 13 Sep 2023 08:35:53 GMT  
		Size: 38.9 MB (38911475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68336a56fcbfa87a1c489e6104360ab265abb53897306e3d4b09b6a7649bcc28`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e209029cdcd07d20e5a87b03da02a4e8a0c69006f4837fb0d0eb73571be80d`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7cd492baf3537340fe6d001aa41f13f04e92943dc5fc877ffb6a51926b4db`  
		Last Modified: Wed, 13 Sep 2023 08:35:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta3`

```console
$ docker pull traefik@sha256:aab993a79d3d48c93f3dcd250ac3ef0aeb7b967ad73a317c8459b05ca7b07124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0.0-beta3` - linux; amd64

```console
$ docker pull traefik@sha256:db21af65fb9edaa04542efe69bb6ba74afa04231874b0240fcccb059547fbf24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42339283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2af65616272cb94e6157ff2c162b2949d831dfe72e5de461e32db2f458951`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:06:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 09 Aug 2023 04:06:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 09 Aug 2023 04:06:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 09 Aug 2023 04:06:28 GMT
EXPOSE 80
# Wed, 09 Aug 2023 04:06:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 04:06:28 GMT
CMD ["traefik"]
# Wed, 09 Aug 2023 04:06:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af32133391e63d8b260bd5a6dca0e380b088a7c2cfe9b6882dd7567b97bf5c84`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 622.3 KB (622281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3fb410d5ad92d4b790c3aeff36ea3d4e6d1768c3d58cd9fadb8f574f8eb24a`  
		Last Modified: Wed, 09 Aug 2023 04:06:55 GMT  
		Size: 38.3 MB (38315021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25020b7f93004e310f3a03e903db4f1ba8ae45d9a5b5b3a594da55f18b0bc663`  
		Last Modified: Wed, 09 Aug 2023 04:06:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:27d59eaf0a71f39755d29f3a8c8c7b7201f56d308c5798bd418370c1fcf5f2c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39835276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7abe214da586596b94490448c92c43ba2f265fc92b07be88fa5dc2278d1b01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:08:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:08:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:08:00 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:08:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:01 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:08:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b6a121fb4926fc8535cfa17caa1e1cd475fcc89a18cc9ecabe5da99ff5462`  
		Last Modified: Fri, 29 Sep 2023 02:08:23 GMT  
		Size: 622.7 KB (622716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703bd65860e0f9aa5ecded58786f3485cd7d4c971208e85e7b103c0ca67d9a0`  
		Last Modified: Fri, 29 Sep 2023 02:08:29 GMT  
		Size: 36.1 MB (36066901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13805ab706bdd42003ba6a623e50accab2364cd4fa0ff3f301ebb829cfbbea26`  
		Last Modified: Fri, 29 Sep 2023 02:08:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e55409b224d531f08d292ce5a7cb06f780e6d8d3f8c95a8a34ed4d07f38d667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39099261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbd4be29ca7d64655207995ea5252b5b6685dd95ede6bbe93e92a551cb2f59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:23:59 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 02:24:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 02:24:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 02:24:03 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:24:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 02:24:03 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 02:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b59e422640e276d23497c5544f7d98d0d1a6eed46644029a75b232afc0e4dc`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 624.5 KB (624514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da0a69e79037e30b0819ae2274df20430ea9bad7e4d8c097b1feadb24567ab`  
		Last Modified: Fri, 29 Sep 2023 02:24:25 GMT  
		Size: 35.1 MB (35142548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4ecaefb151e17955d4f6601aefdca3e6e6adf27c2858a8654f1642b6c5399`  
		Last Modified: Fri, 29 Sep 2023 02:24:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; s390x

```console
$ docker pull traefik@sha256:79ff1827a0fe4f8236b39ea8728144a7d9ad9c20443fab8bcaaa7421d2267ca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40951344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99842a54f239f3e13715141e6cfe726560cd79fee4167a72ff71c25219b5f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:15:10 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 29 Sep 2023 00:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 29 Sep 2023 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 29 Sep 2023 00:15:18 GMT
EXPOSE 80
# Fri, 29 Sep 2023 00:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 29 Sep 2023 00:15:18 GMT
CMD ["traefik"]
# Fri, 29 Sep 2023 00:15:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af407ac96c8e70e35ccb675ba932c1f6a441da5da4bff25fdfee4b8037205c`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 622.8 KB (622839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e08d6b62d3329493d6a6ead807303f1c265143bbda714fdef9382ae8c27a8d`  
		Last Modified: Fri, 29 Sep 2023 00:15:57 GMT  
		Size: 37.1 MB (37113034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7fa0850e9af9b35eca14f9c7eaaf6b8fcc591d1c20fca9d47ecaacb3e1b314`  
		Last Modified: Fri, 29 Sep 2023 00:15:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:dab2b4b52465d429b1bf5b84ffa38c085ea1c00af3121846acd69ab445b4083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:v3.0.0-beta3-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:dee2708e034f9398d1df57ca83b286b95a461705193b858a5b845bb5eec8a7b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055247019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a29344f9d48c4d86ae52a026fbef4ef800a05ecf2a4fe72457d759dd3615d0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:33:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:33:50 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:33:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:33:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4761997e52cfb63512b90853905a746fd9fd54e41674e2d4bcbb1cb8201dd8e6`  
		Last Modified: Wed, 13 Sep 2023 08:35:53 GMT  
		Size: 38.9 MB (38911475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68336a56fcbfa87a1c489e6104360ab265abb53897306e3d4b09b6a7649bcc28`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e209029cdcd07d20e5a87b03da02a4e8a0c69006f4837fb0d0eb73571be80d`  
		Last Modified: Wed, 13 Sep 2023 08:35:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7cd492baf3537340fe6d001aa41f13f04e92943dc5fc877ffb6a51926b4db`  
		Last Modified: Wed, 13 Sep 2023 08:35:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:8c809f2d7759cb331e6787e80637611f0df573ae584057252a404949d93176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull traefik@sha256:162622cb7682b3e6f3274106c7920c71adb69ea58ca89fa282e2ab7c33275f26
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2055286197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ca8a25a6214a37c560d4a7e85db466ec7af762962f6ebe1350bb0e0ffeb03c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 08:35:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Sep 2023 08:35:19 GMT
EXPOSE 80
# Wed, 13 Sep 2023 08:35:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Sep 2023 08:35:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02f28ba2ad38d851b3d6f506b4a28243717438129c2627a3492d29c08c6d5d`  
		Last Modified: Wed, 13 Sep 2023 08:36:16 GMT  
		Size: 39.0 MB (38950677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf8cada8a7cfe4fa87db7be051abb4ec4a26637f91f6404bfce2664ea81dc64`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528ac6fcf0f3b42b632849e634ea6b05511b961bee203c0f893835f04664e6c`  
		Last Modified: Wed, 13 Sep 2023 08:36:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c7270b3462ca9295dd9a569d4ed3b821aa3f7be16a73d895e3483a3165f5`  
		Last Modified: Wed, 13 Sep 2023 08:36:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
