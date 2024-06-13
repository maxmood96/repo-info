## `debian:stable-backports`

```console
$ docker pull debian@sha256:a7c6af3c51af71be472ae08d85cf75732a174aadb6a1e8ce80b6247dae35dcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:4af16ffab548f3748005f407eff905412675d5c4cbc82c8ad21046ecb3aa7e12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc114442c8c50a5e0b7da1ea45319e327fa760176feb63796734ad875763b18e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:54 GMT
ADD file:f461a46593d0f88f51655eb6e5aef85705fb1e59c6643347685aadc84546d7de in / 
# Tue, 14 May 2024 01:29:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:29:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f37cd38c722b1e1d9c2cb61ad8337e6bede774b7680a90cc4f6c1741b6f53dc9`  
		Last Modified: Tue, 14 May 2024 01:35:39 GMT  
		Size: 49.6 MB (49576375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314dbc1cb312e64b9c2bd9f5ff2c9b70ec18aa9cd4ce6efd54bdc2655f1a2055`  
		Last Modified: Tue, 14 May 2024 01:35:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8a386f741fd6e1386d03e4a7df966244b845aed3ab39630d1f693c49d0bc7cba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80183a9093546d3d9679c978b9548da81fd093e4b51f5f04cb17ba3fd796bf1f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:26 GMT
ADD file:4495608fd47098dd151f4f5bcfe5b2c3510bc9727ea774de59c8777d5b7b1812 in / 
# Thu, 13 Jun 2024 00:49:27 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:49:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45e31bf94facab4d4040929ab83ff9180d2e383c16ce574a83b69e8cc92dceb9`  
		Last Modified: Thu, 13 Jun 2024 00:53:47 GMT  
		Size: 47.3 MB (47338463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c18ffe0a2ce9bbfcd5cd7e0a657724920e7afc810b434bb3229829407be73`  
		Last Modified: Thu, 13 Jun 2024 00:53:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c633ed57779ed90953235eb7dbb1a5c7eaca79009b19fb0a9c1eb77e048e8a25
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45175294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe593d4b1d8e19c1a721cb1ee081ad159878bc61b62b2f649f7cea228728e51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:13 GMT
ADD file:d91c04beb7258cbeda73a92d52702ef1ce52bfd9b703f34f75b4f9dc116e8343 in / 
# Thu, 13 Jun 2024 00:59:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df39248e2915accc98a43c4c3134a4faa4f170d5653dc893a2832fd057a9bf2c`  
		Last Modified: Thu, 13 Jun 2024 01:04:49 GMT  
		Size: 45.2 MB (45175071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eadc393f57268d9042dd11df651010230a6ac2452eb88ce6b50e86aea8f1de`  
		Last Modified: Thu, 13 Jun 2024 01:04:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f8b561c0fd0f4848f091d40e1d1cf7e91aa3a7617d033fda6dc42d28c6cebd88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49613631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ee6edd636099ab4fae03333868b8ab9ab25951206ddcb91f44178db4d8967d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:05 GMT
ADD file:5b62f3039a87b1937cda1e5c97a7bf36461825c89832c832c078caf3bdbb2db7 in / 
# Thu, 13 Jun 2024 00:41:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:03457dbd69892698e00a797da22fe81fa1138e09da1460452eec507f5a36ca85`  
		Last Modified: Thu, 13 Jun 2024 00:46:05 GMT  
		Size: 49.6 MB (49613409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519acf6599a603af4cab23dfd99bcf1df3680cd3a7306da6c276fedd1ecb7730`  
		Last Modified: Thu, 13 Jun 2024 00:46:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:88fb7624bac4c5af86334e08aca60fff8f40546ce521fefabb64ea6073ee4105
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626ea1ff87629261b2f6b41a1581834319dd7091af19cae5c9ead0f378a1e7a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:49 GMT
ADD file:c5d2f87fad57933dab55fe8a2afdb3356c6ca0819b886a9ec57a7e43699ff51f in / 
# Thu, 13 Jun 2024 00:40:49 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f757c13ac58ca20fa5b66862a2e124861be3549685bc4b380b7ef9a45b8a7c2`  
		Last Modified: Thu, 13 Jun 2024 00:46:43 GMT  
		Size: 50.6 MB (50602480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7128844e54e1c328d334fca7a3e5744e32f1458e8ef675b98499c5d51f18eea2`  
		Last Modified: Thu, 13 Jun 2024 00:46:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9d1ad6a07f3d9b315ec2b91024ea80d8288bef36b155bebbdcf8033d98ca6b32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbceae1d889665b9faa4378952eee88925ce903ec37f227806db3980431d76b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:15:23 GMT
ADD file:f9ab0e52feb5538919bdd33ae9050e122b8d1d91fbe7944881cfd1a509b38586 in / 
# Tue, 14 May 2024 01:15:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0044db510d84fd2650bea36b923b327105917f16876a1ad4973dceb29f8cfdf5`  
		Last Modified: Tue, 14 May 2024 01:26:55 GMT  
		Size: 49.6 MB (49582333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d03d46d1098c10df1ac99a4a5370c4c4bd8f21df5e1021999d3a2a776ac4109`  
		Last Modified: Tue, 14 May 2024 01:27:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:473703bbbbc9ea58732e89a98e846c8692affe49a8014084ac75a404bcfe6c04
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53579961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04504473d2bc573b2913e94455fa23bd86922d9941c2bd0ccb2144e73625d2b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:24 GMT
ADD file:1afa9009ab53fcdad6de78a608f8350f53815389a9d5e5fd0da2b32f30a0829f in / 
# Tue, 14 May 2024 01:21:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:537829f6a196273679c3ea881b442fa5355f023e3189ad87e0817f2626dba031`  
		Last Modified: Tue, 14 May 2024 01:26:24 GMT  
		Size: 53.6 MB (53579741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e14db29de25656c50ed9a5f5b2e1eafc6de3dd5be1033b454220ae089d1cc39`  
		Last Modified: Tue, 14 May 2024 01:26:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc66f5ef00e4c21d8e0165c41269e74a501d9bcb8d3b4c9630e87acc71c91a47
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9503d6b7d771750a552123ccdcb7244c1fe44b754d8775ddede1bf9b3fb5ec6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:24 GMT
ADD file:f88f06b39d6c737a247de4dfad3590cf9bec53388b1f5430824faf715190a44b in / 
# Thu, 13 Jun 2024 00:44:26 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:44:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f57b71f3fc0c90b322a6291423d2a6828b004a23ce04c403787ec3b1b904deea`  
		Last Modified: Thu, 13 Jun 2024 00:49:19 GMT  
		Size: 47.9 MB (47942435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c9fae301a5a9a6fa91d13c27bda1d8b9501f77526e67e6cd8ffe7daad1543e`  
		Last Modified: Thu, 13 Jun 2024 00:49:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
