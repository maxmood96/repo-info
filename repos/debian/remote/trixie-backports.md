## `debian:trixie-backports`

```console
$ docker pull debian@sha256:d1b8219a71c48b707ff9b28b808609db567f440f0bdcad8fb0fb2f4479b6b4e9
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:e07a0c906e1f8060a6c71849d7c5e4aed2c45fbc4eab6050611ac61e81a8d759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49279754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd4ca830ce2b5995ba290d65d6013a9122fb6187b04449e8969ebfbc0fca3da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6484173975eef9b3a01d2f044c0b4702952feac305ec73b300eda708e1de405c`  
		Last Modified: Mon, 08 Sep 2025 21:43:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:09c6b848a2cbd8f9996e10d6efe345fc1c759a163d315639b232b67d5535e2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7842cba34854bdd9c71236878adf6d6c912fe4260aa5b4c1d77160017b6a96cd`

```dockerfile
```

-	Layers:
	-	`sha256:86fb0203ffa056e3d682b0ad33700a9d376c9947825023c6e6f39858528e7faf`  
		Last Modified: Mon, 08 Sep 2025 21:31:00 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780dd37311cd150eb1a9719631915d29659fc17d2362cc6983efd10be558595e`  
		Last Modified: Mon, 08 Sep 2025 21:31:01 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5d3cec49763cd62127085b8a7c182136ac244e76fee78d4f42dee1e3d8e466e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684f480200763b558af43f35ed7a8e47ef12270c1102b055a8a7ad7439ab954d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:93fee7f039682b45509657d20627a8677376fb460d8b9d61131616286dad7986`  
		Last Modified: Mon, 08 Sep 2025 21:14:46 GMT  
		Size: 47.4 MB (47443594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6553c4f377502a203df260c144b5dc70cba9b3c83f43b03eef97e562cea83a`  
		Last Modified: Mon, 08 Sep 2025 21:55:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1a7c5500805f03ef73f5eb8543ae888cc2d546f59c0f8f6a0e97beb5efcc4244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbc283bca89f6e3c17dab59d836a18d5ed0d777cf228cda2040133692940a97`

```dockerfile
```

-	Layers:
	-	`sha256:b0e3f82494ea13f809ad508eafe1ec73e889f07244eb5d77ab487667c12b3e99`  
		Last Modified: Mon, 08 Sep 2025 21:31:06 GMT  
		Size: 3.2 MB (3172907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffaf4fe2af13e0127d7513d34b3aeaa73d8823b1f89f334d440057d496c1c8d5`  
		Last Modified: Mon, 08 Sep 2025 21:31:07 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2dfe0bbc666b106b5c56ca5bfa037f5244db3216bcdc452a38b6d27232f9b184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45711940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c95b2f0ac60c62f599f83b6a583f7f742ff4ee15819cd43a699539c828f589`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f7fa35eb51143407208b4b2a8933de77f1fab558e6d5886df149523aeaaf7`  
		Last Modified: Mon, 08 Sep 2025 21:30:59 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:339214a7e8ffab5d452267e9877ef7a686d8ccc66b067f0c0b496f857bc97a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5590ac3b56304cb964318d2694f9fa0c03f2a9a633c574178769143307c0d`

```dockerfile
```

-	Layers:
	-	`sha256:e030446b6d5e22cdaf17444538de4c4d27e534dc9a8faf05a855a33074dc4cdc`  
		Last Modified: Mon, 08 Sep 2025 21:31:12 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68385d264358b80d0a7b6615cf40299f7ba5710b3a77282bde51fb40beb8ee3d`  
		Last Modified: Mon, 08 Sep 2025 21:31:14 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e057343afae898b19b0c83e7fb3f73a19819580646141dbba631b49bbf2d0859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49643970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3e09999db3737bb5653d5cb6f9736216d7cfb481ed1896426947067833f53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8c7aa8d0f6c4a945e5c8efe609a9d94f5dfd977ea61bebdf81d51263bd042b`  
		Last Modified: Mon, 08 Sep 2025 21:57:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c8f301014f0b607c33f8eb5f780a05b4844a7f6d5496addbcc0385bf03cfa49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9699b58230b40f6cdc599ab84ed8c6a0aa7af4d31e3bf389cfafc8c6de8ae252`

```dockerfile
```

