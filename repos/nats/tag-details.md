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
-	[`nats:2.9.1`](#nats291)
-	[`nats:2.9.1-alpine`](#nats291-alpine)
-	[`nats:2.9.1-alpine3.16`](#nats291-alpine316)
-	[`nats:2.9.1-linux`](#nats291-linux)
-	[`nats:2.9.1-nanoserver`](#nats291-nanoserver)
-	[`nats:2.9.1-nanoserver-1809`](#nats291-nanoserver-1809)
-	[`nats:2.9.1-scratch`](#nats291-scratch)
-	[`nats:2.9.1-windowsservercore`](#nats291-windowsservercore)
-	[`nats:2.9.1-windowsservercore-1809`](#nats291-windowsservercore-1809)
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
$ docker pull nats@sha256:670c9c3c6577e49df518d30c358b888a265ae155e9e2e8c229be0eb26077bc79
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
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:670c9c3c6577e49df518d30c358b888a265ae155e9e2e8c229be0eb26077bc79
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
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.1`

```console
$ docker pull nats@sha256:71ff84166c6771fef15bee0b39f3305a17f497084ad6384c6704f228701e5bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.1` - linux; arm variant v6

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

### `nats:2.9.1` - linux; arm variant v7

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

### `nats:2.9.1` - linux; arm64 variant v8

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

## `nats:2.9.1-alpine`

```console
$ docker pull nats@sha256:206db47e7a4f9982d1678638548acd36a73ca3219c1282244e1101c8d2972781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.1-alpine` - linux; arm variant v6

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

### `nats:2.9.1-alpine` - linux; arm variant v7

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

### `nats:2.9.1-alpine` - linux; arm64 variant v8

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

## `nats:2.9.1-alpine3.16`

```console
$ docker pull nats@sha256:206db47e7a4f9982d1678638548acd36a73ca3219c1282244e1101c8d2972781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.1-alpine3.16` - linux; arm variant v6

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

### `nats:2.9.1-alpine3.16` - linux; arm variant v7

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

### `nats:2.9.1-alpine3.16` - linux; arm64 variant v8

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

## `nats:2.9.1-linux`

```console
$ docker pull nats@sha256:71ff84166c6771fef15bee0b39f3305a17f497084ad6384c6704f228701e5bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.1-linux` - linux; arm variant v6

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

### `nats:2.9.1-linux` - linux; arm variant v7

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

### `nats:2.9.1-linux` - linux; arm64 variant v8

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

## `nats:2.9.1-nanoserver`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.9.1-nanoserver-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.9.1-scratch`

```console
$ docker pull nats@sha256:71ff84166c6771fef15bee0b39f3305a17f497084ad6384c6704f228701e5bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.1-scratch` - linux; arm variant v6

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

### `nats:2.9.1-scratch` - linux; arm variant v7

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

### `nats:2.9.1-scratch` - linux; arm64 variant v8

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

## `nats:2.9.1-windowsservercore`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:2.9.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `nats:alpine`

```console
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:670c9c3c6577e49df518d30c358b888a265ae155e9e2e8c229be0eb26077bc79
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
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:cd72550bc0dc297ac0d40dc272ab9bc9cba7d2b51aa4ea87af8a8ceb00af4b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:5f52c2aec4c9f9a92ae1e8e805a2ded0c1d8707d78b83f8fdf5c4a347716d1b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108295170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30633d2cd44487d17f0c39e152e8b6dd7ae7365e88fcba7fafc7dda07775eeb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:58259134bc4aec3b0bb4a01151c496cd2e557bf985d41d1838cb10c3492958d3 in C:\nats-server.exe 
# Wed, 14 Sep 2022 15:41:38 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:41 GMT
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
	-	`sha256:379f80368def8337624f5e8a84b520751678f207da4a626cdf50cf3d7392f04c`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 5.0 MB (4954549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acc7fb6dac7daaf12ea799fabe64082aa832976b80fee0dee151e228715c9d1`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3594ed92c60a9025482778f60a98c08bdb781c381811612ab20748b21a5430`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6012bd45501ace7b93d72b0d441a60aac54f5890ade1c8c669469a1adb820a`  
		Last Modified: Wed, 14 Sep 2022 15:42:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e87860897c14f00959ece616cd0716df15e5d22fdfe25eeb2d1c15f80b162a`  
		Last Modified: Wed, 14 Sep 2022 15:42:29 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4da96b2fa5da16b6660f43092d49bd57ffff27e46e1a761eb1522709e0f7bd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:1e1cc1b80a618a109970e841dfa2962318c7348441312b0b7e8f6e64b8eb812f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe06e372ca40928fec9bf0cb9cf9751265f2ea179229b34abf54b42ec3612b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:cd9de75b794fafb19e20bcd172a0323670b10f2af792997a2f16906c4bf3fcc3 in /nats-server 
# Mon, 12 Sep 2022 19:32:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 12 Sep 2022 19:32:21 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:32:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 12 Sep 2022 19:32:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 12 Sep 2022 19:32:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae176e6d0980e9d32d62aab8bce6ee604abd3d7934666cf81bffbdc646275ce1`  
		Last Modified: Mon, 12 Sep 2022 19:33:13 GMT  
		Size: 4.9 MB (4905124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d318ae137e300d4cdce8f1358c0992a66798618c91487a34d8cd6f2d49b220`  
		Last Modified: Mon, 12 Sep 2022 19:33:12 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:94c4431384fa8d72953702c4803d8692b7940d5b90631d189cc55bd20e19de3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:247e0809b6ab5c2c0ac1a2f6ba499573e0630dbd17e322b54f9f7033286088a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709200380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e482f58c884b0b5c9d1eea48f09911122bd3727cf676095384e1593ed6061`
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
# Wed, 14 Sep 2022 15:38:55 GMT
ENV NATS_SERVER=2.9.0
# Wed, 14 Sep 2022 15:38:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.0/nats-server-v2.9.0-windows-amd64.zip
# Wed, 14 Sep 2022 15:38:57 GMT
ENV NATS_SERVER_SHASUM=7bd8f5e4940b67e34cffddbaad058f1d2af1c3bd326dd2879528a6cb72c6a4ac
# Wed, 14 Sep 2022 15:39:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 15:41:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 15:41:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Sep 2022 15:41:21 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Sep 2022 15:41:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Sep 2022 15:41:23 GMT
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
	-	`sha256:f24a2cf651f4ba8c7857f4abdb11810571b36e5defe102bee53ef3c2e4080730`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a39faa2e15c1ea78426e4615b1b98479d61b70aefd276dc25fb7262bc6b5c0b`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71612a4f8d75c46739e99bdf8549ed87e64006880b140c488f5e6cc51f52bd8`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080572f54100805a4bc7bbddd88363bdbcc67f643d325f93bd923cccd60bb66`  
		Last Modified: Wed, 14 Sep 2022 15:42:10 GMT  
		Size: 342.7 KB (342708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74120e9e948ab17f47c3ec2418efb319f7fe7f6d56fd5e3c7ba35c55856fa529`  
		Last Modified: Wed, 14 Sep 2022 15:42:09 GMT  
		Size: 5.3 MB (5279641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7995db94a679a620571d1ea0efd91fedbffddbdd6c90753bd49d886e17f4e80`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b90892bbe4dc980bbdba1a6bddeaa2fe6658454f71909bb9e3bb6897f8298e`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b251925786cd770d698e76d0ee0639bd17ad5a9a970281040ec8179e1dd2ed`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817cd2f546e7b14811902d0ca5d07192f32e6b69afdf1702347cfd781aec5592`  
		Last Modified: Wed, 14 Sep 2022 15:42:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
