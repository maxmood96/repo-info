<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.11`](#nats21011)
-	[`nats:2.10.11-alpine`](#nats21011-alpine)
-	[`nats:2.10.11-alpine3.19`](#nats21011-alpine319)
-	[`nats:2.10.11-linux`](#nats21011-linux)
-	[`nats:2.10.11-nanoserver`](#nats21011-nanoserver)
-	[`nats:2.10.11-nanoserver-1809`](#nats21011-nanoserver-1809)
-	[`nats:2.10.11-scratch`](#nats21011-scratch)
-	[`nats:2.10.11-windowsservercore`](#nats21011-windowsservercore)
-	[`nats:2.10.11-windowsservercore-1809`](#nats21011-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.24`](#nats2924)
-	[`nats:2.9.24-alpine`](#nats2924-alpine)
-	[`nats:2.9.24-alpine3.18`](#nats2924-alpine318)
-	[`nats:2.9.24-linux`](#nats2924-linux)
-	[`nats:2.9.24-nanoserver`](#nats2924-nanoserver)
-	[`nats:2.9.24-nanoserver-1809`](#nats2924-nanoserver-1809)
-	[`nats:2.9.24-scratch`](#nats2924-scratch)
-	[`nats:2.9.24-windowsservercore`](#nats2924-windowsservercore)
-	[`nats:2.9.24-windowsservercore-1809`](#nats2924-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:aad5db2524532795e54e1cff7c5e068566fdb8af08924f8b9e7171c5b6e87ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5458; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:aad5db2524532795e54e1cff7c5e068566fdb8af08924f8b9e7171c5b6e87ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11`

```console
$ docker pull nats@sha256:aad5db2524532795e54e1cff7c5e068566fdb8af08924f8b9e7171c5b6e87ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10.11` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-alpine`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-alpine3.19`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.11-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-linux`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-nanoserver`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10.11-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-nanoserver-1809`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10.11-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-scratch`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-windowsservercore`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10.11-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.10.11-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:4490fa17144b62543fc595d2e15fad40e30904475e9919acdb1aaa963412f547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:c8d58e5e6a4fa6042c8d9bfc995b8bc18bebb99d5d24ddc1ca7cb1f1d7d710b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812b43c7c39dda5f7867b4b80e59f129c04967a7fe956b09649bc4f8436dc8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:10:26 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678037ca9276d32f9575791dad3984043c04a43fc4048ff8454991cb0440308f`  
		Last Modified: Wed, 14 Feb 2024 21:11:41 GMT  
		Size: 5.3 MB (5328954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43280c2f4dac85046944642c6758423c2b7557bf7cbb8ab6ac69382023db79`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f190901347fcbd064192187317e964e2c63c323677138f068aca78626ef75d2`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6650a4744bd074e2bad658c28d84a16a8d9c0223b9cac2101dd070066f278`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706827ac240d7afe4dc966969b272326179254bfcd86d0cd2e42b33fd38bfa64`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:4490fa17144b62543fc595d2e15fad40e30904475e9919acdb1aaa963412f547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:c8d58e5e6a4fa6042c8d9bfc995b8bc18bebb99d5d24ddc1ca7cb1f1d7d710b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812b43c7c39dda5f7867b4b80e59f129c04967a7fe956b09649bc4f8436dc8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:10:26 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678037ca9276d32f9575791dad3984043c04a43fc4048ff8454991cb0440308f`  
		Last Modified: Wed, 14 Feb 2024 21:11:41 GMT  
		Size: 5.3 MB (5328954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43280c2f4dac85046944642c6758423c2b7557bf7cbb8ab6ac69382023db79`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f190901347fcbd064192187317e964e2c63c323677138f068aca78626ef75d2`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6650a4744bd074e2bad658c28d84a16a8d9c0223b9cac2101dd070066f278`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706827ac240d7afe4dc966969b272326179254bfcd86d0cd2e42b33fd38bfa64`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:d8ec739d6e52271e322912359932249827f5acc4d566b39765246a418e118729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:aa18c67f8803247760db9d23e70b50104950ce9b83c6ef962f7613826aeff38c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086538318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667258577115055f809c994abb0fc31d4e35584e6c5e7318871491147e2ae4bc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER=2.9.24
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 14 Feb 2024 21:06:58 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 14 Feb 2024 21:08:18 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:10:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:10:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:10 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157b436181b4ba746d825eebfd966c02dfe05101fa5e05114927859e2cc23c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d1abfaa7ed221ce27358d543622db3b87d1a7609429a92c71235e297197bee`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b728fa4971dd04a7ea76de35a068e854ee90c8b5ad3d8692fbef58e64c60e6`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f657fbfb1d838a6112dc552dff7e8bfce717abc45d4591bf893b1e86816ce`  
		Last Modified: Wed, 14 Feb 2024 21:11:31 GMT  
		Size: 454.7 KB (454707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2beaed384996d1322791d3c44490d7cf06272975e8c3450739535b4a42aa1c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 5.6 MB (5621831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8451e8bd1aa6c595bd6a45e3ee5e44a1d75b7f8b3846dcc6e2aeafc6fc5036`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb595d5dedc4ac6c60fc4825cb448bdbdd013d04a6242ccc00ded4aa994190`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ec1c7b30bdb2048266617b0e6909887e0f0a4a2972ba930e76722d27328bc`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e8a57365a12a6516390f897ece81693600165e4facea75e48c432f5a64663`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:d8ec739d6e52271e322912359932249827f5acc4d566b39765246a418e118729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:aa18c67f8803247760db9d23e70b50104950ce9b83c6ef962f7613826aeff38c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086538318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667258577115055f809c994abb0fc31d4e35584e6c5e7318871491147e2ae4bc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER=2.9.24
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 14 Feb 2024 21:06:58 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 14 Feb 2024 21:08:18 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:10:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:10:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:10 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157b436181b4ba746d825eebfd966c02dfe05101fa5e05114927859e2cc23c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d1abfaa7ed221ce27358d543622db3b87d1a7609429a92c71235e297197bee`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b728fa4971dd04a7ea76de35a068e854ee90c8b5ad3d8692fbef58e64c60e6`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f657fbfb1d838a6112dc552dff7e8bfce717abc45d4591bf893b1e86816ce`  
		Last Modified: Wed, 14 Feb 2024 21:11:31 GMT  
		Size: 454.7 KB (454707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2beaed384996d1322791d3c44490d7cf06272975e8c3450739535b4a42aa1c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 5.6 MB (5621831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8451e8bd1aa6c595bd6a45e3ee5e44a1d75b7f8b3846dcc6e2aeafc6fc5036`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb595d5dedc4ac6c60fc4825cb448bdbdd013d04a6242ccc00ded4aa994190`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ec1c7b30bdb2048266617b0e6909887e0f0a4a2972ba930e76722d27328bc`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e8a57365a12a6516390f897ece81693600165e4facea75e48c432f5a64663`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine3.18`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-linux` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver`

```console
$ docker pull nats@sha256:4490fa17144b62543fc595d2e15fad40e30904475e9919acdb1aaa963412f547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9.24-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:c8d58e5e6a4fa6042c8d9bfc995b8bc18bebb99d5d24ddc1ca7cb1f1d7d710b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812b43c7c39dda5f7867b4b80e59f129c04967a7fe956b09649bc4f8436dc8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:10:26 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678037ca9276d32f9575791dad3984043c04a43fc4048ff8454991cb0440308f`  
		Last Modified: Wed, 14 Feb 2024 21:11:41 GMT  
		Size: 5.3 MB (5328954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43280c2f4dac85046944642c6758423c2b7557bf7cbb8ab6ac69382023db79`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f190901347fcbd064192187317e964e2c63c323677138f068aca78626ef75d2`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6650a4744bd074e2bad658c28d84a16a8d9c0223b9cac2101dd070066f278`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706827ac240d7afe4dc966969b272326179254bfcd86d0cd2e42b33fd38bfa64`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver-1809`

```console
$ docker pull nats@sha256:4490fa17144b62543fc595d2e15fad40e30904475e9919acdb1aaa963412f547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9.24-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:c8d58e5e6a4fa6042c8d9bfc995b8bc18bebb99d5d24ddc1ca7cb1f1d7d710b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812b43c7c39dda5f7867b4b80e59f129c04967a7fe956b09649bc4f8436dc8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:10:26 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678037ca9276d32f9575791dad3984043c04a43fc4048ff8454991cb0440308f`  
		Last Modified: Wed, 14 Feb 2024 21:11:41 GMT  
		Size: 5.3 MB (5328954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43280c2f4dac85046944642c6758423c2b7557bf7cbb8ab6ac69382023db79`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f190901347fcbd064192187317e964e2c63c323677138f068aca78626ef75d2`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a6650a4744bd074e2bad658c28d84a16a8d9c0223b9cac2101dd070066f278`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706827ac240d7afe4dc966969b272326179254bfcd86d0cd2e42b33fd38bfa64`  
		Last Modified: Wed, 14 Feb 2024 21:11:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore`

```console
$ docker pull nats@sha256:d8ec739d6e52271e322912359932249827f5acc4d566b39765246a418e118729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9.24-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:aa18c67f8803247760db9d23e70b50104950ce9b83c6ef962f7613826aeff38c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086538318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667258577115055f809c994abb0fc31d4e35584e6c5e7318871491147e2ae4bc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER=2.9.24
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 14 Feb 2024 21:06:58 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 14 Feb 2024 21:08:18 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:10:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:10:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:10 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157b436181b4ba746d825eebfd966c02dfe05101fa5e05114927859e2cc23c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d1abfaa7ed221ce27358d543622db3b87d1a7609429a92c71235e297197bee`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b728fa4971dd04a7ea76de35a068e854ee90c8b5ad3d8692fbef58e64c60e6`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f657fbfb1d838a6112dc552dff7e8bfce717abc45d4591bf893b1e86816ce`  
		Last Modified: Wed, 14 Feb 2024 21:11:31 GMT  
		Size: 454.7 KB (454707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2beaed384996d1322791d3c44490d7cf06272975e8c3450739535b4a42aa1c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 5.6 MB (5621831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8451e8bd1aa6c595bd6a45e3ee5e44a1d75b7f8b3846dcc6e2aeafc6fc5036`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb595d5dedc4ac6c60fc4825cb448bdbdd013d04a6242ccc00ded4aa994190`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ec1c7b30bdb2048266617b0e6909887e0f0a4a2972ba930e76722d27328bc`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e8a57365a12a6516390f897ece81693600165e4facea75e48c432f5a64663`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:d8ec739d6e52271e322912359932249827f5acc4d566b39765246a418e118729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:2.9.24-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:aa18c67f8803247760db9d23e70b50104950ce9b83c6ef962f7613826aeff38c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086538318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667258577115055f809c994abb0fc31d4e35584e6c5e7318871491147e2ae4bc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER=2.9.24
# Wed, 14 Feb 2024 21:06:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 14 Feb 2024 21:06:58 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 14 Feb 2024 21:08:18 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:10:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:10:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Feb 2024 21:10:10 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Feb 2024 21:10:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Feb 2024 21:10:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b157b436181b4ba746d825eebfd966c02dfe05101fa5e05114927859e2cc23c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d1abfaa7ed221ce27358d543622db3b87d1a7609429a92c71235e297197bee`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b728fa4971dd04a7ea76de35a068e854ee90c8b5ad3d8692fbef58e64c60e6`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f657fbfb1d838a6112dc552dff7e8bfce717abc45d4591bf893b1e86816ce`  
		Last Modified: Wed, 14 Feb 2024 21:11:31 GMT  
		Size: 454.7 KB (454707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2beaed384996d1322791d3c44490d7cf06272975e8c3450739535b4a42aa1c`  
		Last Modified: Wed, 14 Feb 2024 21:11:30 GMT  
		Size: 5.6 MB (5621831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8451e8bd1aa6c595bd6a45e3ee5e44a1d75b7f8b3846dcc6e2aeafc6fc5036`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb595d5dedc4ac6c60fc4825cb448bdbdd013d04a6242ccc00ded4aa994190`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858ec1c7b30bdb2048266617b0e6909887e0f0a4a2972ba930e76722d27328bc`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e8a57365a12a6516390f897ece81693600165e4facea75e48c432f5a64663`  
		Last Modified: Wed, 14 Feb 2024 21:11:28 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:e523869cc4238048638fcc326ed4c9164d87fd880f07996007065c5bd81b14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:a67153aef90c4b154424d9606e7cd20ad78dc70e8ec4e55cc5ad04c70d59be35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9043429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfef57a496f1733409fca9adb2daa9f33d8c26622a494db024b289034dd40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:49:22 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:49:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:49:27 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:49:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c9e6ef5dcfa6bb23a9545de95206f12664e53bb692cf8a5d315be175f45d9d`  
		Last Modified: Fri, 16 Feb 2024 19:50:01 GMT  
		Size: 5.9 MB (5877032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a61358cefa908599a325b56e2e0745eda72cfad44d93505d23ebbf810437a09`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b4b3d8073544a88684878183da3541742f04271b1b94878c7cb51d5050fc0`  
		Last Modified: Fri, 16 Feb 2024 19:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:29d5c5a409bedc33c94722d6cb52e369b4f14b81b161e9c26413db874c776901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8788276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e754822985a359deeba5c92170a135a8d584ebd85ea1230218a80528aaeaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:08:53 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:08:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:08:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:08:56 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:08:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4654d41f79bca7556a6f1afcffdd18d1e53a702aec9324f4d5360b589fa11`  
		Last Modified: Fri, 16 Feb 2024 19:09:45 GMT  
		Size: 5.9 MB (5868377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9ae657cea6c841b6825c1b89390462dec3c16218030236abb82bdb8ca8b1f`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a1426d7f4321aed65641c6a44f5dfb21a7b4c15235c8d219e2709a79994cf`  
		Last Modified: Fri, 16 Feb 2024 19:09:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c37d4af1c76294bbb082fa4d9b5cc02459d90232d97bf71c9a941e23442cd83a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c89131566b5805663df29cdd6d8be7b09bf7c8d2f64e8eb5caa62c646409bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:09:25 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:09:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:09:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:09:28 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:09:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70507d2ea422ddeb72a230443c1d5a3d4dbf786c25773691f8b4251e242c3b`  
		Last Modified: Fri, 16 Feb 2024 20:10:26 GMT  
		Size: 5.7 MB (5733282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b81c70a8f72ad8657f93e02003e92ca0461000a46c089801735c5dfabdba7`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1d0a412a6d1f2c501c09f2b93b701fa047219a5860c673d776ea7df73fb7d9`  
		Last Modified: Fri, 16 Feb 2024 20:10:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:056c6b6400ab7abefca27304710af5f00a01667195e37868876472780cdffa93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f0ab6b89137cd912e7f13739b6e1450395520345e72ee3ab72912830edc270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 19:24:14 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:24:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 19:24:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 19:24:19 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 19:24:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580e3207eaf49447dce6dae3506cf67acfe2234620439750becbb5cecb888bb`  
		Last Modified: Fri, 16 Feb 2024 19:25:17 GMT  
		Size: 5.7 MB (5715132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346add3822ef0d69798ebe87fe12d0e687dd5a62eef000fb587fb6c88ed47a2`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc119f2c1466b9e539e8bdc3c34d404597d09be783ba1e9ef764ddbfa0c70e`  
		Last Modified: Fri, 16 Feb 2024 19:25:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:1a300bf200f11925879202d289f191526b37bef9955b0bb02e1fd10654a30263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02cf0771d1602df7d8025eb4352ce177c81da5a190e9595f78a153432440943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:20:37 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:20:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:20:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:20:40 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:20:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354613a419040d670196afaa302e5b41f3e577de7fc5e193a9218be225af8cda`  
		Last Modified: Fri, 16 Feb 2024 20:23:41 GMT  
		Size: 6.0 MB (6045190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e5693ad7ca3a12db6f7f11abe67bec45724d3ccd0289b40a020da06421dfe`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b416c01926f7fd83d42969535884689283a41b6f78ea54bbab9fb7a4c4b2b9`  
		Last Modified: Fri, 16 Feb 2024 20:23:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:aad5db2524532795e54e1cff7c5e068566fdb8af08924f8b9e7171c5b6e87ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5458; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:8da233a87a5baa2c4b8497f68343d9204826c58790b6b544572ed977957b1317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:cecb2ef293a05b2941e770b445cd8aad5faae07549977c7b5b730623f30f93ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110284960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6fef5c6489fa071aa9e74e48770153340bc45dbba0ff17b3ce6bfc5b1002b1`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:19:19 GMT
RUN cmd /S /C #(nop) COPY file:17da01e26a709feb763e87098db6a192af1afdd8e2d3fd606d93f9e1d043cac1 in C:\nats-server.exe 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:19:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:19:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:19:22 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75719de655fc7bc60f5784c4783e541d05dc105e2479c9470b5b2f62a908342e`  
		Last Modified: Fri, 16 Feb 2024 19:20:25 GMT  
		Size: 5.7 MB (5657038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b16c9ab252b99256ef4baa4314870b948f00b04e7f2735a221661320c1d39`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e528e541ed3ce846c412ed3760d20b2313b5577cff4a6fadf6eefd4f49781ab`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc328aff22effbac672e8f399953e95b698eb198086dec996a4b13f9e15ebf9b`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8dc55369403c1a99de3fdfd38eabb0c412068367e122eea0fae7880d55f382`  
		Last Modified: Fri, 16 Feb 2024 19:20:24 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4ecfc16ad47cc30d2ce83409789473b35365bba207bfa877744200ef80bce081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:836dfda9b861098aa3a10f43524c9f7de3a45b43a6b563dcfe550b67cc8eb1ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0107b98f05b94da476196265a9ffae03fa4936ace58eb5a70df6fa67b698747`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:30d66f5adb9fef3137dcbae1682605e373860c59737712279731fce1cac46b25 in /nats-server 
# Fri, 16 Feb 2024 20:02:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:02:41 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:42 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:02:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e67ae684ddf1551d61a7143ea4eb5824c9886d0c5f91e622834b5b02306381b4`  
		Last Modified: Fri, 16 Feb 2024 20:03:38 GMT  
		Size: 5.5 MB (5541357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cccdee486e921711daea58262ce1fab32173fedaa2e53c8e8860130faf3713`  
		Last Modified: Fri, 16 Feb 2024 20:03:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:fbd4eab441c45cea987cf9f29e12c33faa457f3d364ecc56b03b6b7ebbca5ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b107d48d28c1d9d9700b128da87f75cf4247421e4361af6f35f36e74316b6ff`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:d00eacc08bb28af76e55dc3bcec6331f127a182ab378dca30e172d23dcfd6b23 in /nats-server 
# Fri, 16 Feb 2024 19:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:49:33 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d34cf88026351f89492d976b5cb791d43119dc84c6a98784f6b95962e976ad57`  
		Last Modified: Fri, 16 Feb 2024 19:50:23 GMT  
		Size: 5.3 MB (5254704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a9fa0d65669267ba30c759897588b28cc253cf5ddaf893999e8e66e8d586f`  
		Last Modified: Fri, 16 Feb 2024 19:50:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:833d30ce97094761a3e962ece74fe42be34ac8471805f024c51439d4a4b6eb78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c52a7ac9b9efba9a4321f9d5210c33819c1878e84f7a86bf803830c486f2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:0327e3d021fd59aa545e6e7126e24d8f764bd40a6e1f4cba821892b75ad124bd in /nats-server 
# Fri, 16 Feb 2024 19:09:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:09:14 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55c72f0449f3c0c5bd54d68aca7bec5b0e9636421e32236294e4ee8e25b27135`  
		Last Modified: Fri, 16 Feb 2024 19:10:06 GMT  
		Size: 5.2 MB (5247731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d9a0cf2b6f91db4e2227eb79dedea91893ae65bd7f27fe128e30cbe680382a`  
		Last Modified: Fri, 16 Feb 2024 19:10:05 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:83fc63ee7bad2f5b70c7a7e72457e7980e837ea0548bd5adaf1478256e66f0d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5111585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56e598853fbc23869971ecd70ab0f1a2621d334c5c2eb57b8a944182038719`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:264f6b4cc66828ff14ec378dda18ed5062eb2d2efdc295b010a09a1c75c05b6d in /nats-server 
# Fri, 16 Feb 2024 20:10:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:10:00 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:10:00 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:10:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cc4022d0c8b45e31b6fb9ab744707b55aa54ed2d67ebf2673c3ed4253f289733`  
		Last Modified: Fri, 16 Feb 2024 20:10:47 GMT  
		Size: 5.1 MB (5111077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7810b0de7cae445c03ddca9a38e1d8557ee6653cbe298738b4fcb2e3510d95`  
		Last Modified: Fri, 16 Feb 2024 20:10:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:8deff4e480b8590277f1af54ee464fcb9042467c9aa30e9af5bbf59ff37bd215
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653f4bfa43e6b2ea050e4d35170c864c19f8659861f0bd54ea963b43bcbdcf0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:f0bce5137f828975cd36ffd56265614b7b448a3c505c33229c06bd523f9a5c8d in /nats-server 
# Fri, 16 Feb 2024 19:24:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 19:24:55 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:24:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 19:24:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:463a66e2cf46637df677a6dc10ec624d85b65321a7b7e75b861c9b8a2a855827`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 5.1 MB (5092498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc281f0bf387147798a91ea71203bb17dc206d43b3882293f5f497caedf6df`  
		Last Modified: Fri, 16 Feb 2024 19:25:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b1f6ae75884499fea49cb2fcd4b018ebb8104cb065b60ba8fe73bf68655b14b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a8e8dcaf62c26f383f87b965ef85b431caeee70938acc1bf21145584d0a82`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:3ce1b7fce326319b55b8a34035aba04fcc5edd9d2a7adc184e31ed909df6e514 in /nats-server 
# Fri, 16 Feb 2024 20:22:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 16 Feb 2024 20:22:10 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:22:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 16 Feb 2024 20:22:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3caa5d1c7f4630defc42ab23d52cc010f0948d1862e6a9afeb4af5b3d64dbc29`  
		Last Modified: Fri, 16 Feb 2024 20:23:55 GMT  
		Size: 5.4 MB (5422894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e348bc7be3d405264896161cad0286d0f945ccb1ef8e8ed67f69bddaf0c5`  
		Last Modified: Fri, 16 Feb 2024 20:23:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a65f88d172ecff3123199d41dc1bc0c914eb482d3dec40b2ed2eb57e97b9c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats@sha256:23d29396e19730a49a6b0bde55a9e8afef5cf02f9ee5790098ae5aa03ff3c51e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086846528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e2f65afe15b7ba76ba622a0afaceeb537ae9cb24cb696ce22a7e521486a1b8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 19:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.11/nats-server-v2.10.11-windows-amd64.zip
# Fri, 16 Feb 2024 19:15:16 GMT
ENV NATS_SERVER_SHASUM=e788d206a4e87585cbfbe2cb63fb54ea90f60c5af2ddb3651b4abc0192ca659d
# Fri, 16 Feb 2024 19:16:48 GMT
RUN Set-PSDebug -Trace 2
# Fri, 16 Feb 2024 19:18:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 16 Feb 2024 19:18:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 16 Feb 2024 19:18:54 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 19:18:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 16 Feb 2024 19:18:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df021e078a4ff93bc2323f46046c98de9300b24c8cf77dc63f7a24085b981fb7`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1d10641f0017bba6821c28982686493b31645320f22cfc225ce061cc71eb04`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7af4df07d603b6ebe953c777e30876e1f504f0d1cb2055ef1853986ce06d49`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e14943c6eccfb3f564a17f3210f47f8f53265551a05ea0d70a884f4b5359c4`  
		Last Modified: Fri, 16 Feb 2024 19:20:09 GMT  
		Size: 444.1 KB (444123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a546241baba604db37604b0f53df66414d45cd014c57e03ab1758286aa328`  
		Last Modified: Fri, 16 Feb 2024 19:20:08 GMT  
		Size: 5.9 MB (5940387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a57a0d0985f3c622f5fd6796425f51251bdeef41517125215f9ba85b92dad`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356c8a9f2a1f558ab90e6ff607c87d4e12bba79d7509c9a0e110d881ff3c2e35`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021d61d073b32684f9abed9154c2b0872f2d2b3e5b7a1e5854466fa1e87f609`  
		Last Modified: Fri, 16 Feb 2024 19:20:06 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e45267afd28ae058f6450ebf20484ab578533254f37b8687dbd1103271d092`  
		Last Modified: Fri, 16 Feb 2024 19:20:07 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
