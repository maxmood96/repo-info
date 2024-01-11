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
-	[`nats:2.10.9`](#nats2109)
-	[`nats:2.10.9-alpine`](#nats2109-alpine)
-	[`nats:2.10.9-alpine3.19`](#nats2109-alpine319)
-	[`nats:2.10.9-linux`](#nats2109-linux)
-	[`nats:2.10.9-nanoserver`](#nats2109-nanoserver)
-	[`nats:2.10.9-nanoserver-1809`](#nats2109-nanoserver-1809)
-	[`nats:2.10.9-scratch`](#nats2109-scratch)
-	[`nats:2.10.9-windowsservercore`](#nats2109-windowsservercore)
-	[`nats:2.10.9-windowsservercore-1809`](#nats2109-windowsservercore-1809)
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
$ docker pull nats@sha256:5ef3bd4225cea2eb31e1ef4ef1b93e86eed412d7825d6463e32e55c4bd802aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 10
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
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
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
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

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:b9ef701c1a6c164190123d100b3bc63223b4dc17841e42793337a8ccb1be221d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9`

```console
$ docker pull nats@sha256:b9ef701c1a6c164190123d100b3bc63223b4dc17841e42793337a8ccb1be221d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.9` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-alpine`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-alpine3.19`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10.9-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-linux`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-nanoserver`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.9-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-nanoserver-1809`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.9-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-scratch`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.9-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-windowsservercore`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.9-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.9-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
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
$ docker pull nats@sha256:a80417b674c2e8ad4ab34c851e21394754889650b8bce2d399b050db33dd7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4e6d717f9fb1a9ca8abbdf2ac19d76f8c563316b181e2936c0267ddb34e1275e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822fc1ef74e9fb8146c7428b7d37780db3e7c234e76ad0e199dc06bd5d05fad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 07:55:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 07:55:34 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 07:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:55:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69f772c4b99c75574ad7f1cac560bc3c556ad426c2e18469cf8760a946c4f5`  
		Last Modified: Thu, 11 Jan 2024 07:56:32 GMT  
		Size: 5.6 MB (5608603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a15d6508055f924e822235d623be8495237f3065ac68ac4342bcd57aa7598`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f94d9ca591032305aba5c5983bbe28a4b5680ead1a0075b7e4f89f1da73057`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:a80417b674c2e8ad4ab34c851e21394754889650b8bce2d399b050db33dd7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:4e6d717f9fb1a9ca8abbdf2ac19d76f8c563316b181e2936c0267ddb34e1275e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822fc1ef74e9fb8146c7428b7d37780db3e7c234e76ad0e199dc06bd5d05fad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 07:55:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 07:55:34 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 07:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:55:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69f772c4b99c75574ad7f1cac560bc3c556ad426c2e18469cf8760a946c4f5`  
		Last Modified: Thu, 11 Jan 2024 07:56:32 GMT  
		Size: 5.6 MB (5608603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a15d6508055f924e822235d623be8495237f3065ac68ac4342bcd57aa7598`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f94d9ca591032305aba5c5983bbe28a4b5680ead1a0075b7e4f89f1da73057`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
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
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
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
$ docker pull nats@sha256:a80417b674c2e8ad4ab34c851e21394754889650b8bce2d399b050db33dd7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4e6d717f9fb1a9ca8abbdf2ac19d76f8c563316b181e2936c0267ddb34e1275e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822fc1ef74e9fb8146c7428b7d37780db3e7c234e76ad0e199dc06bd5d05fad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 07:55:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 07:55:34 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 07:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:55:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69f772c4b99c75574ad7f1cac560bc3c556ad426c2e18469cf8760a946c4f5`  
		Last Modified: Thu, 11 Jan 2024 07:56:32 GMT  
		Size: 5.6 MB (5608603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a15d6508055f924e822235d623be8495237f3065ac68ac4342bcd57aa7598`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f94d9ca591032305aba5c5983bbe28a4b5680ead1a0075b7e4f89f1da73057`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine3.18`

```console
$ docker pull nats@sha256:a80417b674c2e8ad4ab34c851e21394754889650b8bce2d399b050db33dd7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:4e6d717f9fb1a9ca8abbdf2ac19d76f8c563316b181e2936c0267ddb34e1275e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3822fc1ef74e9fb8146c7428b7d37780db3e7c234e76ad0e199dc06bd5d05fad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 07:55:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 07:55:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 07:55:34 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 07:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 07:55:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69f772c4b99c75574ad7f1cac560bc3c556ad426c2e18469cf8760a946c4f5`  
		Last Modified: Thu, 11 Jan 2024 07:56:32 GMT  
		Size: 5.6 MB (5608603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a15d6508055f924e822235d623be8495237f3065ac68ac4342bcd57aa7598`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f94d9ca591032305aba5c5983bbe28a4b5680ead1a0075b7e4f89f1da73057`  
		Last Modified: Thu, 11 Jan 2024 07:56:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
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
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
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
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:49579342e54b6fe0263230672cb63c8dc0b85f369a2449295977b2aca1a858eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a4c5bd5499736249a495dc3fd7f69b3d58e0fbb72ec8c39149d45fb2ec828928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7ecbe61391937484d91deea721c26275b838ed2f1a544cb7d27649fea88a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 19:14:23 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 19:14:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 19:14:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 19:14:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 19:14:29 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:14:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60612082b2215deb34927d747ff59cc136d10fbe210aa03face1e3e40745d0d5`  
		Last Modified: Thu, 11 Jan 2024 19:15:34 GMT  
		Size: 5.8 MB (5833330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088f49386fbb3720ad8461c6d7881295e9c48fa99d1f57d11cd0691dfa473b6`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cf6cbe03e155608aa0ec7760aedfcc7e5aab77a5ff85ee0926576da7b32df`  
		Last Modified: Thu, 11 Jan 2024 19:15:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1f244a23d080f3d62399207da0f16e81c3fdb81dfb934a152ec0e747823bc5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5671d61834fd4e6a2823ca774880d51892a714cd391861e9686741fe7b65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:28 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:31 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7896c57e8ba12d7d041989554c83e1bdb3435496b7651f904e28838af7e1a230`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 5.7 MB (5700434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b7e96432806e34e6eec52c821bd6b7973e4a0f8217f515c41a3f81201028b`  
		Last Modified: Thu, 11 Jan 2024 17:54:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b664b78eb4d987975a077342699785ac6e59218ea57df07be5bfdbe31384bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:5ef3bd4225cea2eb31e1ef4ef1b93e86eed412d7825d6463e32e55c4bd802aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 10
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
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
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
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

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:9e7653cadc9f2e1210a6f4d7cf95f6882e73a1fbfb9af317a2a8759cb1080853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:0237da0c92869cc89b906549bcd163a0fa0c35e4600d249088a38e24acedf0c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656365da7eb279cc4f4b5ce458d452faacd307a572871edca17499eabb5e566b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:57:22 GMT
RUN cmd /S /C #(nop) COPY file:f77b98ffa708fbfcf6aa9d766be9e893df4ae6e45b22fd61597a9746c6211313 in C:\nats-server.exe 
# Thu, 11 Jan 2024 17:57:23 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b10e2b988ab2be124746af1ddc26c710ea2f77b50009cc4ae6ac2dc88f31904`  
		Last Modified: Thu, 11 Jan 2024 17:58:31 GMT  
		Size: 5.6 MB (5616197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c333f008880fe22df9882712558f049da18a2f7d116c14ebc99123dc1629f`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb66675f422186e1d9598585f1b449fe84330d2c93232ce521b53f522686151`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ec2a1ec7a58ad21a5616d5baae229ae6070726a34c8bed83a4b9454cfcea7`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5598974f6bf9da7c1b0f0bbfb58c0a658c40e80d22a29302d195b0fcc910ba`  
		Last Modified: Thu, 11 Jan 2024 17:58:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0ae07b8690f01e68e738ea650ce1f22068ea22463561384db824f3c80cdb8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:8e0d7c2f8e1a704b5a1510a9b792965e80df98c23266790f403c12a7e4b334a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce61e33cb4a8d130b0bb7871e706ccd2897ae03b3b77a43a733ff1364582c913`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:a70beb4afc760b4eb620b77324ac11877e2d745bc4b21651e5f559167412340a in /nats-server 
# Thu, 11 Jan 2024 18:26:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 18:26:32 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:26:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 18:26:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08d3ed80ce681bf0a8f2508582bd2ef4aa2dd9939984a992fd90ef1418b10450`  
		Last Modified: Thu, 11 Jan 2024 18:27:32 GMT  
		Size: 5.5 MB (5500831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eee350ffa42c18b6c993b56ed7c2d44e1b73b9a6dc2ab17cd2babda5258ef4`  
		Last Modified: Thu, 11 Jan 2024 18:27:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5d0d4af172e08fcb077acc722a291563bb4246cdc721f75e42741cbeadd9b01e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa461205d8d06abdf4b7afbc36edef28268cff127eca59c15781a21abdc05a44`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:e0407774ec3be35d2e808ec5e153a35f02fee37376866bb6739551963e9d6d12 in /nats-server 
# Thu, 11 Jan 2024 17:54:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:58 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cac40ef0b21a2de49f6f818ce65744412272bb468bb3dca1cc5c716b2a6ee378`  
		Last Modified: Thu, 11 Jan 2024 17:55:42 GMT  
		Size: 5.2 MB (5218521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62cc0a6c2abe679eec457a613170aa1795e9ce68d30456aa09b60970b00a0c8`  
		Last Modified: Thu, 11 Jan 2024 17:55:41 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7b67d3baf5a1e10dbecb7b5514f42d73dce5d50450ceb708c3fa574b2893c430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609cc3c36f05c3ff3e3f4e1e67b5bb40e09138ef4e5f6abc6934e14cf521a2c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 19:14:56 GMT
COPY file:d6340439c8d5766d4955e469bbaca54df62ba032566e17bab50e50e403cab1a0 in /nats-server 
# Thu, 11 Jan 2024 19:14:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 19:14:57 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 19:14:58 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 19:14:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c113f4984cb6e8b3483ce21ba872b78202b3b2eac11c724c47edad86810ce001`  
		Last Modified: Thu, 11 Jan 2024 19:16:02 GMT  
		Size: 5.2 MB (5210343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef6cc09b8153069eb28379b61acacd4a0f45729f233c8b9d4ecfbd48337810`  
		Last Modified: Thu, 11 Jan 2024 19:16:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b543336f8e1639bdb1f2e9a96bc3a78ccac747b1c44fd8c78ea0a13cdd4aa784
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334794d13900ebf879e3e215871526baafdb207c5be27bc100be47f153323f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:0935cf9ca319e159c678d16454c79c757bef4168fafa6ad76522073f867c963b in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ac65c39531784892344fb47f2060284996e6b88ddc75791a829bf12c720767bf`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 5.1 MB (5075680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775bd974958061def57a04bbc652e5ab2f18031b08a9a297bb3426a214baf75`  
		Last Modified: Thu, 11 Jan 2024 17:54:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:04f8f6f0858c1e8fcbf86a758102395de8b6d543fcd2c0baf16d056f09bd4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:4c2e40684788f93bea34db4292aee27373d84be0532c9352632b716ceebbba7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076099707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1795f61d31593be653551564451268e4e397810bc43371619c1d959f48a0e8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 17:54:22 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.9/nats-server-v2.10.9-windows-amd64.zip
# Thu, 11 Jan 2024 17:54:24 GMT
ENV NATS_SERVER_SHASUM=bfbd7ff25afbd3642c609bef2b2b7dc2aa50bd5bd68ccc49e93fad19a9a6cb6e
# Thu, 11 Jan 2024 17:55:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 17:57:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 17:57:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 17:57:06 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:57:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 17:57:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224c7236e12b5aa7993b33657fe38d98004eadc983d555ae67388646847705b`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5bbeb60e71951e04111c84e408cdd8ff873854dba369695063c0eaaefa960f`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88802c34ac4c859c0f62adc19e16fd16bc8f4b47c84b32c87a4f18d8eac3b78a`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353b048c54f8083c5695457ccedd4c190cfc01e5de281cd9c0468f31f49b4b4`  
		Last Modified: Thu, 11 Jan 2024 17:58:15 GMT  
		Size: 453.5 KB (453458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db52828ed754f11fc969146425dadb04bc730c828912958e14467f7be8b5d6e3`  
		Last Modified: Thu, 11 Jan 2024 17:58:14 GMT  
		Size: 5.9 MB (5911146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eccfd4d8ed4c613c039ca077c57d2f930a8d40a949cc242dbb6b371e8cedbe2`  
		Last Modified: Thu, 11 Jan 2024 17:58:13 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33e1b28351a4fe0bc4eec8607395d735316d716474e1c467ab72b15015be54`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7751382e1d3c8dcc7ca1e1ed7c1a75f4279619ead870a41593bcfed71ada5a`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7900d56c1aa3b986dd872e51975e8f01e88c8a31ab9245a07ed46f0215e623d`  
		Last Modified: Thu, 11 Jan 2024 17:58:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
