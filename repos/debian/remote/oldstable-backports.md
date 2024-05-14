## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:223b500bfe2b8ee33bbdad3d5ba6855c9c6b2f16e569a18fc774c52b46b55541
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
$ docker pull debian@sha256:6a3b42fa246529331720455b89e14dfbd3cb6671f2991457321bc4ec27cf567d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f12e2a6485597e72b3408d6ab227744745300b2601ac55480dd8b0b436799f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:18 GMT
ADD file:ce3e56297f02c143f98657eee5fda9a5d26b317af0ef5efa0df6190b40fdc28d in / 
# Wed, 24 Apr 2024 03:29:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:29:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d5c5865411ca39a370691441c89039728716ddc5213860b34ef345eb96225494`  
		Last Modified: Wed, 24 Apr 2024 03:34:41 GMT  
		Size: 55.1 MB (55098929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dba6c69a81beee63df03bad212d7c1fe7ba9ffdb476e8b81b2cc7325bb9aa3`  
		Last Modified: Wed, 24 Apr 2024 03:34:50 GMT  
		Size: 225.0 B  
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
$ docker pull debian@sha256:a28829c83b8ed6d9fac4df4ad3295123240778ce950f061e906ce035a363bc94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50255805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e8b1248565d202e2e67cc829badf8aaf5baa95fa7cdbbf921e9bea3c18dc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:08:07 GMT
ADD file:49ec8dc6cf27136681b59232d67ba463054cb6c4f2a125eec680d9c6da905d9b in / 
# Wed, 24 Apr 2024 04:08:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:08:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cef94b2af8e03da719e6831e0f4454a4e4a65107a474566cb6784d7b461cd6e9`  
		Last Modified: Wed, 24 Apr 2024 04:13:15 GMT  
		Size: 50.3 MB (50255580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d69e2bed973a4360c2ad2d60abd20015f885c43f8b89f222000124c4760283`  
		Last Modified: Wed, 24 Apr 2024 04:13:23 GMT  
		Size: 225.0 B  
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
$ docker pull debian@sha256:7dfe7985c5bda726b6188bf5115a446c63fece5044cb54c68173876d4390a846
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53323002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9a45f2d1d2d839ccc101e071d37a7a857b89a6c24bc694528f4e1f8f88a285`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:16:09 GMT
ADD file:e0dd92b044a7510fabb0ba4bbf29d9f6ef964f381c00e3e2afd3f98eb2065212 in / 
# Wed, 24 Apr 2024 03:16:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:16:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9edcbffefc2bb597b834271d16a82618a34d783ba56738f1b152ae25d68de9f2`  
		Last Modified: Wed, 24 Apr 2024 03:27:28 GMT  
		Size: 53.3 MB (53322775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3167939daf69d4e8bda6edf0a9fb13d7e0aa85bb67806a9883973148eb8360a`  
		Last Modified: Wed, 24 Apr 2024 03:27:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:bf0838947eb39441cf3e4c9e4c8979b0ee94fdfb794870f1265997698d01a2fe
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58968410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe13eab89c51c3c5743febc6088fae0a7a81392e1c2703507f43b81bcc550f59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:59 GMT
ADD file:4192db4d33fd4351a068f704c1add23a9e1f543730c2c0f3c7450bbff357cbfa in / 
# Wed, 24 Apr 2024 03:22:03 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:22:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06d71beaf15ce3ecdd3c6b420b48ef1151284b9d98ff24ef572d612f6b3c64a7`  
		Last Modified: Wed, 24 Apr 2024 03:28:02 GMT  
		Size: 59.0 MB (58968183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958c5daddba88d251d1a5693b4cf3ff939d22761fc75f8658aa292d6357936a9`  
		Last Modified: Wed, 24 Apr 2024 03:28:12 GMT  
		Size: 227.0 B  
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
