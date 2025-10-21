## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:497a0835f07afb7599f5b08263322303158925ef7a0e6bd89dfecc7fd9a93408
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
$ docker pull debian@sha256:ece360ff2b3ea717be29345370fb3b0208d56c7a37edef5e8ed8dc524d536579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43a5e10e1fd6249a195da0b040d47bb7edfcef642769f9a325303421fe64081`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ce7b310cd329827c40d34f3804676b1584d9699011b2e328c10c7c711cfc9a2`  
		Last Modified: Tue, 21 Oct 2025 00:19:46 GMT  
		Size: 48.5 MB (48480568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141006561652b40939a37a2b8eecd78dd52bb2944ba5fdeb702fcc1a17a24ee`  
		Last Modified: Tue, 21 Oct 2025 01:16:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9d61e137675e4abeacade01411bd6ce8873d6b7e9083254c9fada379a957794d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4739e40ffb53a04661b1861eb1ce03371644cee7a65cdf6e8c35c9232805c33`

```dockerfile
```

-	Layers:
	-	`sha256:c6f2e52c0a4b6634bbf9519d716485b995dcf2c55a321093bd18e1b21f6a4309`  
		Last Modified: Tue, 21 Oct 2025 09:24:41 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a879c9f78455db66a1d5d8ac92319d267eeb40b6f1a595ef3f2317393367f7a`  
		Last Modified: Tue, 21 Oct 2025 09:24:41 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:33d12d3be4df7f21bd858bba3da2ddf9c308468f2e1c8f919d54680474e19c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3403f6460060e1529ed23539d428ccd2d9b3237c7f239c1c0bc5e117e7f697`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:84739c0eaad5fe093ecdca6fb6fd0ad8eb5367a30e886ed67ee06e76dcee35d6`  
		Last Modified: Tue, 21 Oct 2025 00:20:22 GMT  
		Size: 46.0 MB (46015584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c055477f4d04700226f2d8a1e61fe3e498b71ad8d8488bca98005857e5ca32`  
		Last Modified: Tue, 21 Oct 2025 01:16:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f70fcd8e44aca1f498493bad159e7901847808c5ecb8c77a43b45abad5bb504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd6906c699c3a9940b6089d163273dc8f9ce44884b1ccaaaa4b96bacc7df16`

```dockerfile
```

-	Layers:
	-	`sha256:c9e3f99cda1b6b0aa06cbe7602582e7ba6041df4432254baa80853a606d4177c`  
		Last Modified: Tue, 21 Oct 2025 06:24:19 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f90babd9211bda1ac6d5b6664902f2b6110ccce22e6ca332a0f32ada6a87fa`  
		Last Modified: Tue, 21 Oct 2025 06:24:20 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3c724f6702cf01b32b276f54bd0dda51705332db5369b90e651f06f10bb75711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755ef635e042557de5755c0b52c20766c16e418d9c7e2a89e80417755591cc13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a9307e8b877e052bff0e4a0629925ceb5984a5b8a7c75ab9e395cbc7bc6ef17`  
		Last Modified: Tue, 21 Oct 2025 00:22:34 GMT  
		Size: 44.2 MB (44195915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb93b48f8b2d5c16be5c2c6237c7766fc5b4b9323341a60887f13cf48fb771`  
		Last Modified: Tue, 21 Oct 2025 01:16:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:78e75d1d518515585a93bfe7b4a41d53d054349b77dcd9c3a5fb0b56eaca157e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811defb2218d7a2a8be0dc2fa6cc1a5ff974a390adc59cbbc3b5739770f3207d`

```dockerfile
```

-	Layers:
	-	`sha256:377e5c3b83cf00fe11e11b582dd9448e44778974499c409a2ab53451d911bc5a`  
		Last Modified: Tue, 21 Oct 2025 09:24:48 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42e49f5a854a6c8a1f23b2a4f7c72c2654c3e504adbaa7fb395814a4ea70cda`  
		Last Modified: Tue, 21 Oct 2025 09:24:49 GMT  
		Size: 5.9 KB (5908 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:65171520bcccf31ca168921bf4d006f2a31b42a34bd67d190fdcf024beb20a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f1fdd477522a6d5cfc676d748bd9b0d36a87a1c6403458b3a2baa7cbb46414`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:077b78175c0b8682aaf65a91890efdc6d7ba2ad5e084cba718c2cde1bfe83f07`  
		Last Modified: Tue, 21 Oct 2025 00:20:43 GMT  
		Size: 48.4 MB (48359000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aeab4ec1c78fdc793468965c81c4058f93b298ceedf599df0f40eae59f8c4a`  
		Last Modified: Tue, 21 Oct 2025 01:16:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a3d7951f68d24d03064a78878686998517f4097aafbfdb8fadb567772e28290d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c2fe2da6a612cb5833f1c7fea3f44e875f7a14cffee4d6f881a417dc04562e`

```dockerfile
```

-	Layers:
	-	`sha256:45d4616615f7c9b76d2583075f1b161d35580dc18d5425d75305ac0ad6b6db18`  
		Last Modified: Tue, 21 Oct 2025 09:24:52 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23c661174f12fe12682d1b42ca485e44e4f5c595c3c98cc45904c22dee78bf2`  
		Last Modified: Tue, 21 Oct 2025 09:24:53 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:725d44bc8a6b7e06574c7ff2e3c6bacc4daedab0e008441b76ed1e29e083ab61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a54acbc6cd25a16cd9fc18834b530e0d2075bad58c20aea8121417b4d9a241`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ea026a22058b4382e06dabf4998a6da41c0ba5da915ab9cb54c6249648097867`  
		Last Modified: Tue, 21 Oct 2025 00:22:28 GMT  
		Size: 49.5 MB (49466723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d96c4f9720d345245a2fb3ebfc8b829cdc09300c7a71e32e686b179eeb29aee`  
		Last Modified: Tue, 21 Oct 2025 01:17:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:701d01f5389ed223d60b9609f59c94d1c877c56e673e2669e57edcb4af8c7933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d5028f50799cb4d3c7b0f53acf1082c5fd31c9cf99b4524ecc94e0dc02040f`

```dockerfile
```

-	Layers:
	-	`sha256:e3464f9171594f7418d1eff557443a5e50a1bea083778b38c2117a8e1427c3d6`  
		Last Modified: Tue, 21 Oct 2025 09:24:57 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad1f0fb53b8db99fe4d45d90cc46ae222d53846b6ce82a16fd56ab51f15f547`  
		Last Modified: Tue, 21 Oct 2025 09:24:57 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:04ab1002377d156d7b7b20369530f0409178f2984f669efd12694d3cef87025d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524c3b20ffdae6e190df78b1dbfaf26b6f68531d4b97b251113d248891db0c27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ba815bb7070e4e694b9ffe09db23feb8cc4409f638580b44be95c6adc5f208d`  
		Last Modified: Tue, 21 Oct 2025 00:20:42 GMT  
		Size: 48.8 MB (48760749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe900418eccb839982f0d31aa661308b5d5f896c78935a5fef339d0265b6774`  
		Last Modified: Tue, 21 Oct 2025 01:17:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:61890d096ced4d8eecd9759d5e586818efc84fc9f481d8e5a29bb62f4d4d0cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cdd6bd4b5573c8ec2e0bbed764b2b265753f8e5a8d83507a45b11e1c33f35c`

```dockerfile
```

-	Layers:
	-	`sha256:5cc6b11e2e1cbd4027d52d59b8aaec3441053cc8ea8236299f439dfcf96e05a8`  
		Last Modified: Tue, 21 Oct 2025 03:27:58 GMT  
		Size: 5.7 KB (5677 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2d30b85d171bddb0df1875068bf4afa7196b47cf153b4475f09ad5ab7d01b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d02d758a3eed17bd2e7f87642de0adb2944aec9e4bc953bd65e45dd6b0528ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b8d432a6f4cab1a53781c3fb554c1a8e7c299a62ff180921e034c12166489150`  
		Last Modified: Tue, 21 Oct 2025 00:21:52 GMT  
		Size: 52.3 MB (52326789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebe048295ffbc0adc68c9650b83ad47c3b09b05c81dbaf79e61b8c08e43916c`  
		Last Modified: Tue, 21 Oct 2025 01:18:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8b7b2f8f50fd89b2c23fbd33eefdf4fb0b38bac11f0b2afe120c6fa22cddd549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761a0dc175c804000dfc1ac932208e4680fa5b965083fc2508d14fd5803a9ecf`

```dockerfile
```

-	Layers:
	-	`sha256:3a004574d8992aa99a03aef90842216a7bf7744e9cdd8d993a6798192e5e7e53`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f840b485cbc46a4d0eec42429b3559a23cb60736c69585d221f52f6e3d8f1b1d`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cfdbc7d0a34f1c5b8aa8a885beaf8013aa052e62428eb50fcf0ee849b56dd9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633298fc133bb5d0b621bef086e79874d77d0fc57a8e20e773b10a2a3f9776e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac5319e24b05db3522476dd009c8e3e00181d2ef24813ab4b46d3ce75223df28`  
		Last Modified: Tue, 21 Oct 2025 00:23:23 GMT  
		Size: 47.1 MB (47137528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27296d06bbb2114f2c6da323e2530db41fc35ad8a13803d86e451dc71c5c8994`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ff120fae08ab3680bd36b0ece1e1e7ecb20e3fab96b817f4a9f8ba263a549b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80514674f579076adc84bb5a817ddbc1249eaf62f6a51ffe431e6e4cc33878d`

```dockerfile
```

-	Layers:
	-	`sha256:46306e982ca99df5285686679a70fe6405fe59eb29672955c9a762c9bc56fe73`  
		Last Modified: Tue, 21 Oct 2025 06:24:35 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a364f7a85afb144aa848ed07fbb5fdc9f7c26fcc6469bc2049dca5bc2665cf55`  
		Last Modified: Tue, 21 Oct 2025 06:24:36 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
