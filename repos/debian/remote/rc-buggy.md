## `debian:rc-buggy`

```console
$ docker pull debian@sha256:0ef3619fa05d05587956031014ef87d602bede04161cbea8d6d18eea1c62a512
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:692090fa0d2bd977859cadb0f58304cb6e6a64316250125fe124a9e36748cd7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffc02377ae73b2368cd228954609756ffdd4546682a2559035ed8758bc439eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b7471bf88646f833d6e3044f4ce142e3f54af7dd826307e4fa0dd941786d37`  
		Last Modified: Mon, 29 Sep 2025 23:48:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:3c13cee3a62eabe661ab9422d550886a2224677c24db4ec830d18597c54dc132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6219070f26b023af51d08bead4504c6c8b526e8a4ac16d6ad34bf95e1e662768`

```dockerfile
```

-	Layers:
	-	`sha256:4bea9c7539b9da3a4683300081113eb6e88029f9a7300259a66ed51a066c6e86`  
		Last Modified: Tue, 30 Sep 2025 00:28:44 GMT  
		Size: 3.1 MB (3127639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8181ba93328c44306b07a7a396a03e723f7761cd43b5c7f9318e8f571b08cf86`  
		Last Modified: Tue, 30 Sep 2025 00:28:45 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:df5659b3d9fa9b116e36742c2908469954830092c41eb091dc35d2a5a4c11c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46593738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d301b51deca6af4057ca24ecfcbf65b3556c5e5cdc57cae2fc6fe09af0e62e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:204bc56c72452e737a2bccff3f4208682016048e825d5ac2bc52dc2c4d4649de`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 46.6 MB (46593513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4b0048d32f8275c1074d6eebf7d2541ac0bd45848a0247c8e76c65ce1bda1a`  
		Last Modified: Tue, 21 Oct 2025 01:17:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:2b2a6d9ba0ea94bf4a30905235314a503be17c4ee27b2a54aba37e1122878b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d8ea5c377aa4d95ec4b79746f168435744a183653e4fb7b3ef5591818f94f9`

```dockerfile
```

-	Layers:
	-	`sha256:cc3a021e79bc108b92b4e0d2836d3c5a68f15e707b838ccd804c36a97866a4c7`  
		Last Modified: Tue, 21 Oct 2025 06:24:28 GMT  
		Size: 3.1 MB (3131373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb17d8a2cfc091ac0f186684eefea15cb33603e5044f59abbf181f12b6110c7e`  
		Last Modified: Tue, 21 Oct 2025 06:24:29 GMT  
		Size: 6.2 KB (6162 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:7611a63cba1c8b3975c4951644a1457b1c6f2d3b24e19af701f8e0855d79a180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44859019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e10e015f90369649a22d2c09418a3960aa2adf604abd5aeca952185925630b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:410e9863388c7a21d38fa0364bd31feaac4d5fae5c51ecfcc10007da8077b744`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 44.9 MB (44858795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69714d31003a88c9a74234179d6db8968d7281cce02af8af2e4c724972d7700`  
		Last Modified: Mon, 29 Sep 2025 23:54:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:fe2eb5e7a7d16325b47dc4efe042d0414e11fdbdc31f524bcf42cfcf5785bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61202e94d02a4ebabd4fd835a601e7acdebd0aa4f1801527982ca9c9ff3b42b9`

```dockerfile
```

-	Layers:
	-	`sha256:a77252f0f554e4661307e2deaa11ff7a8671163140d199b076ec4b2251b60c64`  
		Last Modified: Tue, 30 Sep 2025 00:28:55 GMT  
		Size: 3.1 MB (3129015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eba29ad42ed52789deb4ee0f5381786a7ad4afe2ff8e5965806cd43128f9237b`  
		Last Modified: Tue, 30 Sep 2025 00:28:56 GMT  
		Size: 6.2 KB (6163 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f809dac03f2127f45d9e195f6ca1aedddb6f6c1bc9f59e91db6ec57485ff634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a39a3f5af0c9a597598e432bb8bbf38c8e6555852642f52c63d0fc0e944a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f135b89d3b765584128aa73ab02e379394fa444af6258d5b9284c97fdce83`  
		Last Modified: Mon, 29 Sep 2025 23:49:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:438747b4596fee8fd05001ea208e6f1d4633a7fb06e8c2bf654446cc1875be1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c066a8c37d12ece50d2637ebb9ad5701c3579ca050fdad393104db85f23601`

```dockerfile
```

-	Layers:
	-	`sha256:2a5d7a16dbe58945b2eded63550070a1666f53f8789c4527aa2ca0bc12f15291`  
		Last Modified: Tue, 30 Sep 2025 00:29:00 GMT  
		Size: 3.1 MB (3128492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6798c5241d9a9aef8abe88b915ad63dca092d4d86aa66a3dabaff384cea7a456`  
		Last Modified: Tue, 30 Sep 2025 00:29:01 GMT  
		Size: 6.2 KB (6179 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:a4c89bd67a5a9c0083778ef6194d39bbe8e9db210045a048c4b7ca3bc8efc631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49686396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3055f87ade2f00af3552f8818287db47dc9d88242f5ada2c00ec1bd6ee02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ca23dc0a61d46a4395fe0d292bc4e252d7dfb816af90b224663dcddc1b8091`  
		Last Modified: Mon, 29 Sep 2025 23:49:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:f796f65a46a9c68e4658d7cfeee9c71a8a8fd4bbdb72d81513d40161b57a0692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0567e3418e4a866aee2ed7690cf1bf1d95ccd6aead28bb17d9c6f98c345bf71d`

```dockerfile
```

-	Layers:
	-	`sha256:ce86b9c04c1b577a1f8621a98bb3a6ea92bca54d788d46d41e48bca1bdf169ec`  
		Last Modified: Tue, 30 Sep 2025 00:29:05 GMT  
		Size: 3.1 MB (3124843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c423860179c2a9797c8f4db929ad9b03f9d0bb3cc28754082ddb6ca2f76522`  
		Last Modified: Tue, 30 Sep 2025 00:29:06 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:de3eb9262618a1490a6e24f078adff176b34712ce0e8fae6c7a186ec45cbc481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48586752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7371cc11cbdab4aaaf313c4dd6cc5aae546bd68912ec68837ac08d507c3501f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6dd82e8f3bb693d3ab0a24c9bfd56d40d1be2ec87a80a565bb29ebde51d7a8a9`  
		Last Modified: Tue, 21 Oct 2025 00:21:36 GMT  
		Size: 48.6 MB (48586528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116eff6bf458ff5ee108e46837b25598e7ecffe702be3c6eba90c706564207a`  
		Last Modified: Tue, 21 Oct 2025 01:20:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:affde86891f45a9fd767555813fd48a586236e06a9568d725c7a851d6e5ed781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 KB (5932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cdc6dfa4ad46c9e8a6fcb437bb03df1052ca50c7d149280c6161c92716d467`

```dockerfile
```

-	Layers:
	-	`sha256:0ac69aaf16aa71daa7d929a867956a0a1f147aa316421de283fa176d74228ed7`  
		Last Modified: Tue, 21 Oct 2025 03:27:58 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:6c50a11030a8f913ffae1568e0ba59a4a4c5f147a257c98bd721cd4c718beffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53217785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e8fb86f95839475cedf2c1dcea9da65767686b9d5ed6af749ec8f0ac1d18f1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:573dcf794048f7c1a04d7e5caace5a2fd1f7290004272bc4f3dfd960a096f8a9`  
		Last Modified: Tue, 21 Oct 2025 00:23:18 GMT  
		Size: 53.2 MB (53217563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42405aff8ba5fb66fcffb07829acb3bcddc4372ca0e6691d7a9af09cc7598e6e`  
		Last Modified: Tue, 21 Oct 2025 01:22:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:223d60e5adbf169ff3593601c5c942cc9c7bf3ed6100bf42323a3fe2d940a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609e86d7aed2ac4b22a2c8c5c38fe570b66c09425d2b7c9438e20c57c8bdf2b7`

```dockerfile
```

-	Layers:
	-	`sha256:7c4bd3c402108a0a6ac62fb3086b45fc3786bacacc465295070605f352d8ac0c`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 3.1 MB (3131908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbe7a3e0dbd8cea4664a5c30b6c99241a0c5f9f71a58e5c76da39cfcbe656af`  
		Last Modified: Tue, 21 Oct 2025 03:28:01 GMT  
		Size: 6.1 KB (6131 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:00646d1cd1694894dc8c9ce49d26da6b5eb787ef73fa4e0447408c63670bfe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46705395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e1b36968a8a8d5e34bbdec603868c80c13b7eb9a32ab09fd4455d7d3df5e26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2be9bed11e9fd66165d84261d66ea19eb2c82eac8e67869aa7908bd19fd9be21`  
		Last Modified: Tue, 21 Oct 2025 00:25:21 GMT  
		Size: 46.7 MB (46705170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c587c9e6cb38e42d0c4f9e9581d91514d328bf148032b1a76c52cd641d364f94`  
		Last Modified: Tue, 21 Oct 2025 01:26:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:ad32e358d6d8e760769ebe9af2061b302db0de79e2a810dcb53a032a196affff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3126849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f869ff25d284ada4a794d66dda9bdccc0243a62120805bf1f84cd320fc5870`

```dockerfile
```

-	Layers:
	-	`sha256:61a39b0f7947a034c1b93cad5d925c24dddb3888268218c45effeb1b6e4f8609`  
		Last Modified: Tue, 21 Oct 2025 03:28:05 GMT  
		Size: 3.1 MB (3120718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938bae4fc7b0ece11dad6d28be78ec063fd9c4fa97ebb64d9692f87dfd9a5847`  
		Last Modified: Tue, 21 Oct 2025 03:28:06 GMT  
		Size: 6.1 KB (6131 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:c66b3f90122bf92c76b69f7c16d2c4eaa183efd85f0aa415066e5d060bf87595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48267419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ab8a0627fccc12709f064d369ed6ccf0151327fe145e466a04ee836dad9e72`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bfcdf3c01297eb06b59232529bb37e83cf5e8225551f7278d0bbddf997984733`  
		Last Modified: Tue, 21 Oct 2025 00:24:47 GMT  
		Size: 48.3 MB (48267195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef5a0b42f9100e44eb49431e4c850ab4272b6777900df8ef8efb9c14dc438e2`  
		Last Modified: Tue, 21 Oct 2025 01:22:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d7cc5c1dfeb5cfd4650962ca0db2ddc65eb9f5d661339e7e60eb8527cec70f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808b9fb4c0080cf4f3fdbe400ed3b1e8d1111f9895bf0dbe6410dc3c89d9bafc`

```dockerfile
```

-	Layers:
	-	`sha256:f32ad6600863ddadbe50e71b81ed286ce978b928fd5b4f0381a002ed2af18cb9`  
		Last Modified: Tue, 21 Oct 2025 06:24:47 GMT  
		Size: 3.1 MB (3129862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708602379f8173ebd0493d0296396e354cdbc80c267493215413c6a546994ee0`  
		Last Modified: Tue, 21 Oct 2025 06:24:48 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json
