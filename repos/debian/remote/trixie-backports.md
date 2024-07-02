## `debian:trixie-backports`

```console
$ docker pull debian@sha256:8febd09defe53d6f5f58674138c92ddf823a97ba4d543b7e25cb45a253a0a846
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:581b44645604f916d48c439eece9d253aaec112d76ff455a0ebef06b82d2a974
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52277986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904bd675d95580f3a536bde25940f2d07cd59303062cbb8ac609e610fba18385`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:33 GMT
ADD file:fb6f38952a56f7cbaa95d8ba94e80e8248829fe8e6ea398f1cbcb89942bd1547 in / 
# Thu, 13 Jun 2024 01:23:34 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:23:38 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1794c1f4707f1bb7231b64706e50d1615843d67660a3142771596a820e257b8`  
		Last Modified: Thu, 13 Jun 2024 01:29:39 GMT  
		Size: 52.3 MB (52277762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558367f762493b6467beac3d043ada333067688a77ef29c0f1aa1fd08f6457fa`  
		Last Modified: Thu, 13 Jun 2024 01:29:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:338ab480c9d8883f4e59c8c8638d156fcc2535164c313f5ddf9d8797a1c2cc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49521645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c6a9cb9d82e900dec4c711b27c9ac97b1fd1d1bf03ea1e4c20cefd8922fc50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:52 GMT
ADD file:c318229166795e4eb716c1fa6af23bbb2d4ecba024b60f621a291810a3a401d4 in / 
# Tue, 02 Jul 2024 00:49:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:49:56 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:000d0bc5723ca659fec8fc6ce252cb52307971eb476903fc3b9275de15df06e8`  
		Last Modified: Tue, 02 Jul 2024 00:54:39 GMT  
		Size: 49.5 MB (49521421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db1eccaa44ea57384084dce90c1ae9ed3d94de923311eae9ade39e60b856f9d`  
		Last Modified: Tue, 02 Jul 2024 00:54:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4b862bd381df2bbc7d07df854caf3aa45e0891f557daa474f4effb4fec9d4434
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47028281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee426fa9eea7814f09e792ca70133d82d6ebfb9f9a090bbdd9af5d0f60de277`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:43 GMT
ADD file:527e478975b1f859c9421d232809fcdad4ae845a2591655169c3c0cbd9556cb0 in / 
# Tue, 02 Jul 2024 01:01:43 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:01:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4626e10f2b2fa1f8bd684a19417be06dce44506821e68c986c039ebcf444ea1`  
		Last Modified: Tue, 02 Jul 2024 01:06:18 GMT  
		Size: 47.0 MB (47028058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f2b4794aa28f0a40b22ebd96849741136f84faa5c20f27c93776821e4ad36c`  
		Last Modified: Tue, 02 Jul 2024 01:06:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e3e4aee671881b26b37a8f19f200709edb299b3c4683d492bb5002657283ea76
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52693544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92e687bff63f5cfea3de58adfc05fb14582857199f1fe509d1d80154a74e16f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abee659a582f253a0eee4a414366f304787c7da2d000d7ec6b64d935ea41196b`  
		Last Modified: Tue, 02 Jul 2024 00:45:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:8ca2dd40324902c88422d62b26d7e88c887551e36260487e6936005ae5769b68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53333401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167f1bb48699bbbe54c19e6db162ff61f3a3344270dbf7fe11f26cf719cc0776`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:52 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Tue, 02 Jul 2024 00:40:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:57 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a4650c9182de42a1ef5cad8a13649890363bf3553955334ea0fd17b11f3de`  
		Last Modified: Tue, 02 Jul 2024 00:46:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:1af7cda1dcd47a644de2d976cc75399f1a59dfde95c7a3f684761a38a4308100
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5863dbd87ef93aa58e95ef884077eed8fe8ca1e80f7f4e0d506823c757aa41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:26 GMT
ADD file:4f8e64cb73f0bac5394470bb779521bb9b544dd7513205d8a870b13ebce84cf0 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:17:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:82cf140ea060591c60ad59c1c2af2452121c8cf77b184829ed04be1d69b176dd`  
		Last Modified: Thu, 13 Jun 2024 01:29:05 GMT  
		Size: 51.1 MB (51137261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda84962dbd94609ae191a57f98b515216bd95fe141ab00bc273c7e4688aafa`  
		Last Modified: Thu, 13 Jun 2024 01:29:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9f0c01dd055d45a5018f29b7fd08c6a34f209f6179a738dde4384c31155f9a53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56345427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf040a4437aa66aae21a12e09abd64d690d8ce9e3f5cfae46bcc49ab5cbf04f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:54 GMT
ADD file:2befd9889f7183dff7c3af514af787c529a360a9bdb089a9e9db6dafcd6001c6 in / 
# Tue, 02 Jul 2024 01:19:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:02 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1562048ab74aa86e6df4a38c0c8f568200759fc4f56abccc22d1df342f206dab`  
		Last Modified: Tue, 02 Jul 2024 01:25:27 GMT  
		Size: 56.3 MB (56345204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5059660d89ce0bb956a44072388cb445c5ba9cd395d58ccc036a27b5388727e1`  
		Last Modified: Tue, 02 Jul 2024 01:25:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:2325d17e89bb32208772bd123eebd93bf9b4af3adb5f32beae97f58cc0b5af03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52089703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f068bb0790383ddacf83a866c5dbee5ba0ad4c82b0bab52c455db7abb076964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:46:19 GMT
ADD file:8bed729fdb05f23c2c9685e4b49aca399cccb129d549ff0cd5178ece57a34073 in / 
# Tue, 02 Jul 2024 00:46:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:46:28 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7663a7e6ec84fcce1d022bfe86b7d77ebcf92e841e95456e76280883841e0985`  
		Last Modified: Tue, 02 Jul 2024 00:51:04 GMT  
		Size: 52.1 MB (52089479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4a72ab7974324638fbde3b08f383220ede861c99935645ccfc7470f5db616d`  
		Last Modified: Tue, 02 Jul 2024 00:51:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