-	Layers:
	-	`sha256:529020c999f0b2369259f482be71b289ce8f79be8983b7e28ff764654849ebde`  
		Last Modified: Mon, 08 Sep 2025 21:31:18 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a41826519a8f0e24ee9e86333e1cec2c971dccb643fa03a60a79130c00d2d12`  
		Last Modified: Mon, 08 Sep 2025 21:31:19 GMT  
		Size: 5.9 KB (5894 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:846168f48e96e6e5f7f06062a5e3b49bdbc4738517fb563d5c1ad324f8dc323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50795174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104487c8599d2dbb0bf6422290c3974aa0d386b5fa911aab9bbedb90ee3def0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8f0f605f86e758b73b0d3362fb36eae1e1cb2f323db491c61eea3504a9a965`  
		Last Modified: Mon, 08 Sep 2025 21:55:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2d956bceb879450ceff0bc9a5d9aecc84f4a01c21866a66c54e37f7f3246c195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ae02e0e9d7f8a480dbeb4b2486adb5979f58a42c50a1a665d509045deffbe`

```dockerfile
```

-	Layers:
	-	`sha256:6a3125cf644695b7a44accd5fb1a96eaa7bcbe962d30f20f43130167fb932232`  
		Last Modified: Mon, 08 Sep 2025 21:31:24 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552a06a63801edce5a50fff0136acffe4c5138e5bc8b3073d369455fac0919c7`  
		Last Modified: Mon, 08 Sep 2025 21:31:25 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4a00ba346e9808dae90bde530e8e8d35a20532e436a58c13c28e6e3cdbaec31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53104656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4ddac24910530253979e1deb0437e203ef6b01b180a6d528a5292b2b29c266`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66d95f8d42c7a234997f80ccbad8dfbf679b3ed63e0a6be2c1fad00a2a53a2`  
		Last Modified: Mon, 08 Sep 2025 21:59:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9d518ab49e2cf0468476c8bdb1f94dfb6c9fb111303b9bc2d68276ff4d699e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075c2b4e964d9415cdc5db9ccc51a6eeb6d2c650a221b3463a28c59f6cbccb6e`

```dockerfile
```

-	Layers:
	-	`sha256:f533912d0de0b42fbc55ac5365b1c18eb1139ac2c384806d2f63d62a053dbaea`  
		Last Modified: Mon, 08 Sep 2025 21:31:30 GMT  
		Size: 3.2 MB (3173481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056c9061ea207c5777c0e0425318bbdad8016eedca6cc8619e772995533f530c`  
		Last Modified: Mon, 08 Sep 2025 21:31:31 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:6e2dd89d2f95f9761d824b13dbbea5720a21ff19cd25f4558f7dd16405b8c2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47765671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73396a1ad814b833022cd0efc11454ef71f6a14214a542d1de9fd0ecb49f37cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6161aeaefb07f8e55ef05510ab0b089e5956caf7f11a7164c32b9f5beeb9a6`  
		Last Modified: Tue, 09 Sep 2025 15:22:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:22c0e54f2783a427dde1d1e4d9ea61852dad788533d864160e44c1a8ccdb40ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ea4debbbe2d9b0876bdc0e44a266af0145e560fd3170b8e73f1d6ab475d9f8`

```dockerfile
```

-	Layers:
	-	`sha256:34f1878942f23862af1b52d8f4388283955bc37f2cbc6e3e84dfa3aed460f07b`  
		Last Modified: Tue, 09 Sep 2025 18:24:56 GMT  
		Size: 3.2 MB (3162293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a186b59060f948dae921a213fa0ad422cf6e7719941e4089ee9a10edf4055c6`  
		Last Modified: Tue, 09 Sep 2025 18:24:57 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:2780edb2449e8710d4e204f2dc7e14efb0a248770a3a5e13f3bb51e31adac656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e33861d8362606fa752228670f4c8c166e49a92a7aaed04a3a086c8553843e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622809380b98b7e4407f3dd4bc1c6e0f78f242a5a1501c89fb7c17ce2e5d9893`  
		Last Modified: Mon, 08 Sep 2025 21:56:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:86e900e650c2ecb259bd2bbf996df62d0b562fb97667aab0fe17b0dc270f23bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a194ceed5e93718ffdf9d7b5e60dd5d2908117484b9a641aaf40eaa72d33b2fb`

```dockerfile
```

-	Layers:
	-	`sha256:821ef3955a1ce71b2129b3083d528725d132a12d72c3aaa718f12abb4a35a4e8`  
		Last Modified: Mon, 08 Sep 2025 21:31:40 GMT  
		Size: 3.2 MB (3171417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d61a65f5ca39894d128101317cd9fd79bd44d7a0a59904be1896c2be38251c`  
		Last Modified: Mon, 08 Sep 2025 21:31:41 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
