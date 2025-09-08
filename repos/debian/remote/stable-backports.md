## `debian:stable-backports`

```console
$ docker pull debian@sha256:8bbb0da0bff145f3dbf086a4b6faa5a58d43597865cfc3c06f6d149f6aaa1297
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:597f40a587b352a30dfe7ed989a020c4ac0e0c639a49947f6b77c50c1e28b0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49279753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ece890589751d483f6bfd47c94afff0003d996b55afb354021a8c4fc15519`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:79045c1f327b489d1f97941156d6c399aa987086f778b8b832e06cd33a147e35`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322c992774e8c4c78a3bb48ba970851f91d459964200285155d0f9c987346d5d`  
		Last Modified: Mon, 08 Sep 2025 21:20:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b340a41d08e13c2aa62c193887aaf60c201fcfc3d225f99a8f834d7caac9bd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b10d6d28e091b1969b8a4113e12b5d4f61b08f29addb1087d23446c5a89000`

```dockerfile
```

-	Layers:
	-	`sha256:06fa6eec8a1537c648437ce25769a6e89719d21cd98c96c04ca35d22930ce7c6`  
		Last Modified: Mon, 08 Sep 2025 21:29:29 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2b04a42e45d3db080dbc5c4f65d896bb27ca8da95f975dec1c0ea718aeaa13`  
		Last Modified: Mon, 08 Sep 2025 21:29:30 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f8407a4c0f47e99b8c909a16478c3e1d751e3ce89dac574be84d058727906471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f8e396b49c4032f862b2f42e197251636a09a4fe5478a213b659756033a348`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7ecc0b9630bbb73ce7832534f560992ffc1eee2caf4b287e721685135bd3b725`  
		Last Modified: Mon, 08 Sep 2025 21:15:08 GMT  
		Size: 47.4 MB (47443589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9265df767d334887a44d355126b8007f5976e759008b6126d83b6736aa1cd9e`  
		Last Modified: Mon, 08 Sep 2025 21:15:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:984f1d491f81a12e9e52a796f1daff653166a99618e25a5baa8083269a992354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c1c141dae69bb3aa7d9a21200e5d5698e041d6940bca5997bac865d1c4642`

```dockerfile
```

-	Layers:
	-	`sha256:4a1115719fb5b5fcbbbbce67adae63e56e52fd5b8ad9770f079db49d1a0be3a1`  
		Last Modified: Mon, 08 Sep 2025 21:29:35 GMT  
		Size: 3.2 MB (3172907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d2f011ddff6ffc66bc4e88f7647550a5dae26b03e895083183ccdfb9fc89ff`  
		Last Modified: Mon, 08 Sep 2025 21:29:36 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a206960c6e9097db1a6c5c4d5fb77fd81945920cfc4f9eae797732a692c4bb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45711945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef512d0046cddb2920b583726be74fd4da4a529ba219fd788c4a67963ec281d3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e287442e0d01ead00f024c1064528b60f9f41cf87f638e89a624f29b17105c5`  
		Last Modified: Mon, 08 Sep 2025 21:15:23 GMT  
		Size: 45.7 MB (45711723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f8a82188f811c1e05a875d4d2b5af34b30e695e27811ce695365cad76025e5`  
		Last Modified: Mon, 08 Sep 2025 21:15:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f05d31021369673c2b1bbbdd95687fbab554cf319b43a53215e5fd61198d3f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49cd2f73dc754969ee2c856abc56bc20d5fd1474d934bea73da29adf46a8f2b`

```dockerfile
```

-	Layers:
	-	`sha256:a068d5c5e193dbcca50df472a4e6ca13f4bd1e60373fc4f910515ce2acc4399f`  
		Last Modified: Mon, 08 Sep 2025 21:29:42 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f0f9e7cb192f52f306f8dbaba75834223b6e8e731e29315c106cf5587f0875`  
		Last Modified: Mon, 08 Sep 2025 21:29:43 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d10e469a50ef98568ddca8d3f855319748858a35985c3d68676248713f2a036d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49643967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ccc787a259cf6f12a9461ad37c38b452825d58461842c6d90e6b9683d90da3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e54ba093b9499aea4074b17b6fbbe50ebcfdcf57e92262846c38c929743d30bf`  
		Last Modified: Mon, 08 Sep 2025 21:15:13 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68198314c708fbe3ee3375087239b346888e5c5a7210cbc9f049b649b24518a`  
		Last Modified: Mon, 08 Sep 2025 21:15:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bb18bb2b98eb3213a76a5d52740687808689d930c853d3def275a4344b0836dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1af843bc15b4096d64fc38dcc32f3fda4d264c7ca050074792298d86867021`

```dockerfile
```

-	Layers:
	-	`sha256:8d1909e4e2aebfc4389a5ac994442c9cdc1395b2a4ef9a359e9b5a5ffb220c14`  
		Last Modified: Mon, 08 Sep 2025 21:29:47 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b904cec37a5b4fb0188b21d256bf09e3efac1cd2de6dce17108f53fe9db7d77f`  
		Last Modified: Mon, 08 Sep 2025 21:29:48 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:811b997f12eb10dd154de408514a783eb0277183127737bc2558624a5bca79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50795176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9d6b5b4ca2b8efc5c576f3b08cbb2db24e5b9a2bb0c115096c58959d68d137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8aa7a1f68238c2ca65aa910b32c2bdbdb184a405d195925173799d9a16b6f19f`  
		Last Modified: Mon, 08 Sep 2025 21:12:30 GMT  
		Size: 50.8 MB (50794954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d0e15fb0c1775ab93274321736436811976ce85e769a9dc195353483a5447a`  
		Last Modified: Mon, 08 Sep 2025 21:19:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ada8a5435028acc6fd02ba17419f24ef4b386ba24772a3169817865d6bd83ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea827f8d83169c50119f375d26f63ae612213f817c5f4c03494a2d231155755f`

```dockerfile
```

-	Layers:
	-	`sha256:56b3f3c875f5255de74ffd316407fd3c0f12d01a98f393065b144ccdcbcbb70c`  
		Last Modified: Mon, 08 Sep 2025 21:29:53 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b87ea373624a75481f59a7bf720997a1c2c3f00b7bf42f9466d3a943fcf40f0`  
		Last Modified: Mon, 08 Sep 2025 21:29:54 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:da1d921eed5722b06785fff48a7f27fe30e15704a584caf1433f6af0cf6efa38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53104655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620fba207bd0934047497e82cacb3658c64b0894ec5325b56571f509da124bb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9dc9b7543a3cbefd44560f11db218787c2733076caaecd1c0bdc6d19ef91cb31`  
		Last Modified: Mon, 08 Sep 2025 20:39:00 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1e5a9660a65fa36aa30b93ce25a5f9f07df734fd1f2018ed25227c83cf8579`  
		Last Modified: Mon, 08 Sep 2025 21:30:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:892110910c5db59f4e92f81fe8b058faf1855120636ab7c44a44fbdf6ba03d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7c985b5e751342dcbcb0e6d129986ac6377234102edb974a1b8a4a88f63543`

```dockerfile
```

-	Layers:
	-	`sha256:64452e2c83140bca789fbba16d0038694a31a56ef162cabdb8ed3269a3e3b667`  
		Last Modified: Mon, 08 Sep 2025 21:29:58 GMT  
		Size: 3.2 MB (3173481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fd1068c8f45ab24333a21fc2df0e500e1b1d850ccd3acea3f4faf2503b11e5`  
		Last Modified: Mon, 08 Sep 2025 21:29:59 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:73eff327a800783b9c944edb49ae9c41b221faa6ae848370c6e045ef4088102b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7a4ecbb8d6aeac813bffa0a620a987ee7d58f33559fdfe6102b4bc71b2896d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d3e2263364f38b7c5adbd0cec8377100e13ae4288dae026bc1360600669e44f3`  
		Last Modified: Wed, 13 Aug 2025 01:06:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf412212b715cf4fe28632d0baf548d063335f9c2120065740b0d1d2bc4e5bbf`  
		Last Modified: Wed, 13 Aug 2025 07:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:36ab098b57db7f6c2c78b2454d4f84726ae8a0b8e0550bbffb637af7fc726a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a37940182633267fc40eb4aa261cc0fc1177146e4682149c5cd8ede3182417d`

```dockerfile
```

-	Layers:
	-	`sha256:e8c8671d07b5fe4f592f4a762e68415d0c0ab4972fa2b94ebea6c52d1d035a6e`  
		Last Modified: Wed, 13 Aug 2025 09:24:53 GMT  
		Size: 3.2 MB (3160812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09a9b5e0401e80cd84f8fd6b28355950e08b7cd1ee225f02d6a103a2d173a8b`  
		Last Modified: Wed, 13 Aug 2025 09:24:53 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4ed8136b31326d4191fc2d66e791bdff312c20615d81374db76119dbad02c7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775b38221e5e2d329abd1db533dd34e81fb84bbd5318c45e0cc4c6c9c472ed1f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:584e7708ec313ac27acba3cb95780461dc9d1f8f47dd474c5a1c5254228e1672`  
		Last Modified: Mon, 08 Sep 2025 20:39:06 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ce186fc498fdcbd06e8efe1edd69545ce9a29901cb8844ef41ef1e4bd76336`  
		Last Modified: Mon, 08 Sep 2025 21:18:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aeeeecab2ca5e754da5878c3dedb3ece08aaf072b1fb73c6d13f0530ba17e409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866ad8d2cd89f922108472d5c81235bf3dcc0b5fdddda60bd2044cf6232cf333`

```dockerfile
```

-	Layers:
	-	`sha256:1e989da1f4a9e52c88e6d9ab2d8bf63e64406741e70a5f2414bd0d7c3443a954`  
		Last Modified: Mon, 08 Sep 2025 21:30:07 GMT  
		Size: 3.2 MB (3171417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16be112e5733f4455a15a0835f27f202a9caf78e5687274fa6c1d64a4545dddb`  
		Last Modified: Mon, 08 Sep 2025 21:30:08 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
