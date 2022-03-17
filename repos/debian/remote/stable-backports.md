## `debian:stable-backports`

```console
$ docker pull debian@sha256:e387c9d46b58b0a20cfc11367ea5d2579d6295635db7f54245a566c5bd4659a0
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
$ docker pull debian@sha256:626c3cbf793ff46f18566915681242fbd380e2b0cda3d1e6c31cd5ff8b0e1410
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54923096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d170658f60a238d0b2eaed0b643052ec66102f089130358ae28d21ef8cc762a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:14 GMT
ADD file:ad59c82fccc7305f2c7e3b2811d4f9dd0fe0d5c8200c4c0f6b944b6772233f6f in / 
# Thu, 17 Mar 2022 04:06:15 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:06:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:18409aafdb459273fa88920af01b8dd3b57942f3ca8d9c3d06420dfb28c7513b`  
		Last Modified: Thu, 17 Mar 2022 04:13:01 GMT  
		Size: 54.9 MB (54922874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe32c8670900af401033d7a4d06e1b6b4f881aad92cf9089d9ec50fb3cbd0e58`  
		Last Modified: Thu, 17 Mar 2022 04:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b0fdef4ecfd67cffe99bc5394b3f7b8d9457abe7a8f1b90896022d0eea794f60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52470503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e9b1bc6cfac39106d0957cbc179e844a3df84cc106b236419082f906fe3fd0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:23:50 GMT
ADD file:9070099b9e7f65925cfc27b967a7f26d77c4004f85af4eb650e5d68ddabc3232 in / 
# Thu, 17 Mar 2022 05:23:51 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:24:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ebcd44d6a8669eec12cb7bf0952b4514ce89281ad2d178b77e3a2aee08216a1`  
		Last Modified: Thu, 17 Mar 2022 05:40:51 GMT  
		Size: 52.5 MB (52470279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe35ed79b2ba3969a99a3cad750301658e9ee908eb5b166a6a069324d2fbba7`  
		Last Modified: Thu, 17 Mar 2022 05:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ffc2bfede771f82347cd7ca6488a16b03659de70188eccee7e9f9d45eea79695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50122540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c72d59eab1b861130bcae4979d5f7d4c7871767e859856f2d77be5823dd9a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:35:24 GMT
ADD file:f628ad367a67a919d1385cf48311ebb0883d86274244b887945cba4c453f4b35 in / 
# Thu, 17 Mar 2022 09:35:26 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:35:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a7cb48db87768c0e7194b1e29a5e16b2ab6203dcafa7213fac705c99542e5059`  
		Last Modified: Thu, 17 Mar 2022 09:51:52 GMT  
		Size: 50.1 MB (50122316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc279f0603b60ad84ac9bf56bb551e81e99990f042f8c1032f51df45fb335fd`  
		Last Modified: Thu, 17 Mar 2022 09:52:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a1eb9f2d2690118ea13468c8ed5dcca42edd5caf7b7655e1c56287e35129268d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53616548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d9af6ac422c18b1ea269e96343e28764a58f817c939f22b0cbda2a9072c85f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:23:38 GMT
ADD file:705f4425ddacd75f812dcf45c6ac274fff1ae16b7bcc9d5c870733ca0d977686 in / 
# Thu, 17 Mar 2022 03:23:39 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:23:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2ce4ce4b464a69b9add768f10f0bdfd1f2257d2be2f600556f5ec1a3c1d289d`  
		Last Modified: Thu, 17 Mar 2022 03:31:45 GMT  
		Size: 53.6 MB (53616327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2170751bec3bc187a8331f7ed4be7047e9c3a79ebe1e76b4607d12fcbf1a92`  
		Last Modified: Thu, 17 Mar 2022 03:31:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:df8c3f0229986f367593744a46d7587a4a83333942b6a57cc84b4a1121ce2ce9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55942601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824c279d909fdf61381b5d275958960f699f800b66650d84290b8fe18b6f828c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:18:08 GMT
ADD file:6c5c67c17d3279bfb703a67f865cad2094457c4b4f68b313d7c39a2eaa504ab0 in / 
# Thu, 17 Mar 2022 08:18:08 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:18:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61709287572d528e3d07d1dafe8d1f8dd2392cb7ef6102fe86261dd8bfceabba`  
		Last Modified: Thu, 17 Mar 2022 08:27:39 GMT  
		Size: 55.9 MB (55942379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787e7a59e69b9333fe0cb15b712dafe029e94a6193dd036cd990ecd51e46470b`  
		Last Modified: Thu, 17 Mar 2022 08:27:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:c07b98f5a5dfa70508ea40dff4cbb793df7c5613845ae3d5298996169c9955d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53180172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff7b61fe4cb752694e2fd4c5778bcfc5714278ed48e36e6aa87963b0164e828`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:21 GMT
ADD file:22446ccb92b020a34bb4fa578062e94a7e776313998cdbb8743e41442ba7ab18 in / 
# Tue, 01 Mar 2022 02:06:22 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:06:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:db3e6adecc9ec8995a8ed05a9d749b28d4de14d32f51c9d679541304d9030af7`  
		Last Modified: Tue, 01 Mar 2022 02:16:45 GMT  
		Size: 53.2 MB (53179948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303b4b714a209c56828d9cc135e13903d71dfa9f193f5edfe34910d91e60f65`  
		Last Modified: Tue, 01 Mar 2022 02:16:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:210bc19cbfeb9aeeeab355404dd42b933e1e2bf3dd6ba987978ba461a0c5a78c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58834342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6578e654be9d46b1d985259b13667fb89efca0c0085383de7dec6b26d32aa791`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:25 GMT
ADD file:c6e5b056c4ecb473fcbc63681d88f2f87b0934c9ba037863e9da9b370f087079 in / 
# Tue, 01 Mar 2022 02:08:32 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9023d75dd894dc3a0ea6919a2f19f70fe20c23ca26106693ba19f113162b3cfa`  
		Last Modified: Tue, 01 Mar 2022 02:18:19 GMT  
		Size: 58.8 MB (58834118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b75eebff70246db2cf542c2ee6b89a7e7f4c7dabbc0a83c9b221f2cc737d3`  
		Last Modified: Tue, 01 Mar 2022 02:18:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:db4fcbf6211caa26f1695cb3e723fa16b79c85baeb71534b5217ccaeeb26e6cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53217737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b32e511a7c0d9242823b7100d9772fce8d205eeaf8dce728bbaf7178ddfec5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:08:35 GMT
ADD file:3d17b3df6f50145162ccc296aeb7ff213cb25781e3109520213e5747f12890d9 in / 
# Thu, 17 Mar 2022 03:08:38 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:08:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ae361ac8cd28ad1d5ad50743b8f0571065feba2dc813626ecbe91b8c74b281d`  
		Last Modified: Thu, 17 Mar 2022 03:14:22 GMT  
		Size: 53.2 MB (53217514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b65f4ad312def0ba87e49cb4ba9be86d7769025d57fb4e871cf85e0b0328eb`  
		Last Modified: Thu, 17 Mar 2022 03:14:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
