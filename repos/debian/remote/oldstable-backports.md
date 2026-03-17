## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6d02e3e02f11e09ba7cbef012f5c7c4375bc94038748d0ba1545339493c34b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:b1c7f11f1a58ff473f56249c599dc7b8b24aeb9592f216a18f4f93f06555b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec36325700cf172a7dd6908b6cacd47d2ccf11ea73a97cd057c6b9ffe90edc81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:17:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e8a910903c79b093153d31ef8451a5d6c153e9beb7d0c5a8c0b019864aae5b90`  
		Last Modified: Mon, 16 Mar 2026 21:53:57 GMT  
		Size: 48.5 MB (48488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da40cdbb0427dfd6539d6621f2f3503a071dbc443b8c2055a25e7c86e8d780`  
		Last Modified: Mon, 16 Mar 2026 22:17:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82e629f155410fed58c71fd44487d897d37a781806a1079f0d28e2850ef5a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab816600d58a227f240fdf4eef14576bb97df7799f8b01cd9eaf7cc94fdb0985`

```dockerfile
```

-	Layers:
	-	`sha256:04eb16a1de56c72b48898e65add048d45f3561dbf9ecb3589019deb57de266cc`  
		Last Modified: Mon, 16 Mar 2026 22:17:20 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1ea97bd500227fa117c144f7186f98048741aa3ebb98f35f9f065fb9523224`  
		Last Modified: Mon, 16 Mar 2026 22:17:20 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:42ed10dd225714d08d38cce9d8a2be338f2872d30cde0963af4ae143fc986464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9373728c2fb3a4669dc6d72e30b238012cc50a35193f8e2a9582a35fdac024f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:15:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c5c854455a9fe2791b275a745cd9f591d67a60577a8042ba1282f9a9f9200a29`  
		Last Modified: Mon, 16 Mar 2026 21:52:12 GMT  
		Size: 46.0 MB (46021485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ea8ed7a0fa026b872d34a6c8fc135efc1ee5e976223b6665e0391d8653dd0a`  
		Last Modified: Mon, 16 Mar 2026 22:16:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8caf2a8693b4399b74cbdb6fdebf4df817273269418bd2492edc25a3830c9618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5416976daaa8e22590016626f82fd9b19fe355388ed2ceab50711316d32f0b6`

```dockerfile
```

-	Layers:
	-	`sha256:d72a61f71b749cde014c532ddc51d8f3d5fbaaf0ac2768015c6dc199663e411d`  
		Last Modified: Mon, 16 Mar 2026 22:16:04 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167957eed52e97ba467666a5de31fba32f12329be7227c96ec39240617495f02`  
		Last Modified: Mon, 16 Mar 2026 22:16:03 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:794c27803524ba9cac54b09cee549e7935eaa8d3eabf5473737d21865e89b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e6bcdb24f3ffda01c8cf80e0cb9fc020ea1f3f22df9fdd0329b74fbedbd3c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a881fa4c4d4dc3214615d8bfff6ccf5f4a480792b6582d9c5d71360507c56dc7`  
		Last Modified: Mon, 16 Mar 2026 21:52:58 GMT  
		Size: 44.2 MB (44207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1030f0f37045777dd979fb5bf97d12fe837292c5847adf1f7589d40b3c72d935`  
		Last Modified: Mon, 16 Mar 2026 22:15:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e4fa86bfd813a9b629f71b03a56ac32731a7c1ba82abfcdb48a31e4be0628c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35ac632e7ece78b6ff70663d57bb49984fd29f904db9c1b3e0f4c2ca55e359f`

```dockerfile
```

-	Layers:
	-	`sha256:4a78588bde38b856d5b353829a7dae4d953119a0a64d7649bdf8766e2776a39b`  
		Last Modified: Mon, 16 Mar 2026 22:15:59 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b52f5c2cd9a0291137d74c04585fa75ee4e6f9d9954807f7035ffd4034c1e82`  
		Last Modified: Mon, 16 Mar 2026 22:15:59 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:109d75ca9dbc37ecea545d373ffa0494e941da4faf0ab5601d9c8f1eead4b14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24814280962bec41ea705acc1e3695c12c306af2b9f3148d234ba267bc9570ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:15:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c267ed1f77f6b80e4bf2bbbcf1ca7d26307eeb2b8c5c73a5fb1da2b652014cdc`  
		Last Modified: Mon, 16 Mar 2026 21:53:11 GMT  
		Size: 48.4 MB (48373036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846a0ade9469049d4a44cae99160399f3e12f588af4fe684f5599d7cd23c2a3`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:44b19c26d178749d7dfc2cc143c3881107306d2d2df5f8a9dc6e501d0ffeb52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01c4b49dc35c06c53646b9b25d945923d43dbc836d677f2d1a5620c07c2bcbb`

```dockerfile
```

-	Layers:
	-	`sha256:281e749c5b371b912f239ae3dc613ec9f02003b80db3340fce8e52c6a50afaee`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31178652a8510bd0921dd8d526af498160f1baa564a2fc213b80c9c0941e1aa6`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:e5fb46007b885bd0b4de50560e5bfd719497e5a4558d401f0937455e8e6094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c84b65d66780f418b7cc11e0faf6797c232a87950f699397fa53ef03aabe52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:15:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:39b38030b2d949f97233337a7a26effb0cd57bbee33a7553330402c7cb684845`  
		Last Modified: Mon, 16 Mar 2026 21:53:53 GMT  
		Size: 49.5 MB (49477658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035d67eb126d9d648c20bf7071c9a1f29f130ea865d5b2517c964f2600f6c95`  
		Last Modified: Mon, 16 Mar 2026 22:15:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d162f023e7f0f0a56a0abe56d17d699e69d325832cc45d1b8df9c227c558a23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838533721a0ee39a1bf0a74497f9fe9b739de0bb59bb7b080a89e6a3e271b1d5`

```dockerfile
```

-	Layers:
	-	`sha256:184d383ca70f1dd27dc5b6657e560d31513ef28b4dfc44ad559f4e0a7b12efa3`  
		Last Modified: Mon, 16 Mar 2026 22:15:36 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11aaf6633a21fc673dcf47dbb97211b7623e7e2f678e107057e52015b71fe229`  
		Last Modified: Mon, 16 Mar 2026 22:15:36 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2b31f6daddefb4834e3bb677abca190e0a0f32ff434ccdc6f05412d208dbc63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7043c93b5ee26e11ae6c0004ba662d8d6a244fbe693daf53b849c03e2311a40f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:19:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:acd77b2679668e257cfc50cf9c45358d7bf7fd8999b0502f0d199ced893ab927`  
		Last Modified: Mon, 16 Mar 2026 21:52:12 GMT  
		Size: 48.8 MB (48782295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bfb4cbfa00199b8ee3b986151741bf19e15665647321a75b730d74db261355`  
		Last Modified: Mon, 16 Mar 2026 22:19:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:53dddd0185aaadb9248a0d4d22be52d0eee0fa452a7d43e10f7edc49c300865e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e6b7accf68856bc07962a4d144a3bd99ee83784750cc691b1bcd80b1b55b01`

```dockerfile
```

-	Layers:
	-	`sha256:8381d2b24b04e3c66e2224fddcfa8d82bce3b32ed17e4fb6ec925a1465b3cdff`  
		Last Modified: Mon, 16 Mar 2026 22:19:23 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2dc1516c5a023aadc7d339eab6378331896ceb33698ab28739a5d607b34fd8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b6ac6afc619fbcca0aa1051b5f5fe3e00f9b27101bea4565e0e3a49ee7f12a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:54:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:da1317e86242c74f450b977878d2ed53f0330a33b84b0bad125028ce138f136f`  
		Last Modified: Tue, 24 Feb 2026 18:43:05 GMT  
		Size: 52.3 MB (52336802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825df5c739ff7d090f8b7200b729b097eae2ebbba2fa6f8c7ac98f06a3481b87`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97fcf79dbcf411926206d16a9698aa7566d4c3e26aaa725535a98e9a75679284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c98bdeee8b9734a299706ec6ec1d987fafa694a5e7693610d25757dead4a5bf`

```dockerfile
```

-	Layers:
	-	`sha256:7a185b3ced1a9bedd6521879ba1cbeb2b884c05a330b17c957b98d7196daa2a5`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98903e700ff1f1294ae841e326c27d02b3100ee217e1c7fbfaea05a5cc51c25`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e4c654b2f0a41fdf1447a138342a7d4053118a904425e241e8dda4b32b0426d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5aeecaba564ee5e74f62805e2afb5f7099a3af885e853ff35d13a500c4e4e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1773619200'
# Mon, 16 Mar 2026 22:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:62e425eb999eab3bfac253b1048ef86cf78f4d7b894a39dce5b5f928525755b4`  
		Last Modified: Mon, 16 Mar 2026 21:51:52 GMT  
		Size: 47.1 MB (47147922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526bb93865b750e9e02cfbf05f3d708bf743dbf4cf41e074a4f52b9483718a5`  
		Last Modified: Mon, 16 Mar 2026 22:15:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e528b79c632ed02dc4c20a7777f33740b13fbf51db6b8d9f1d2ee3648723a55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6917f623335bc83b08ff0974d4849bb5e8e07f2e204a673995f6d15e326dfdab`

```dockerfile
```

-	Layers:
	-	`sha256:3794d51c658b72ad9b8ea1e9edd7453e0f99bb00aabf075a3a855e6280fe6723`  
		Last Modified: Mon, 16 Mar 2026 22:15:08 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11355968bf5fd028947343b85b3a399b0d149b8b1ecc81257be15429ec1e91e0`  
		Last Modified: Mon, 16 Mar 2026 22:15:08 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
