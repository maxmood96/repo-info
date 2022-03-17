## `debian:stable-backports`

```console
$ docker pull debian@sha256:91ee933d7a02f1b4f5ad4ce2c7eba377fb2899b6feee1fecec7c6b8317eef345
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
$ docker pull debian@sha256:bd007727567e32513b423f75259c65281adbb7e2cd07dc64d090235d61e9de56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53187689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba64a088d5fe1f1da1fe52309d357491abd53f18bd6307cbb2db85e98a87e81`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:56:44 GMT
ADD file:c692fb767ac3c1d9c4baa0fc6e15af57c52c5367065e85293e9ac926e8a40e76 in / 
# Thu, 17 Mar 2022 08:56:49 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:57:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:96ea1c4e2dcde973aef8bb20a482040038f9e50f6ca25a40f337065196217754`  
		Last Modified: Thu, 17 Mar 2022 10:47:47 GMT  
		Size: 53.2 MB (53187465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec4479097720cc88d4d0e74d627c29ca560c4256a9de982a9645ded35c2ca6`  
		Last Modified: Thu, 17 Mar 2022 10:47:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c883dd14a1995a91721c19f2a8798ff1117122d30595471fba018c60cf08c231
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58842796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944033855c480e27d14790ee9224e53d2fda311154fcd1efb34fad8debcf0370`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:21:00 GMT
ADD file:993daefd4be7520217183e1faf430c4305b9c71b3521c2e5370ca812d34d83cf in / 
# Thu, 17 Mar 2022 11:21:07 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 11:21:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec9f3e0be43598d9f763fab1e013bcd1e0a00c65519d7ba374313f2534aef52f`  
		Last Modified: Thu, 17 Mar 2022 11:31:19 GMT  
		Size: 58.8 MB (58842572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f831b5d4299c4925d6d3199b1f1367c8e6085e8a3ca80a717cdef0bc2fa75077`  
		Last Modified: Thu, 17 Mar 2022 11:31:32 GMT  
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
