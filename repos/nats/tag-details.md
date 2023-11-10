<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.18`](#nats2-alpine318)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.18`](#nats210-alpine318)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.5`](#nats2105)
-	[`nats:2.10.5-alpine`](#nats2105-alpine)
-	[`nats:2.10.5-alpine3.18`](#nats2105-alpine318)
-	[`nats:2.10.5-linux`](#nats2105-linux)
-	[`nats:2.10.5-nanoserver`](#nats2105-nanoserver)
-	[`nats:2.10.5-nanoserver-1809`](#nats2105-nanoserver-1809)
-	[`nats:2.10.5-scratch`](#nats2105-scratch)
-	[`nats:2.10.5-windowsservercore`](#nats2105-windowsservercore)
-	[`nats:2.10.5-windowsservercore-1809`](#nats2105-windowsservercore-1809)
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
-	[`nats:alpine3.18`](#natsalpine318)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:4f6a1d713c5da5452aabfb750b69e3e69aac488edd6494419c99caeac4147510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; amd64

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

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

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

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

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

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

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

### `nats:2` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:0024077d143b0a7bfdf95f956e18ecaa8575a2f88c3de67f52966eed613d16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.18`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5`

```console
$ docker pull nats@sha256:0024077d143b0a7bfdf95f956e18ecaa8575a2f88c3de67f52966eed613d16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.5` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-alpine`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.5-alpine` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-alpine3.18`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.5-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-linux`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.5-linux` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-nanoserver`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.5-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-nanoserver-1809`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.5-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-scratch`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.5-scratch` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.5-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-windowsservercore`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.5-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.5-windowsservercore-1809`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.5-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
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
$ docker pull nats@sha256:138ab48f7b047283e3eb2d1acf622b23c374e75cfcc3b6d970567707f4ddbfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:81b47d0149350c9bdcfb8d8feb9a7fef29cd5035fb715cb5e132bbbf016af9ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26772a7b06a9668999f1994d61cb44dbcb35eb0e7a2d640b367c849c443924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:22:36 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:22:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:22:39 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:22:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9a38ba99bb0f5173ade4d43e7fab314c2ab10222375531e385a4d2c9aa4915`  
		Last Modified: Wed, 08 Nov 2023 19:23:31 GMT  
		Size: 5.9 MB (5871161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720cc03594a9482c305f2d83a0a42f1b58375fe6a0cf77d59472f68e56f9492`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c67b58ad44ec40d5f53875e515c77ffbe094d188b1f03002c1d9225580e83a`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:42c4c1b5ee3ca102e2c87387f37e509dd2acc7f21237fb070b7839b355871e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891614b88f4afa6ba67829171937018244da68802f536f02cde151602ad181d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:49:22 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14ca6423684b587ba0262d9327e475682141e06124c8b1ad8d5f7183a4db39`  
		Last Modified: Wed, 08 Nov 2023 19:49:57 GMT  
		Size: 5.6 MB (5608134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadd992a7090765cc1618e97ab3c1e91c7562cdfac327ae4b0d3fa82b6a4ebfc`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce3326cb3c80cb38d95420df5fe02436ad2f7258013bf9ac090a1a31cb9176`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:12be30d3fbcf1ba0084d37062241b5a9b11bd3dca3e02e61e87e5758b4614726
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8500685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6c039f3e9980643e17a19cddab5bf03c6c40a27ec871902c5b182bb10fd9dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:57:32 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00dfd55d3c54b407a4323cc40a651a2d308612aad22ac03d9aec00e0d109a5d`  
		Last Modified: Wed, 08 Nov 2023 19:58:19 GMT  
		Size: 5.6 MB (5599781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b846c96f4a323e0bfa5d04c866d6cae2153e34cadb9cb523e346640495d12c`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046438499ec06ac30ba00bf1e95fdc844d3c33035a91fc00647b7a5ba5248f14`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5c1dc2ba418501cec649509985005205b7887bd044243a47d0fdd15629d44be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8741956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf429242ed0ac373234ceb07135db81c4f910c88cd272879d16b79a4a8793ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:39:48 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:39:51 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfbc4ed5ca02b96f7eee7193f388bbe02a696b4f6855bd548497787379811ff`  
		Last Modified: Wed, 08 Nov 2023 19:40:45 GMT  
		Size: 5.4 MB (5409126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d331d938262245841172487da0e6f0712ffd1285d029df8a2119c4ddef1fa44`  
		Last Modified: Wed, 08 Nov 2023 19:40:46 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5078d93de0c2bb6c2b2699858587a800428f0d34107e25a11186ddfc2d8bc96`  
		Last Modified: Wed, 08 Nov 2023 19:40:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:138ab48f7b047283e3eb2d1acf622b23c374e75cfcc3b6d970567707f4ddbfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:81b47d0149350c9bdcfb8d8feb9a7fef29cd5035fb715cb5e132bbbf016af9ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26772a7b06a9668999f1994d61cb44dbcb35eb0e7a2d640b367c849c443924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:22:36 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:22:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:22:39 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:22:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9a38ba99bb0f5173ade4d43e7fab314c2ab10222375531e385a4d2c9aa4915`  
		Last Modified: Wed, 08 Nov 2023 19:23:31 GMT  
		Size: 5.9 MB (5871161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720cc03594a9482c305f2d83a0a42f1b58375fe6a0cf77d59472f68e56f9492`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c67b58ad44ec40d5f53875e515c77ffbe094d188b1f03002c1d9225580e83a`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:42c4c1b5ee3ca102e2c87387f37e509dd2acc7f21237fb070b7839b355871e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891614b88f4afa6ba67829171937018244da68802f536f02cde151602ad181d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:49:22 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14ca6423684b587ba0262d9327e475682141e06124c8b1ad8d5f7183a4db39`  
		Last Modified: Wed, 08 Nov 2023 19:49:57 GMT  
		Size: 5.6 MB (5608134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadd992a7090765cc1618e97ab3c1e91c7562cdfac327ae4b0d3fa82b6a4ebfc`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce3326cb3c80cb38d95420df5fe02436ad2f7258013bf9ac090a1a31cb9176`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:12be30d3fbcf1ba0084d37062241b5a9b11bd3dca3e02e61e87e5758b4614726
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8500685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6c039f3e9980643e17a19cddab5bf03c6c40a27ec871902c5b182bb10fd9dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:57:32 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00dfd55d3c54b407a4323cc40a651a2d308612aad22ac03d9aec00e0d109a5d`  
		Last Modified: Wed, 08 Nov 2023 19:58:19 GMT  
		Size: 5.6 MB (5599781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b846c96f4a323e0bfa5d04c866d6cae2153e34cadb9cb523e346640495d12c`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046438499ec06ac30ba00bf1e95fdc844d3c33035a91fc00647b7a5ba5248f14`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5c1dc2ba418501cec649509985005205b7887bd044243a47d0fdd15629d44be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8741956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf429242ed0ac373234ceb07135db81c4f910c88cd272879d16b79a4a8793ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:39:48 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:39:51 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfbc4ed5ca02b96f7eee7193f388bbe02a696b4f6855bd548497787379811ff`  
		Last Modified: Wed, 08 Nov 2023 19:40:45 GMT  
		Size: 5.4 MB (5409126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d331d938262245841172487da0e6f0712ffd1285d029df8a2119c4ddef1fa44`  
		Last Modified: Wed, 08 Nov 2023 19:40:46 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5078d93de0c2bb6c2b2699858587a800428f0d34107e25a11186ddfc2d8bc96`  
		Last Modified: Wed, 08 Nov 2023 19:40:44 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:a9f3a2110f1eb09e470ec8e6ceb8c0367ff9730e5a2858ae9227e099ee54d9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:0c226012b5b4f1ba95bdc615ef0e8721437e90f31cd402b62d2fc213c9e18545
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109799861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aba9099c0138472555a1301407981aca26b5968c5163a1eabf4cc84d6f66cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:19:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:19:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:19:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8ca9b4f8e7c27e1feeed9a95c93fb06d510c31ce572345243669dc8f91827`  
		Last Modified: Wed, 08 Nov 2023 19:20:11 GMT  
		Size: 5.3 MB (5328957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782df3c17bd28dab80efc3d155bdf906bb3a3c4f9445fc0c3cb2149620a1901a`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8671231e5b6fc8d1f848dcd0c02afdf0fc51af5e208cfc0c289e97247ed926b`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965fc975e399f4517925aa0d7da6853eb6490d55b0020fbe27ef0dcd28189aa`  
		Last Modified: Wed, 08 Nov 2023 19:20:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd991a6bc6adb9236cdfad3525a81799ce1d6792cdad9314d27c9cbf4487dc1`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:a9f3a2110f1eb09e470ec8e6ceb8c0367ff9730e5a2858ae9227e099ee54d9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:0c226012b5b4f1ba95bdc615ef0e8721437e90f31cd402b62d2fc213c9e18545
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109799861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aba9099c0138472555a1301407981aca26b5968c5163a1eabf4cc84d6f66cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:19:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:19:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:19:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8ca9b4f8e7c27e1feeed9a95c93fb06d510c31ce572345243669dc8f91827`  
		Last Modified: Wed, 08 Nov 2023 19:20:11 GMT  
		Size: 5.3 MB (5328957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782df3c17bd28dab80efc3d155bdf906bb3a3c4f9445fc0c3cb2149620a1901a`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8671231e5b6fc8d1f848dcd0c02afdf0fc51af5e208cfc0c289e97247ed926b`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965fc975e399f4517925aa0d7da6853eb6490d55b0020fbe27ef0dcd28189aa`  
		Last Modified: Wed, 08 Nov 2023 19:20:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd991a6bc6adb9236cdfad3525a81799ce1d6792cdad9314d27c9cbf4487dc1`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1152 bytes)  
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
$ docker pull nats@sha256:9fecbf245c762139b1c8e49baa716fff12e6cad3233e7b49f9a590015df44668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:e22ec2e18e611127f304fdf60c7a032f83484a3ad301ce7fc75d82558a3771be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037678583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fea0869cadcb9bbc44da57b5632e1f9d30bed6bb29865c88372e88a4ae7f99`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:15:28 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 08 Nov 2023 19:15:30 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 08 Nov 2023 19:16:50 GMT
RUN Set-PSDebug -Trace 2
# Wed, 08 Nov 2023 19:18:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 08 Nov 2023 19:18:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:18:49 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:18:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:18:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bb09743674adf30dae2f580e68ed4220cc275d1030138af1d9196f76db2dfa`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaaed723ac8145db4b016a47b3b6521affc9a2f5050a585eaa14373bab2e743`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4d02a56b40173f24235e4dc92e3e9c7d1b269ec1759bb4b958b24e95b30d66`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cfaf12507ccec6b44de4f8d2a6221ecab3a1a73436c8a318bc853cf50fcc87`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 454.2 KB (454205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f2dd0c08a5888a4a703ffec15d7cfe3b84561b703863061f3bf2df4c80f16`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 5.6 MB (5621137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff03a18d184bbf4e65a5e606a7d832816b14188a275f95833b62653cedbf0b`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9debd38a84d325d9fe18f837ac253fee28d0adeffd2f4d7b3271f68ad54c675`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33772821716109511229ab14a2f27900374a31cb60f803e934a5a200fd17d1e7`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba80d2cf335caa73b826fc7a7668cf860c76ad1b3788cdad09108ce5c8aaca5`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:9fecbf245c762139b1c8e49baa716fff12e6cad3233e7b49f9a590015df44668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:e22ec2e18e611127f304fdf60c7a032f83484a3ad301ce7fc75d82558a3771be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037678583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fea0869cadcb9bbc44da57b5632e1f9d30bed6bb29865c88372e88a4ae7f99`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:15:28 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 08 Nov 2023 19:15:30 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 08 Nov 2023 19:16:50 GMT
RUN Set-PSDebug -Trace 2
# Wed, 08 Nov 2023 19:18:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 08 Nov 2023 19:18:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:18:49 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:18:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:18:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bb09743674adf30dae2f580e68ed4220cc275d1030138af1d9196f76db2dfa`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaaed723ac8145db4b016a47b3b6521affc9a2f5050a585eaa14373bab2e743`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4d02a56b40173f24235e4dc92e3e9c7d1b269ec1759bb4b958b24e95b30d66`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cfaf12507ccec6b44de4f8d2a6221ecab3a1a73436c8a318bc853cf50fcc87`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 454.2 KB (454205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f2dd0c08a5888a4a703ffec15d7cfe3b84561b703863061f3bf2df4c80f16`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 5.6 MB (5621137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff03a18d184bbf4e65a5e606a7d832816b14188a275f95833b62653cedbf0b`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9debd38a84d325d9fe18f837ac253fee28d0adeffd2f4d7b3271f68ad54c675`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33772821716109511229ab14a2f27900374a31cb60f803e934a5a200fd17d1e7`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba80d2cf335caa73b826fc7a7668cf860c76ad1b3788cdad09108ce5c8aaca5`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.4 KB (1387 bytes)  
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
$ docker pull nats@sha256:138ab48f7b047283e3eb2d1acf622b23c374e75cfcc3b6d970567707f4ddbfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:81b47d0149350c9bdcfb8d8feb9a7fef29cd5035fb715cb5e132bbbf016af9ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26772a7b06a9668999f1994d61cb44dbcb35eb0e7a2d640b367c849c443924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:22:36 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:22:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:22:39 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:22:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9a38ba99bb0f5173ade4d43e7fab314c2ab10222375531e385a4d2c9aa4915`  
		Last Modified: Wed, 08 Nov 2023 19:23:31 GMT  
		Size: 5.9 MB (5871161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720cc03594a9482c305f2d83a0a42f1b58375fe6a0cf77d59472f68e56f9492`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c67b58ad44ec40d5f53875e515c77ffbe094d188b1f03002c1d9225580e83a`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:42c4c1b5ee3ca102e2c87387f37e509dd2acc7f21237fb070b7839b355871e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891614b88f4afa6ba67829171937018244da68802f536f02cde151602ad181d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:49:22 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14ca6423684b587ba0262d9327e475682141e06124c8b1ad8d5f7183a4db39`  
		Last Modified: Wed, 08 Nov 2023 19:49:57 GMT  
		Size: 5.6 MB (5608134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadd992a7090765cc1618e97ab3c1e91c7562cdfac327ae4b0d3fa82b6a4ebfc`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce3326cb3c80cb38d95420df5fe02436ad2f7258013bf9ac090a1a31cb9176`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:12be30d3fbcf1ba0084d37062241b5a9b11bd3dca3e02e61e87e5758b4614726
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8500685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6c039f3e9980643e17a19cddab5bf03c6c40a27ec871902c5b182bb10fd9dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:57:32 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00dfd55d3c54b407a4323cc40a651a2d308612aad22ac03d9aec00e0d109a5d`  
		Last Modified: Wed, 08 Nov 2023 19:58:19 GMT  
		Size: 5.6 MB (5599781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b846c96f4a323e0bfa5d04c866d6cae2153e34cadb9cb523e346640495d12c`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046438499ec06ac30ba00bf1e95fdc844d3c33035a91fc00647b7a5ba5248f14`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5c1dc2ba418501cec649509985005205b7887bd044243a47d0fdd15629d44be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8741956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf429242ed0ac373234ceb07135db81c4f910c88cd272879d16b79a4a8793ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:39:48 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:39:51 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfbc4ed5ca02b96f7eee7193f388bbe02a696b4f6855bd548497787379811ff`  
		Last Modified: Wed, 08 Nov 2023 19:40:45 GMT  
		Size: 5.4 MB (5409126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d331d938262245841172487da0e6f0712ffd1285d029df8a2119c4ddef1fa44`  
		Last Modified: Wed, 08 Nov 2023 19:40:46 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5078d93de0c2bb6c2b2699858587a800428f0d34107e25a11186ddfc2d8bc96`  
		Last Modified: Wed, 08 Nov 2023 19:40:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine3.18`

```console
$ docker pull nats@sha256:138ab48f7b047283e3eb2d1acf622b23c374e75cfcc3b6d970567707f4ddbfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:81b47d0149350c9bdcfb8d8feb9a7fef29cd5035fb715cb5e132bbbf016af9ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26772a7b06a9668999f1994d61cb44dbcb35eb0e7a2d640b367c849c443924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:22:36 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:22:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:22:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:22:39 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:22:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9a38ba99bb0f5173ade4d43e7fab314c2ab10222375531e385a4d2c9aa4915`  
		Last Modified: Wed, 08 Nov 2023 19:23:31 GMT  
		Size: 5.9 MB (5871161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720cc03594a9482c305f2d83a0a42f1b58375fe6a0cf77d59472f68e56f9492`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c67b58ad44ec40d5f53875e515c77ffbe094d188b1f03002c1d9225580e83a`  
		Last Modified: Wed, 08 Nov 2023 19:23:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:42c4c1b5ee3ca102e2c87387f37e509dd2acc7f21237fb070b7839b355871e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8754428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891614b88f4afa6ba67829171937018244da68802f536f02cde151602ad181d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:49:22 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14ca6423684b587ba0262d9327e475682141e06124c8b1ad8d5f7183a4db39`  
		Last Modified: Wed, 08 Nov 2023 19:49:57 GMT  
		Size: 5.6 MB (5608134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadd992a7090765cc1618e97ab3c1e91c7562cdfac327ae4b0d3fa82b6a4ebfc`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce3326cb3c80cb38d95420df5fe02436ad2f7258013bf9ac090a1a31cb9176`  
		Last Modified: Wed, 08 Nov 2023 19:49:56 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:12be30d3fbcf1ba0084d37062241b5a9b11bd3dca3e02e61e87e5758b4614726
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8500685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6c039f3e9980643e17a19cddab5bf03c6c40a27ec871902c5b182bb10fd9dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:57:32 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00dfd55d3c54b407a4323cc40a651a2d308612aad22ac03d9aec00e0d109a5d`  
		Last Modified: Wed, 08 Nov 2023 19:58:19 GMT  
		Size: 5.6 MB (5599781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b846c96f4a323e0bfa5d04c866d6cae2153e34cadb9cb523e346640495d12c`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046438499ec06ac30ba00bf1e95fdc844d3c33035a91fc00647b7a5ba5248f14`  
		Last Modified: Wed, 08 Nov 2023 19:58:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5c1dc2ba418501cec649509985005205b7887bd044243a47d0fdd15629d44be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8741956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf429242ed0ac373234ceb07135db81c4f910c88cd272879d16b79a4a8793ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 08 Nov 2023 19:39:48 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 08 Nov 2023 19:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 08 Nov 2023 19:39:51 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Nov 2023 19:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfbc4ed5ca02b96f7eee7193f388bbe02a696b4f6855bd548497787379811ff`  
		Last Modified: Wed, 08 Nov 2023 19:40:45 GMT  
		Size: 5.4 MB (5409126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d331d938262245841172487da0e6f0712ffd1285d029df8a2119c4ddef1fa44`  
		Last Modified: Wed, 08 Nov 2023 19:40:46 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5078d93de0c2bb6c2b2699858587a800428f0d34107e25a11186ddfc2d8bc96`  
		Last Modified: Wed, 08 Nov 2023 19:40:44 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:a9f3a2110f1eb09e470ec8e6ceb8c0367ff9730e5a2858ae9227e099ee54d9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.24-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:0c226012b5b4f1ba95bdc615ef0e8721437e90f31cd402b62d2fc213c9e18545
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109799861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aba9099c0138472555a1301407981aca26b5968c5163a1eabf4cc84d6f66cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:19:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:19:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:19:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8ca9b4f8e7c27e1feeed9a95c93fb06d510c31ce572345243669dc8f91827`  
		Last Modified: Wed, 08 Nov 2023 19:20:11 GMT  
		Size: 5.3 MB (5328957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782df3c17bd28dab80efc3d155bdf906bb3a3c4f9445fc0c3cb2149620a1901a`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8671231e5b6fc8d1f848dcd0c02afdf0fc51af5e208cfc0c289e97247ed926b`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965fc975e399f4517925aa0d7da6853eb6490d55b0020fbe27ef0dcd28189aa`  
		Last Modified: Wed, 08 Nov 2023 19:20:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd991a6bc6adb9236cdfad3525a81799ce1d6792cdad9314d27c9cbf4487dc1`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver-1809`

```console
$ docker pull nats@sha256:a9f3a2110f1eb09e470ec8e6ceb8c0367ff9730e5a2858ae9227e099ee54d9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.24-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:0c226012b5b4f1ba95bdc615ef0e8721437e90f31cd402b62d2fc213c9e18545
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109799861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aba9099c0138472555a1301407981aca26b5968c5163a1eabf4cc84d6f66cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Wed, 08 Nov 2023 19:19:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:19:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:19:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:19:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8ca9b4f8e7c27e1feeed9a95c93fb06d510c31ce572345243669dc8f91827`  
		Last Modified: Wed, 08 Nov 2023 19:20:11 GMT  
		Size: 5.3 MB (5328957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782df3c17bd28dab80efc3d155bdf906bb3a3c4f9445fc0c3cb2149620a1901a`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8671231e5b6fc8d1f848dcd0c02afdf0fc51af5e208cfc0c289e97247ed926b`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965fc975e399f4517925aa0d7da6853eb6490d55b0020fbe27ef0dcd28189aa`  
		Last Modified: Wed, 08 Nov 2023 19:20:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd991a6bc6adb9236cdfad3525a81799ce1d6792cdad9314d27c9cbf4487dc1`  
		Last Modified: Wed, 08 Nov 2023 19:20:10 GMT  
		Size: 1.2 KB (1152 bytes)  
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
$ docker pull nats@sha256:9fecbf245c762139b1c8e49baa716fff12e6cad3233e7b49f9a590015df44668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.24-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:e22ec2e18e611127f304fdf60c7a032f83484a3ad301ce7fc75d82558a3771be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037678583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fea0869cadcb9bbc44da57b5632e1f9d30bed6bb29865c88372e88a4ae7f99`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:15:28 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 08 Nov 2023 19:15:30 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 08 Nov 2023 19:16:50 GMT
RUN Set-PSDebug -Trace 2
# Wed, 08 Nov 2023 19:18:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 08 Nov 2023 19:18:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:18:49 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:18:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:18:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bb09743674adf30dae2f580e68ed4220cc275d1030138af1d9196f76db2dfa`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaaed723ac8145db4b016a47b3b6521affc9a2f5050a585eaa14373bab2e743`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4d02a56b40173f24235e4dc92e3e9c7d1b269ec1759bb4b958b24e95b30d66`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cfaf12507ccec6b44de4f8d2a6221ecab3a1a73436c8a318bc853cf50fcc87`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 454.2 KB (454205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f2dd0c08a5888a4a703ffec15d7cfe3b84561b703863061f3bf2df4c80f16`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 5.6 MB (5621137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff03a18d184bbf4e65a5e606a7d832816b14188a275f95833b62653cedbf0b`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9debd38a84d325d9fe18f837ac253fee28d0adeffd2f4d7b3271f68ad54c675`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33772821716109511229ab14a2f27900374a31cb60f803e934a5a200fd17d1e7`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba80d2cf335caa73b826fc7a7668cf860c76ad1b3788cdad09108ce5c8aaca5`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:9fecbf245c762139b1c8e49baa716fff12e6cad3233e7b49f9a590015df44668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.24-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:e22ec2e18e611127f304fdf60c7a032f83484a3ad301ce7fc75d82558a3771be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037678583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fea0869cadcb9bbc44da57b5632e1f9d30bed6bb29865c88372e88a4ae7f99`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 08 Nov 2023 19:15:28 GMT
ENV NATS_SERVER=2.9.24
# Wed, 08 Nov 2023 19:15:29 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Wed, 08 Nov 2023 19:15:30 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Wed, 08 Nov 2023 19:16:50 GMT
RUN Set-PSDebug -Trace 2
# Wed, 08 Nov 2023 19:18:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 08 Nov 2023 19:18:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 08 Nov 2023 19:18:49 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:18:51 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 08 Nov 2023 19:18:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bb09743674adf30dae2f580e68ed4220cc275d1030138af1d9196f76db2dfa`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaaed723ac8145db4b016a47b3b6521affc9a2f5050a585eaa14373bab2e743`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4d02a56b40173f24235e4dc92e3e9c7d1b269ec1759bb4b958b24e95b30d66`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cfaf12507ccec6b44de4f8d2a6221ecab3a1a73436c8a318bc853cf50fcc87`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 454.2 KB (454205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f2dd0c08a5888a4a703ffec15d7cfe3b84561b703863061f3bf2df4c80f16`  
		Last Modified: Wed, 08 Nov 2023 19:19:59 GMT  
		Size: 5.6 MB (5621137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deff03a18d184bbf4e65a5e606a7d832816b14188a275f95833b62653cedbf0b`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.9 KB (1854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9debd38a84d325d9fe18f837ac253fee28d0adeffd2f4d7b3271f68ad54c675`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33772821716109511229ab14a2f27900374a31cb60f803e934a5a200fd17d1e7`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba80d2cf335caa73b826fc7a7668cf860c76ad1b3788cdad09108ce5c8aaca5`  
		Last Modified: Wed, 08 Nov 2023 19:19:57 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.18`

```console
$ docker pull nats@sha256:21d43d8f8a9792a6ecfef55906908b9e74ce45642fb1847707945b73899420f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:16bc4f1997aa864a9adb650e0ea9feecaaf92d34c96daea542b826076c26b906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d4c09f46074c3ec57c857dd28630b59562cd7d2d4c4b20690289ed8873412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:19:59 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:20:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:20:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:20:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b26920aed8cd630891b64f6529f1637165e6bca368ec15b4c2a281d07d306`  
		Last Modified: Thu, 09 Nov 2023 23:20:43 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c6aa57cdc8774d7842eff23d32a9345c2b05454afd06cd3b79cb46bd4c65c`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282c5707fda46b68376eb95c5cace46da910f4604382bc5a16c5a4797978d19`  
		Last Modified: Thu, 09 Nov 2023 23:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ca2d0e50754620c5ea2a7897cce55c22e9042467dc919d442bf96fc7a16f840b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8967829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324f2eb8de0fdc19732cfe48c75790a91fd9011c6631e69e1e8ad24fd87fdc73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:49:22 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:49:25 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeccfd74ddf9a4d5416ac9eacb0ff972775e9161b55779e9f88044fe3cde09b`  
		Last Modified: Thu, 09 Nov 2023 23:49:57 GMT  
		Size: 5.8 MB (5821538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2290e2e7736699cf662fd25c981f56737ab8de1124d7fd7db1b0d12748841a65`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198ed93bb0c6aebba2a409e988aef19a4c81f7d46492490bb305ea4954f0e1c`  
		Last Modified: Thu, 09 Nov 2023 23:49:55 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6ecfb6c18d97d00a1e30b5766f1d3c4eb79319a238d4df7b66a88351ffefad94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cab0f66b79cbe6b38a967ebbd986f95e7118144a63fe0ee146598ae3df0f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:46:03 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:46:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:46:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:46:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175f54685917e884f1dd05d8c1e88c3e8c1c6296cc984f561887f63ff8023169`  
		Last Modified: Thu, 09 Nov 2023 23:46:51 GMT  
		Size: 5.7 MB (5679507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0428071c0dab0cb0caf30304b23cd037009004e7d83e700b38aadf1822024fb`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7afe9f8070aec98e4f225fc67551b2397ed94d0ab8e23ac16c37f1b67f83296`  
		Last Modified: Thu, 09 Nov 2023 23:46:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:4f6a1d713c5da5452aabfb750b69e3e69aac488edd6494419c99caeac4147510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; amd64

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

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

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

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

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

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

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

### `nats:latest` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:9b762a502b622e230c9f28209a99fa42c02b210c141db7d69371af3f314d2cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:13c8d74fcc1a65baf6183ffd2fb0e6bf203c1733604bce5ed976f92899c4908a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5482912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a3a784500564d97666dfd079f51bd760ec9381c8e37672164ee5a8814dd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:eb240b5bffcc0f613e659042b381fda542cd7e880986c213f55614d8c9cd276c in /nats-server 
# Thu, 09 Nov 2023 23:20:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:20:16 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:20:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:20:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cba24f033da718f2444230f64e704439d7f2b84fabfc969c8d76bb9384846971`  
		Last Modified: Thu, 09 Nov 2023 23:21:11 GMT  
		Size: 5.5 MB (5482403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e73b7f3a0e802d16548b50a27050fdfbbeeceab3baa40b4d8edcd30ce2e9e4`  
		Last Modified: Thu, 09 Nov 2023 23:21:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3824d5a2eaced6fc383dd112f9aa4419e7b695f3e28bfd82b777c51e0ed4f05b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c60b316ede95784f2e76d75502281fac3810627f124e56407076cc6b24413`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:9170d5b0d1641eee9b12dc349f23f35eda534f163f4e0774c2065bd1c6a6454a in /nats-server 
# Thu, 09 Nov 2023 23:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:49:34 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0b806f760797ca6495655d6ab966c0c7eb478e31a9e10edd05a11d19849361e0`  
		Last Modified: Thu, 09 Nov 2023 23:50:20 GMT  
		Size: 5.2 MB (5197530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa083376696ef3cfa57138bcef07c661395d393e21c97b5c292916c586b1113f`  
		Last Modified: Thu, 09 Nov 2023 23:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:076db1c8274b6d3365971b0789c7f8a8a0681edfbac5d8957fd61b0b451dec53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba964d20fa3e0e7612e094883ddbdfa4a2da08e5991acf12078d98e6b0b40ecf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:c2ac13057067603fc11d31bf35f44ec61100129c7bd0159bca62c9ad70ec0446 in /nats-server 
# Thu, 09 Nov 2023 23:57:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b415d8adad5189ef844c42b0a3f47fd89e72a26541b97ea226549fa147225c05`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 5.2 MB (5190076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc460654454d2ed863a7f07f1c65e9e81729b7021d1eaf8f4502ed7b74c4b4f`  
		Last Modified: Thu, 09 Nov 2023 23:58:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e02c3b198a6cf4ae395748b57c79c0306c6cab08d6b6f2df1541bd50858f6973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84170acbecc01b9d59102d83553de280f88645ad50d89c083db5ff92ed5de6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c77c6a1a9d77db3770061afda23f8d949858d1478cac389c677692fcbd14f75 in /nats-server 
# Thu, 09 Nov 2023 23:46:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 09 Nov 2023 23:46:27 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:46:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 09 Nov 2023 23:46:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:42f19c7824138f7306c0dc9c7f18acfbaf351d86f0631725acff764dec1557e9`  
		Last Modified: Thu, 09 Nov 2023 23:47:16 GMT  
		Size: 5.1 MB (5055195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96f43f0639ac050e05813fdaa230e83b8066636d9c1be745853c81ece9ac89b`  
		Last Modified: Thu, 09 Nov 2023 23:47:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:20d3b546a9b573f27169861bd07968e5d0939d7738f65378373b258a12c9b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:fc957c65d2150d7fd183fec1749bbe5adb538bf0dcfc6cafd92667d1a799489b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037960811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fea01147b21c066c4a63a73c76ae02a61387390cc5515a352c4491f0472ed0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:15:13 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:15:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.5/nats-server-v2.10.5-windows-amd64.zip
# Thu, 09 Nov 2023 23:15:15 GMT
ENV NATS_SERVER_SHASUM=0e07ed8f8ce2b0db0830eae0ba996f5023d8297ca043801411775555c183a964
# Thu, 09 Nov 2023 23:16:21 GMT
RUN Set-PSDebug -Trace 2
# Thu, 09 Nov 2023 23:18:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 09 Nov 2023 23:18:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b597f532bd5de48a9112abb9a71b13f9d8de9d52bbdbce1e11f9fe5a2472c641`  
		Last Modified: Thu, 09 Nov 2023 23:19:02 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ff2adbe6ec2a2587e8d4e25c48fb8c2623d5cec00758597b115e1f1f837aa1`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d9ece8307102c110647a0723cdc86fc1d4831a8c6e7272952d117ec8008c`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15081d252ec8cd448d61be1c1f55277085ed9d2a2795bf5bb57cb4bdedd03773`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 459.0 KB (458951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab9f279797e45b6e0a34cc00b41b1295ae26e5baa12b643180050cfa74b180`  
		Last Modified: Thu, 09 Nov 2023 23:19:01 GMT  
		Size: 5.9 MB (5898621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8754922d0f4912e6bb515690f0f752b9ae90ce8c927c56c77f0edb075a45de72`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b26c7151bd7bc6c861d6ed1a9dc1dbb53b7264b39a604f829c6e8b6105d7f0`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9dcefa248b044f2fb0c41aebcf9cb9ae7d75591edfc294272559a1cb79665f`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425508b62365bb42b7246651837150d092986710c7f6686e79f2e8d2be16c64c`  
		Last Modified: Thu, 09 Nov 2023 23:18:59 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
