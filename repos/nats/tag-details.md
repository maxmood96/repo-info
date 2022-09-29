<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.16`](#nats2-alpine316)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.16`](#nats29-alpine316)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.2`](#nats292)
-	[`nats:2.9.2-alpine`](#nats292-alpine)
-	[`nats:2.9.2-alpine3.16`](#nats292-alpine316)
-	[`nats:2.9.2-linux`](#nats292-linux)
-	[`nats:2.9.2-nanoserver`](#nats292-nanoserver)
-	[`nats:2.9.2-nanoserver-1809`](#nats292-nanoserver-1809)
-	[`nats:2.9.2-scratch`](#nats292-scratch)
-	[`nats:2.9.2-windowsservercore`](#nats292-windowsservercore)
-	[`nats:2.9.2-windowsservercore-1809`](#nats292-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.16`](#natsalpine316)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:7d0483b6be62ec431b425e56be704aeba0bfffa905d4b7e0b59b687ef7926665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3406; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.16`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:7d0483b6be62ec431b425e56be704aeba0bfffa905d4b7e0b59b687ef7926665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.16`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.2`

**does not exist** (yet?)

## `nats:2.9.2-alpine`

**does not exist** (yet?)

## `nats:2.9.2-alpine3.16`

**does not exist** (yet?)

## `nats:2.9.2-linux`

**does not exist** (yet?)

## `nats:2.9.2-nanoserver`

**does not exist** (yet?)

## `nats:2.9.2-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.9.2-scratch`

**does not exist** (yet?)

## `nats:2.9.2-windowsservercore`

**does not exist** (yet?)

## `nats:2.9.2-windowsservercore-1809`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.16`

```console
$ docker pull nats@sha256:53a519acb4f4e870507e1ae9d8cb7c05048b7886b1b44c872ff2b495182b7db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:37f1d066c049004d7933c5a4a060d096c2730528e68139573a43662fe78ec3d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836273ce99f17db3786cc6e7f7cb950b3afa89f58cf570739571044bed9a12b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:26:56 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:26:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 23 Sep 2022 00:26:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 23 Sep 2022 00:26:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 23 Sep 2022 00:26:59 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:26:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:26:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018f9439fee40c13a8c9d22440de2fe7aca8e34649c1ef518dff4fa59f326fbe`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 5.2 MB (5188460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbe04166b885e99b37c3dc4137c080351a40098f78a2b57ebe293a7871712f`  
		Last Modified: Fri, 23 Sep 2022 00:27:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdbbe65a686fff6110ff20b903e32164414b3f19be1b919a6ad297bcaa25ed5`  
		Last Modified: Fri, 23 Sep 2022 00:27:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:7d0483b6be62ec431b425e56be704aeba0bfffa905d4b7e0b59b687ef7926665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3406; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:bf993f74acbb61d1950713b6320e04f564081174971dcd14de48c8485a082bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:21af3bca28b8098feaca472b95d08826bc01c6f9eec22e0dc47188b147aa37b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f69f1c0c080fddd7a6d67355e5a038b3ff517b41b25bbcbfac4443eca4f44b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:f89708d3323159716590cff84cd205e99e67cfa41e46db6298f326785cd609a0 in /nats-server 
# Fri, 23 Sep 2022 00:27:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 23 Sep 2022 00:27:06 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 23 Sep 2022 00:27:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 23 Sep 2022 00:27:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:df84418648c136b8dd1539d7bbd5f9a7638b3593d4bf8e1a57f04f0409beb0bd`  
		Last Modified: Fri, 23 Sep 2022 00:27:56 GMT  
		Size: 4.9 MB (4905938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4590e101d8fa2186039733995a70f977bc0d9c6b5e49898eeb698a5c0d8573b`  
		Last Modified: Fri, 23 Sep 2022 00:27:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f9c6f9abbead4a684c7b883f4a7452710aa092d1ed595ba0dbd6179372d0be63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b361f078e342fdb327cb4f5b2914d500fb5670e8424ba7dc9f20ffb4fff3c68`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:945dfac8719ced982d1230b42c4e21c20cfe1792458759d37bd8f34702b97d49 in /nats-server 
# Thu, 22 Sep 2022 23:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:49:35 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de6a34af6a596d1c7b7537e42748d9178faf87b637f714573303791154838994`  
		Last Modified: Thu, 22 Sep 2022 23:51:04 GMT  
		Size: 4.7 MB (4668293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d5a0f70821a3f8fc7b8b1111c2166c03c48d05ebc9ce0473931d1ca74a09b`  
		Last Modified: Thu, 22 Sep 2022 23:51:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:03a39590b94ba73f75c39970947a3ff276c7f37d7e6e8009ccf780251f6cbc81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4660097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ae12fca7c133fb2e99616ac3d87777680804b3654472e9c4d78d28db4e965`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:8333f5a10c97b92118357725370604074ebcfef54b0d6e7d818b8a5280ac8fee in /nats-server 
# Thu, 22 Sep 2022 23:58:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:58:10 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:58:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:131d7d99719c2d3afa300226a95a811f986eb26f05d0aa3bd08fda92824f90a7`  
		Last Modified: Thu, 22 Sep 2022 23:59:35 GMT  
		Size: 4.7 MB (4659588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b4198acf76381af038bfd14e9332c1ccd3a7235889f327c2d387fbd44b1b3`  
		Last Modified: Thu, 22 Sep 2022 23:59:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:080acc4ece31f7fc871e35471f286e4991b8febfe1379f1fb6b1e0d6eac551ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3fd2d5a277619c0411f028a92dd0e001aaf241be51e3bfc66db595c651f32`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 Sep 2022 23:40:22 GMT
COPY file:78383a44c18e587e522cc9799431581c891b0ef3afdf06dee4c7f7267ca8bde9 in /nats-server 
# Thu, 22 Sep 2022 23:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 22 Sep 2022 23:40:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 Sep 2022 23:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 Sep 2022 23:40:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3708e85fb8eb51ba8efd3211608a7049a9714a9f0f6282c1d78fb3efc99abed8`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 4.5 MB (4493908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57fd3c887f07b3980dd16bfc149abfd66ce3cba86f7e877dfa055492cba071`  
		Last Modified: Thu, 22 Sep 2022 23:41:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:4a5f0f1338dd824bb02f9bf3627e488c36d0268c80e776a09d7b53c49a70fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:393de0155c0b6f8de5477aef648f43ea93641702f13c1cda2639f2e5e1985f63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709242447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20de7c7ffd122e1ddbac2ad4894d5001d89c75b5710e278ffb31e9e5b5cfa7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:25:06 GMT
ENV NATS_SERVER=2.9.1
# Fri, 23 Sep 2022 00:25:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.1/nats-server-v2.9.1-windows-amd64.zip
# Fri, 23 Sep 2022 00:25:08 GMT
ENV NATS_SERVER_SHASUM=46f5bff3c4dab610b2933b1a54d65d032069a4807ec4b79b547597b777c0e43b
# Fri, 23 Sep 2022 00:26:14 GMT
RUN Set-PSDebug -Trace 2
# Fri, 23 Sep 2022 00:27:35 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 23 Sep 2022 00:27:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:36 GMT
EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:37 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fd9807aae2fa3228c120563ccfa3b0b180f2606914491980034b3ec5f9dc1`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cc7a7f304305120c33226ad2c62076802a6c96f616046a36bd392500e9a5`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b78b9a895606af70b1d5f0d236f81fbbf1d998c354a92518256b52f36c4bb3`  
		Last Modified: Fri, 23 Sep 2022 00:28:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29770dcc1ab3d0431d9750b92bddacb1a525b10dc3b229ab8da585c24d19a5b`  
		Last Modified: Fri, 23 Sep 2022 00:28:24 GMT  
		Size: 358.0 KB (357972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ea6c8f4811d3ff1fb0d304b3f30af6e5f4f1db8fe74eed89f437faa465d5db`  
		Last Modified: Fri, 23 Sep 2022 00:28:22 GMT  
		Size: 5.3 MB (5306475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9675650ccb8db40e25a12ddd87abadda091761d36c3a4503bf18163652783e`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6270e6e25572e4aded2a135d3fde6f7ee84c8872e190c87de5d1a935cc7102`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d131b037aa2273b7d6f1b8007a30e3162d75cfbc57e066926dd7b5318be8b2`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980fcd1a6610a968940facba09e0729d6d6ad1b6e8fed26c1f314461be93c04`  
		Last Modified: Fri, 23 Sep 2022 00:28:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
