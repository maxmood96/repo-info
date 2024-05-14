## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:26cc5f7fec152963fcf44b7585c1c3db7835674eaf0400b12f7c8a9a4a7e1e8e
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:abb0d45273c3cb063af46d0159fc7549ba87b6376fd9a3be24f8863502bbce80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaea0218483221f068f46995457c8deae5adebfcfa95cfd0b116091bd3d691c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:13 GMT
ADD file:7b9ec2bc447148065c15856f9e732b94f2b534011ede5939002e904bada7044a in / 
# Tue, 14 May 2024 01:29:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:29:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce314f7c9291d3ef0af89e3d92b5458ee154a39ea5bb198e51813bd983a6a20e`  
		Last Modified: Tue, 14 May 2024 01:34:30 GMT  
		Size: 55.1 MB (55099434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d65cd28b616f33428b6d9ceebeefb735fe9dcb789a3b98afe2a2dc5ff90c39`  
		Last Modified: Tue, 14 May 2024 01:34:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:48c12a54fc5d6c053bab7349673c9b84317d7d13fad0ded41031b861799dbda7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52602982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32db3931916f833b14347e6a495981669017c15aa2c89c9cd76c6a2aa3efd033`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:58 GMT
ADD file:13a42f1d0d96574cd178b73d649159e19cc66b0e82d42aa74855e9a10ab282c2 in / 
# Tue, 14 May 2024 00:48:59 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:03d9bc10c22757d74b153f2269cdb2f771de262ccb030e2d7fc092db5cb623ff`  
		Last Modified: Tue, 14 May 2024 00:52:36 GMT  
		Size: 52.6 MB (52602759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d0429bf66054c03dc0f7cb2f7df5a6c31b7b3fbac3be3fad25125130592136`  
		Last Modified: Tue, 14 May 2024 00:52:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a454de54c4913ae9aff1e44bd5cffbc0d7d23dcb21e6fbb2e75e223167bd507a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50256695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23cd655ed52f2bc5228e236fb4120e70a6fd76e49a39703e4c9e3a1b5c06531`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:09:42 GMT
ADD file:63719cf633d93e57c4bd75f789d6db91f1d8901c4b90ea404caf1328dea89d72 in / 
# Tue, 14 May 2024 01:09:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:09:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:97558ac59bb8ee0f89ab1819e25de6927b53ba7635fd1e458cac5707ef74a785`  
		Last Modified: Tue, 14 May 2024 01:14:51 GMT  
		Size: 50.3 MB (50256471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2e54b476493139c3d84e491ceb300e50b916abe5c49201d3fd313818526fe3`  
		Last Modified: Tue, 14 May 2024 01:15:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6fbe110c530d6af9b6ac685f5cffca38c65c32b671f163f05dce5d6dec99a645
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b9a12ca6ab1d083a41efa51ae7684ad2bd3600097e8c5e914dff4e0c9205cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:26 GMT
ADD file:de1099c2a1e9d3e89f834090eaaa6edbc98022b52bef2225e1507cd3712d024f in / 
# Tue, 14 May 2024 00:40:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c4f566910cd98a75c873befb2b5b10c8e19bcdc5320b9b5fba12016edbb79d5`  
		Last Modified: Tue, 14 May 2024 00:44:44 GMT  
		Size: 53.7 MB (53738943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11909dd21ebc438a78197c22300f78286d3b40226784a35ce3e11463d956d9f`  
		Last Modified: Tue, 14 May 2024 00:44:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:53f5ac65dae06d11025b08aadd606e23cd81a8d580e1ebc4a3b112708e6059bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1163a786234d0481bc53d933cb743e9c184087ef0bb93b70de28f4143fe81f45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:24 GMT
ADD file:9beb07c7ae102adb48c3e88bbadb035bd42b072f5b0d9c0e9b8aa399501cfd6c in / 
# Tue, 14 May 2024 00:48:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:48:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73b280b9894d081f8d59047728fa35ac303b730b5d939d666786efe4d000a76a`  
		Last Modified: Tue, 14 May 2024 00:54:19 GMT  
		Size: 56.1 MB (56076046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf781ce143a3075ca76e0fb8ae6baf3c3094b97a018113d187aa206af3eb3a2`  
		Last Modified: Tue, 14 May 2024 00:54:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:5602e7dd6ab8a95e81a8c77ffd9124307ca8c7912e0d612a40630641696bedbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839ba624d42ed673f449500093abcc4f4bd66ead1c21be2e39323066b24f3b51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:12:58 GMT
ADD file:ab7a7c4552b9baec3a6fc2725df0719e4757e6cb0d4c64e6815e8a3fe56daa91 in / 
# Tue, 14 May 2024 01:13:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:13:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d2eb60f220e5c6c125a56679db08e8c2523f7d15e5aedb0ac08449c8d08010e`  
		Last Modified: Tue, 14 May 2024 01:24:28 GMT  
		Size: 53.3 MB (53322088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caebc8ffbc8a56bf851fe3189785bd65a72a6db6cbce1b41ed7335abc509dee7`  
		Last Modified: Tue, 14 May 2024 01:24:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c767dd11563b1c20a11e63ccbc383dce79ab04bb71817cf820362b7fad6c62af
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58969624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f0fa92758a5f51a1b3fa90c6651a156a07495fd6a48dd6d36603bf8d0e0e1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:20:38 GMT
ADD file:61a3bb0f165b7e140ed2c521846c9df5fb991727c11a84df84186ee94577b5be in / 
# Tue, 14 May 2024 01:20:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:20:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d6813d8fcfdcf2e2360325d7bffcea01864d894227093b951de3e18038b743e`  
		Last Modified: Tue, 14 May 2024 01:25:13 GMT  
		Size: 59.0 MB (58969400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cab1bf915795064b5a64b8f7f4796f32883e9bfef249dbcc849a918c9eed692`  
		Last Modified: Tue, 14 May 2024 01:25:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:00ba98df326b87fe55dd34211ef3bf62e195e54cd8c42dcbc6906f32cd6bd580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53337814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5610262b22a4ba31f2b13739a6f03eaeb4051c98623197e607cbdb89548a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:23 GMT
ADD file:5b0f91387cb6daa675e1e72c0543f1d21245d9a3415c4941c20059596643d6f2 in / 
# Tue, 14 May 2024 00:43:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:43:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8816ee22aa5505b84aa73f5b06bc56c4541a6c0cd8fe946ae5ff9e268dc353e8`  
		Last Modified: Tue, 14 May 2024 00:48:20 GMT  
		Size: 53.3 MB (53337590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56344a4178555a50adba70a3b7a39ada9d027863c7524ffa12854c32015a93ac`  
		Last Modified: Tue, 14 May 2024 00:48:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
