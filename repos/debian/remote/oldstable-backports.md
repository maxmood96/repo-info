## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:394e6d50a4ff8c526e223b305137fb3916f4d5a1aa63d42cada5b62a76cf2ff9
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
$ docker pull debian@sha256:25f27307df93a5365998d836579e8376e5206966ac756bcb074eb0d3b3e88a1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47145519bb5b92a141eb6f1e66b4d47d429515eaa4a4616c34d1ab50154ccb7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:36 GMT
ADD file:3076c11b91dbcd726551218a818e6a6ebab851cd8b68803346ec9c5d9d3247d0 in / 
# Wed, 24 Apr 2024 03:53:37 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:53:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba213c2ab49fde4c72c9c0d98122e29742fb16cab984811b24acb10744051aad`  
		Last Modified: Wed, 24 Apr 2024 03:57:34 GMT  
		Size: 52.6 MB (52602925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1456d516b2abe0d64d7ec7b8c4999f76b2f9d783a9d161acf15610093446bf`  
		Last Modified: Wed, 24 Apr 2024 03:57:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:77092ac1452b0fc26d86195266b8654c54f8bea87a5fbf2b51b534a6ae3bb194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50246677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a058b7d3d1c35d0095e6c651419e46688cbd27dee42a6f01b777734ee0906b99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:00 GMT
ADD file:e61ecc3e656cfc321fc9b248be57e44d22d354a85153998c2c821ef696a735b8 in / 
# Wed, 10 Apr 2024 01:00:01 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:00:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:203ea083c11dd7781e27b1097c03c52d31bfd5b9f00e2cda6016b1719161c946`  
		Last Modified: Wed, 10 Apr 2024 01:06:59 GMT  
		Size: 50.2 MB (50246449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de12796d0cc54a919a89ee504e1373268e2d056512797d2d3321367867623d39`  
		Last Modified: Wed, 10 Apr 2024 01:07:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:99b5ee7ee3af4b4f9b1ce9ac39beb6798c084395ac29015278253131d23745d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53729381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fe12e6c31824d768818936b091128f29d6288ff10b5e7ec84baf2f021d6544`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:16 GMT
ADD file:53856f27805a92ba19246277ad1f99715b9ebb795b70d52c57c1ebdb2f2241de in / 
# Wed, 10 Apr 2024 00:41:16 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:41:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b94d92df6a8d1ebc18864a73e66c0f8447d12fd146762271805d17c1f59da96c`  
		Last Modified: Wed, 10 Apr 2024 00:46:18 GMT  
		Size: 53.7 MB (53729156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9615cf8f43bae91be79a1a6a7c6e36e7c9f8750f32b3a9e03e0e1bb5ee8a10`  
		Last Modified: Wed, 10 Apr 2024 00:46:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:548d7cf5ea42b61cebd90c257ca826af5156d1c2e378c38d602722ea1bf951dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3199bff7b4562fa6c2f584c1aa507283518c119b57fa18658f62c3c1e37e135c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:09 GMT
ADD file:8f569588fd432200be400406a6c4a8940f12157fa0f0925206c01e03d21fffbd in / 
# Wed, 24 Apr 2024 03:40:10 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:40:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8af620412f83a482c74da93f3e47a6e6d67e1dc186f4ccdaef1d78909212dbec`  
		Last Modified: Wed, 24 Apr 2024 03:45:57 GMT  
		Size: 56.1 MB (56076585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a015c43d482b0a2dcce17e36f1490cc9c5b157ef01c546758f4b30a90b449673`  
		Last Modified: Wed, 24 Apr 2024 03:46:06 GMT  
		Size: 227.0 B  
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
$ docker pull debian@sha256:64bb73723362cdcab5bda70daf4aabaee48030d6e5c81fd27638c26531035261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53337664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94378d953ab07003655794556806f7bbf1b547c64d89baab445d438b9521ee76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:24 GMT
ADD file:1960f30ff8746471ba8bb791981af15400168c093c3b61558a72b68dd0aaaa8d in / 
# Wed, 24 Apr 2024 03:44:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:44:36 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:257a898cbd262d879926ec0e3a5bf41c715dd12afcd9ac558b5c21270dd9c6a3`  
		Last Modified: Wed, 24 Apr 2024 03:50:02 GMT  
		Size: 53.3 MB (53337440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707b0ce698eae5531ba85c7c504e7a6e99e4c321396ac730b8890ceb7a311bd9`  
		Last Modified: Wed, 24 Apr 2024 03:50:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
