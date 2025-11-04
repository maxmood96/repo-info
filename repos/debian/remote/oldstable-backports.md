## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1546863e3dfcf12196bc4d60cc966d65369af70543e3327fb2be88adb910406e
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
$ docker pull debian@sha256:b93fc122fd5b84ea3649774a748d4004a8e9bad4cfef0b0f89b53c0486e89f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b3cc389f519877b77de9a8137c61d8b3cd023de94398a10bc90717ac2b07e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 00:20:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba3e984208185eebf501e446e9046cc294f49018e87c7c8b41687c210902e1a4`  
		Last Modified: Tue, 04 Nov 2025 00:12:43 GMT  
		Size: 46.0 MB (46016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3a0419f7f98d55c4251e0b75686b8db51f0a226bfa868b4ae774d8dc3b9cec`  
		Last Modified: Tue, 04 Nov 2025 00:20:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50c228636279f79a49de2bda8dd6fa4b200a0a287e274a613d561cfee1f72a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b1295d3f401478d08cad6f4055ba1a44d4e69cd3f52864ab1600b23064b126`

```dockerfile
```

-	Layers:
	-	`sha256:9f57ebe728902dbf7403b8cbf4cbb1f47e7e0e2acafceede7aa9d0423a2635ab`  
		Last Modified: Tue, 04 Nov 2025 07:28:38 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cae2b5b79cff1a050f3e233a316dfd5249b37bb23179ba6d602ed9b3497ffba`  
		Last Modified: Tue, 04 Nov 2025 07:28:39 GMT  
		Size: 5.9 KB (5866 bytes)  
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
$ docker pull debian@sha256:39f51cecbd7d51615d83c0b2aa58a5705feb523e688304cc2dfa9fa608b2bcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4acb22665c2a6e77753700e823dc0be4033106b23ef9451c6f47d9333cdebf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 00:18:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:deb63f79a3e780f6c895b686d3acd3362fbff1594f406951d9ab487ed8966203`  
		Last Modified: Tue, 04 Nov 2025 00:12:31 GMT  
		Size: 48.8 MB (48761283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7607f678de5aefc085176faa2760356cef9a8904120c19c310a69765b6ae5`  
		Last Modified: Tue, 04 Nov 2025 00:19:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a1f531d67d06fdffec91fb37ae5d743e61e69811de4d5309bcf211547dc9a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e717057119add05375763c2afb4512bd68e60aa901e948586c9ca7ba05811d`

```dockerfile
```

-	Layers:
	-	`sha256:5b0ca025be5499d38d98e8e1ab60ca89a37fafa81e7a5bd8affbd4a710edcbe4`  
		Last Modified: Tue, 04 Nov 2025 07:28:54 GMT  
		Size: 5.6 KB (5634 bytes)  
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
