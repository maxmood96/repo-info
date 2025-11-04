## `debian:testing-backports`

```console
$ docker pull debian@sha256:816a31f4455a294a7be90e00ecbcfa58ad2683202f5a433f6af4f733d39e1798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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
$ docker pull debian@sha256:6b15498cfd23d1693232457b8e19aeec19ffe8450a07b736471bc9f639a28d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49759355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b3306b161ac6e178db39d1e0200b39a6c64e86dfe297380f8cb3333f424645`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4a5c7cbd3a941ab0c02b6508acfe1e36538433539b8d0d1b5fd34bdb9f52ad60`  
		Last Modified: Tue, 21 Oct 2025 00:20:25 GMT  
		Size: 49.8 MB (49759134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031f405cdf46849ae674d66612a024c08c9b05d4a9eb8406a33fb88b0218be6`  
		Last Modified: Tue, 21 Oct 2025 01:16:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c18fc77b0c7502bffec320df11fd3a363d10641aa5da25afa2c52c5234639a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fca4e736c2df748ad289ceb86354e88acfe3415003303cec82c26cb558559d2`

```dockerfile
```

-	Layers:
	-	`sha256:64c25e7fab72078767b0961329992c4c503291500c2385fe3829601f48de9067`  
		Last Modified: Tue, 21 Oct 2025 09:25:34 GMT  
		Size: 3.2 MB (3164893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7387c5dd3e2c9aee224e0ce9b70d0465d340e4597999c63223bb0e488e82451f`  
		Last Modified: Tue, 21 Oct 2025 09:25:35 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:979fca4e8bfa4540555a060c68dd360a8caf902b0c836f6ada84946c3bba1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46030654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e064bfb5c3f90ef88baccc4a167781f87f153eaa7252b695ef2c9df7ac6bea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f8585307ec266dbd125281365a49ef992a4038bfcb783fcb1cacafcc1e6e1223`  
		Last Modified: Tue, 21 Oct 2025 00:22:21 GMT  
		Size: 46.0 MB (46030433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4b24e8b0440bcd61f216cb57b29285b7af41aae556534a5989415a573ce8a`  
		Last Modified: Tue, 21 Oct 2025 01:17:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7181051730bf302d7dfbbdc7aa18ec7d1759bd73220e98668e938f5bf19b66c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644d7390c13af41829d0329936f7c40e40033b4f8cc4024be24764571aa9316`

```dockerfile
```

-	Layers:
	-	`sha256:6387e99cc65b82411f14f3aeb81a31d1e57a9f9e231160cdf60f254d75f69e65`  
		Last Modified: Tue, 21 Oct 2025 09:25:39 GMT  
		Size: 3.2 MB (3166267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2394e7b9ee0e52e8f39e929cc043f886556b4cc0c057ad633e7856bdb61f9a25`  
		Last Modified: Tue, 21 Oct 2025 09:25:40 GMT  
		Size: 5.9 KB (5893 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3136dab6c0f147f7f609bdd99f36d04d68c48826d11b5dd78f2c19ebe1208d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49888699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f20a654cab9f9414b8ced29857a6c9fbf47ff16505c9d84a08319a5fd11d561`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6d3cb0e5bff2ab511722bdfb0d01ad86b98208ac1234c63856d04921ea955fa`  
		Last Modified: Tue, 21 Oct 2025 00:22:22 GMT  
		Size: 49.9 MB (49888480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67175d7753a5eef9ce09f120fe7ce1f9f31ac1e4412b69a3f38fd8fa2ddfa5`  
		Last Modified: Tue, 21 Oct 2025 01:17:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bbb940276affe657feb55bed503cf9f7b0672a0e45395ac337589e6c6e32ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b4c6691a8f4c691b9642718f08642ee80d4e327aa74e43847adb4def4c43b8`

```dockerfile
```

-	Layers:
	-	`sha256:685a103ce9bdba4a756cb26715d5fe85440eafc89f238941198044fd0e156881`  
		Last Modified: Tue, 21 Oct 2025 09:25:44 GMT  
		Size: 3.2 MB (3165736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6579c87a8c4d208570e0f5b559bcc78ba578c7404649beeda0eb6c482cf9b0e`  
		Last Modified: Tue, 21 Oct 2025 09:25:45 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:f7813e4444edb2f5ca8818f8aeb092d4b6b3e607f851db713711a4f5527005c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51134623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9da10cb8012b694222132f771be68aeb59bee20634a3b1d5796846aa24523e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:308cf02eabe65349fa3a70feb5124a2fe47a151e6dd9979e9d7fbb1a5945a0d7`  
		Last Modified: Tue, 21 Oct 2025 00:20:50 GMT  
		Size: 51.1 MB (51134401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21ac736c67100efcdbf3f97c5c3ac738def204c55eea048452ca8669abd611c`  
		Last Modified: Tue, 21 Oct 2025 01:17:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3a9ecabbe16328c1dde4a47678cf78385ed46e9864f83508ce13b988e164c33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52429b29bfbcdb8d3abc31a2f0ba11314445c7e29824a9b1c3cb059b41b329b3`

```dockerfile
```

-	Layers:
	-	`sha256:e58b8d654b4d26f1f55d6e8086e8499ac575534c3d862d5b838ee80d2e01bef4`  
		Last Modified: Tue, 21 Oct 2025 09:25:48 GMT  
		Size: 3.2 MB (3162098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3854edde20d30ce9bc7882e66337973548af33a65017495ceac69760467d4e`  
		Last Modified: Tue, 21 Oct 2025 09:25:49 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cfac20c7f45fdeca21f06154914712b836f5670a527580eef6448f4b0f84c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54876016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25015fbf94daa1ff7131bb53fdecac1e6ba0643dda9ea921f8709bee52fb11`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36d0226101dd4d1467e5db6271afb57e987afc3f5bae52044471b8b5521e9b0f`  
		Last Modified: Tue, 21 Oct 2025 00:25:25 GMT  
		Size: 54.9 MB (54875795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e5e84dae6e148a2e77c25200318fd38420c4547054a33caae893d6990b2074`  
		Last Modified: Tue, 21 Oct 2025 01:20:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f6872127518d4bc8b23996f83e8065bbb652053765bf84f4afdf66d60f0a3ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07650f11ac9cecbc2ef486dad3d39afecf00fe87fe3f773bdb23e9103c5b80`

```dockerfile
```

-	Layers:
	-	`sha256:5987ecc8ad58d76d91edb67ec6e93ed163ba44d8047ca922d8c419a49802bcca`  
		Last Modified: Tue, 21 Oct 2025 03:30:33 GMT  
		Size: 3.2 MB (3168400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6862d302da6a4ba70a8a4d563c1f6dcd1a6d1649890e6dc77d8a3e1679872c7e`  
		Last Modified: Tue, 21 Oct 2025 03:30:34 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2bb0c74841c0edca86abd64d431db715ebd131936bcd0654ee2cb82cf40c397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46791344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7787ac7cb78a2fbfa4c917089cc9b882ce68fb6291dcc5dc4bc280ccd0fad7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:21:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a3c633bd5a8a638b091323ca9232090c97b6cf727820f884e36ab020bdcbcd4f`  
		Last Modified: Tue, 04 Nov 2025 00:24:17 GMT  
		Size: 46.8 MB (46791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d01c79ee2370649e5004a7e14fda3372d3b2814882bf5ad70cc31e37fbb07bf`  
		Last Modified: Tue, 04 Nov 2025 01:22:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6ce6485d05b891be07c778412972709e51cc9cd3dff74dda128e8f4212e8730d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cccdd60d0557a488fff9ab1d0092eec83c0f6712ad62946314d09a8df2c68f6`

```dockerfile
```

-	Layers:
	-	`sha256:b97b630296b7b40610db9d13540319f3e760a878ac15809e520dbe4cdee23d4e`  
		Last Modified: Tue, 04 Nov 2025 07:29:55 GMT  
		Size: 3.1 MB (3121840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3baf77c90c93a2222ae4e8c8a0b67f8bbfa48c8049f365a0f301a82e4b370c54`  
		Last Modified: Tue, 04 Nov 2025 07:29:56 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:df1b3835bf3667c2860eeb7d106e3a21e6d1dc6d0d0a249c813d8242f1afb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49621006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd8052bd20c0ed0321798c5e477ad2f9fae61379aa3ddbc96a28eb81bf1068`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:51fdd12f65670bad766fd6f57cffa9e3640464411e76b2dce4dba9c4c4c01438`  
		Last Modified: Tue, 21 Oct 2025 00:26:48 GMT  
		Size: 49.6 MB (49620786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeb07c73e04ab8522cdd804a6ab398078b76379d11817b905d1ec3edf0ea6d0`  
		Last Modified: Tue, 21 Oct 2025 01:20:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a96a3f341d2aa3099f1862c3b7a24b009df29e6b8e469899574c2045e25d9ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282dbe84438bc8f27b1093f6d54e251a9f1487720fe4f541eba11c382f1fa4d`

```dockerfile
```

-	Layers:
	-	`sha256:147d98b80ffbfdb828a103c4473b71538d767c11ce38ea961f91d808a837b971`  
		Last Modified: Tue, 21 Oct 2025 06:25:09 GMT  
		Size: 3.2 MB (3166340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b06a93fb3570d044ac539fbab3cfe50be8f744e6553b11b65a6a04537c3c6f`  
		Last Modified: Tue, 21 Oct 2025 06:25:10 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
