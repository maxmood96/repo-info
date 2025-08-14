## `debian:testing-backports`

```console
$ docker pull debian@sha256:8694c348493fa53492f10833cf617941cfb9cdda20bccd870d32660c3f8db09e
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:48cd898ee6e311064d43cadefcfa7abf9db0b91f8e64c11292c1828bafbc284d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49278499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf32b942568201fbc03d5e481b883176e3bbdfbd23f59c987b6a483e8c38525`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:183c6c07933c216179cd1e895ff01916eb3110e79f0745835a0f37a59a4e1217`  
		Last Modified: Tue, 12 Aug 2025 20:45:06 GMT  
		Size: 49.3 MB (49278276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f834931fe92c6c24c0dee5a1ba272d3e510718a2db7cf804559b0b324e4c35`  
		Last Modified: Tue, 12 Aug 2025 21:10:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0e851f5c3c9f964decb1750d5aaddf0cf2435631dbe4c362f3474e6d02a4d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2345e3778f99b3fe985d74c4db3b5ef6fe40fd58fb183d7db147eb3554a3f31`

```dockerfile
```

-	Layers:
	-	`sha256:351060cd4643b5dd9bc1b7970400e09cb56432c3b2f23d86cf9ecc182aa6b65e`  
		Last Modified: Tue, 12 Aug 2025 21:29:17 GMT  
		Size: 3.2 MB (3168491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9edd6830f154eac7087328f204c3e97fb8128b50b314419cc9a198da5fe0d11c`  
		Last Modified: Tue, 12 Aug 2025 21:29:17 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6a052565009b599e7653f9ef7a300532c5de4aa02fec15ac0d66f9f0aecafbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fec8022d74d5c51279b44df51825ad333561157513c5d5f0433a95b86fe8a9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9a691f9496288e214153087c04ec243a217b23ad928387b4ecd1894bd025e8b4`  
		Last Modified: Tue, 12 Aug 2025 20:48:12 GMT  
		Size: 47.4 MB (47442420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f998aafbae6974becceb4131714a52952934ff035d9b836e7b0faab51012e`  
		Last Modified: Tue, 12 Aug 2025 21:11:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d29ed87d917ca18068c788adbc40c11f20bbe4478374c19b25f7dd536987e4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ba3a9709fbb9156038381fa2729ecc3168cb376f6ff8952f975d26b7f6baec`

```dockerfile
```

-	Layers:
	-	`sha256:9f17b84e257ef43a4067244ae82cb328b64ee7fc4bd00f0f57b9625fbe79e12e`  
		Last Modified: Tue, 12 Aug 2025 21:29:22 GMT  
		Size: 3.2 MB (3171428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ffe9c2c95feec0951b162334255abf259fdf8780a7302fe4a209404c7dbb4d`  
		Last Modified: Tue, 12 Aug 2025 21:29:23 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bd5fa2e2335b83b901e68761fa4e5ddcad4f30716f7629b2e64e4b517d8bfcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd62d00a7ecb74b9a2e308c5c3774f2520c3b68aab1b04b32b555bf95f7f1d55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a6bcdadf631cd6a0bc90b370d69674c6c98e72a7aec5dc239920942440e2dd66`  
		Last Modified: Tue, 12 Aug 2025 22:18:56 GMT  
		Size: 45.7 MB (45712626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae378ad5fbd0e0a4953ca6f0c3b78baff1465f2d23a22401f0b436c64b15f91`  
		Last Modified: Tue, 12 Aug 2025 21:36:09 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c4a08070336ee12e2f1f6bc76b88a3d0ab8eade3913f0d2ff0723710c3b3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380207e0b89b06dc80e2a66b1eebddf27b15cf03af2093a4c968c52327a2b1d`

```dockerfile
```

-	Layers:
	-	`sha256:311dc26ee254785dbadfa32fd358dd4f3dc1c7ef25cba5228b25081d92c2e111`  
		Last Modified: Tue, 12 Aug 2025 21:29:28 GMT  
		Size: 3.2 MB (3169865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d9dd581417b7e8fa4631e1f2f745c7840ffd981434f0809c8f6cd35ea26818`  
		Last Modified: Tue, 12 Aug 2025 21:29:28 GMT  
		Size: 5.9 KB (5886 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ca47617dca02423fcacb556648521d077c5f36a6db1db1c5e6c928c6be6d20f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49641826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b21ddeb8b3c344d9e5b0ddb391fdd28558552366d4b5cc15e44f69129681d33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7906ceaece39d18b2e7c69126723c225ce46b2550c6e388f597fd687b30b7ffc`  
		Last Modified: Tue, 12 Aug 2025 22:11:59 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31754b9471269f0e84718d835d4bdc0abc6b27041978c27351ca1e259113256`  
		Last Modified: Wed, 13 Aug 2025 01:51:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:93e7b65088373166a76b9818b827acd924cc44d06524036582481ad1451a48fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c007c6316b1bb2adac6f4a25c53efc1676eb6264d73e74130f70ceeaffae7d82`

```dockerfile
```

-	Layers:
	-	`sha256:77ede9908c7735f9f8be8705af2ba346f0c0854c117135910d8c639ee15c9fa6`  
		Last Modified: Wed, 13 Aug 2025 03:25:38 GMT  
		Size: 3.2 MB (3169972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b1ba1c7b78ab524eb392708cd957df631fc401479f10201ef117a4ea82767`  
		Last Modified: Wed, 13 Aug 2025 03:25:38 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:72364f31746be5f9d1f2aa304bb5c105ac6951872b3270c08bb8dbb4f13621fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50794479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145eb29b5a4774c59cf90bad7716daff20811226838c0f0e253782ceaf0eff05`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b962703ec9eacf4d1b2c7de265b0e67feee996a84441129dbac74b3d66811b98`  
		Last Modified: Tue, 12 Aug 2025 20:45:07 GMT  
		Size: 50.8 MB (50794256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1928d344fb338fdb30946e597b3d3ac3edd317624a830e7da131d57a0a7ef61e`  
		Last Modified: Tue, 12 Aug 2025 21:10:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:738e415db68ce9e5a915bfddc3753718a46475d181cd058d974c418845d55f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23eedcc43452673b2e9f3f53872ff5ba8a866c939aafa9b5ea81c813045e8d7`

```dockerfile
```

-	Layers:
	-	`sha256:d072c25d8c0b407963ec310025851e480463535007ebe944092263c147bf7fd4`  
		Last Modified: Tue, 12 Aug 2025 21:29:37 GMT  
		Size: 3.2 MB (3165694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997381622f497223a1873fc849f7cfac68d049135153a06fb66c326e78141543`  
		Last Modified: Tue, 12 Aug 2025 21:29:38 GMT  
		Size: 5.8 KB (5818 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ff96278bef120fd5b271cd8350d6e02384253d0a87b8d94ab4c9c58bbc725c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53103599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc081e4fea6301d4535b7067ce96fec2e7eb9bb63cefcd9ddf7717a19ae77e2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e0e720fbbf7674e3333bf57c0ffa5840d5f88cd640f2eef04ae4e830fee84e14`  
		Last Modified: Wed, 13 Aug 2025 12:02:08 GMT  
		Size: 53.1 MB (53103377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d5047b67dff4dd5542628dc09ba629568d16ef134b2850cc18e2e55c919278`  
		Last Modified: Wed, 13 Aug 2025 05:08:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:db6d2332588442b7eb0015c6b1cc0a5c39db5b13b42ac75014e21b3f6183df15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d49de9f27acadb254211b37dcf52b9c730a2bfcb9fdfe863b7834e794ae543e`

```dockerfile
```

-	Layers:
	-	`sha256:20ae82498b882a024b1ceba8853d8c34d5ea12aa4b69866a4bb998bb23b6e08b`  
		Last Modified: Wed, 13 Aug 2025 06:25:00 GMT  
		Size: 3.2 MB (3172002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804d2a2640ebd18274429029d604b4c74a7f317ab5de801bc1046d61827c4ed4`  
		Last Modified: Wed, 13 Aug 2025 06:25:01 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:6051ab1d15d0e39fc9c8b7b525340c443c589ed95b9b38070de492db2334d083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245a475968fe233b91d68da01c28b4592b14b309ca578802ffdfa07e0fcef47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cb9a52a499db4647b784ad4549ec7a50c9127ce8c522037fd781151ac4a51159`  
		Last Modified: Wed, 13 Aug 2025 01:10:02 GMT  
		Size: 47.8 MB (47764300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd75b191917817098e283e27553ca30ae87b913559c536e7ff6cb31cf44881`  
		Last Modified: Wed, 13 Aug 2025 08:20:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4feabb968fbcfa6e5a219561c35a0168c18e0e96926573ba00c845ccd37d557d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bba2a6205cf66764af6437b878c21abef3e7827353a3d1cb7ee7a267a2a1638`

```dockerfile
```

-	Layers:
	-	`sha256:7a4410c14a529b6a6e4b7f7611dd991643af017aa9270117bbbb8b2589a94745`  
		Last Modified: Wed, 13 Aug 2025 09:25:05 GMT  
		Size: 3.2 MB (3160814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825fc194efdb876b05dff0d5b4e54072dc7c9e7a7cf3d14a9f0efb85ba523670`  
		Last Modified: Wed, 13 Aug 2025 09:25:06 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:6f9948a478a01be44c3625ce78c96119d7194275166cb1e16f25d219147144de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49345381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483601ea7a553127e77a7ae029a7bb18705c4e199e0abf714e664ee68c513618`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e3fba30a53b175f7d81ae2ba7c6194799d01dd14bf5dc4efae9e8516a4d5579c`  
		Last Modified: Tue, 12 Aug 2025 20:58:13 GMT  
		Size: 49.3 MB (49345158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9ce3915281ef3a1d7d15b517b3e8f095985b42a846286c8927b6b81e3f8715`  
		Last Modified: Tue, 12 Aug 2025 23:13:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c0a7a866ecd686b7f0fb6856f855dae0d95bba724f080d971895fa51d01a24a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c14a87a8719b0035dedb862a0fee7b2cf64c33884ba28e6ca525cf5736ee33`

```dockerfile
```

-	Layers:
	-	`sha256:d33d65b2fdc3f88b77b597cdb15549f9c99f232db5dacc40d46cd50af899d74c`  
		Last Modified: Wed, 13 Aug 2025 00:27:19 GMT  
		Size: 3.2 MB (3169938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14830f5b80269571cfcf94a0c659d4c7d5762a869a857034fc4c50f4ae973b57`  
		Last Modified: Wed, 13 Aug 2025 00:27:19 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.in-toto+json
