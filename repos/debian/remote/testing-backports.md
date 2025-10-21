## `debian:testing-backports`

```console
$ docker pull debian@sha256:9897ee53577143a558112b1b77e66b62c50cc9d91662bc29f780e62eb8158c87
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
$ docker pull debian@sha256:c94a3c5afc419d95b9d1ef59eb988f84a6eb9aff7be85f5e0acd94e0636a5cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49737039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0406cad4ded4d7a6a8a1595d3fc0e558a416ae0992ddc4eaf7b563c46c8b5443`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e53bf7ab07ea4ef0bdd293b1b3d03f786cf07ef52cf9fa96c661bdb1e7e3d20a`  
		Last Modified: Mon, 29 Sep 2025 23:36:06 GMT  
		Size: 49.7 MB (49736817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265f039e912e15dd81fca61ad79edd7d56dbe230493bbca2421904544a323582`  
		Last Modified: Mon, 29 Sep 2025 23:47:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b938feaa474f9f30bd2581056424eb9684bff957f84c5d424296fe2d4b9b0d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b3ab8305b848cfbb624710fdebb6ab7d4d7c8667095946ae1c26964ad39ce`

```dockerfile
```

-	Layers:
	-	`sha256:a90ffb1cc0f85fe9c2a439e0d555f71109a2be555164f945e5f8983e0e2ce95d`  
		Last Modified: Tue, 30 Sep 2025 00:31:25 GMT  
		Size: 3.2 MB (3164646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39aedcc3bbda1ea198abb54ddf537b5d810c1982e2c0c162d7f2f0916c3590ca`  
		Last Modified: Tue, 30 Sep 2025 00:31:25 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c45b46888b545c120ca511747c51d8e9acbd613d8dfebf3f93576e7ad14304f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84140c9615b1ea2fe9cd4aed42c8932096de0171aecf4bf2ac5fd7496a8d6a05`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e0c42b30794d7809e756b71306a8a347b4104aaff80f2934d3aba31ef14da533`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 46.0 MB (46020846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c340acf86cb58beaaaa762ba2cbd4d5000a4c4b2b785cd2200bc722233dd167b`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2aedec6f1614464b8f9b35635dd2fdb0801d8c629c077df1a4889e7ced0cd7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817bc999ddb2943b41019c0a304db7969e4035674470c7d93bc8eae33ecae053`

```dockerfile
```

-	Layers:
	-	`sha256:67365e5f222bee02e52637fdfba5724f89bdad41dfc8d66f662c21aa10728ab5`  
		Last Modified: Tue, 30 Sep 2025 00:31:30 GMT  
		Size: 3.2 MB (3166020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e6d7158d47d70e5a05c948ca8c3366371aad45fe1638de274366a3afa5e7a4`  
		Last Modified: Tue, 30 Sep 2025 00:31:31 GMT  
		Size: 5.9 KB (5893 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fdbf760c3f4935382d6c8e266e7474dcba6d1d8fd0c3c4335ab25a3df002b3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49880098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2cb47d240dd8bda0f882fd00bcb98098200bb0a3355e7d508dcdedb27b6ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eaa39e59530b026aca4c6a2bd8547ebc0f3668ab204470b61baf267315ca1cf9`  
		Last Modified: Mon, 29 Sep 2025 23:35:15 GMT  
		Size: 49.9 MB (49879876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99bb4f73d6fbcb317c728eaf73faa8101823b98c01852ba3b21dc3cd285c10e`  
		Last Modified: Mon, 29 Sep 2025 23:48:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d3262c6baefcded1d9d4a569c986bab4319396a01b486ea398f5320a98f95521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c763c07ffff08bb8926c4679b22a8158b938d22b4e810ccaea8934a03d7ae78`

```dockerfile
```

-	Layers:
	-	`sha256:ae63969eef83da765c8e8d3c852d8c1ef3777472f433fee35d423a6099476f9a`  
		Last Modified: Tue, 30 Sep 2025 00:31:36 GMT  
		Size: 3.2 MB (3166127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6568dddf56c31880fc502a51beaaeba927eb19ff40c373bf283c49398826ae4`  
		Last Modified: Tue, 30 Sep 2025 00:31:37 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:500a91968cb66cc888b41b324c4f2a659bd7502e63f7bbc8110f07c8cf109a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51119640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba379353c8d471e217c27d464d84d65a4f16989f41abe802f8f61b0924b036`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4f313a379a9bffd32c298c8af86f7e155ff0aea7519eee23a8d28bf9b6fcbfb`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc84173b4a9033dc25e64c0589ccca398091d4ad6ae807e2cd72cc38e5745b9`  
		Last Modified: Mon, 29 Sep 2025 23:55:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:69ae4d4ed32f9c1b516969787c70bbb80d097e1a30d93abc664a6b6347cf9da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e85f809546dea620ac89ffae72ac34186b5f9540196431148da41aab3c192c`

```dockerfile
```

-	Layers:
	-	`sha256:c2dec28c6b0475ee3cbc06d24e781944b56c68fe352f8dc3b2fa929e60acd97a`  
		Last Modified: Tue, 30 Sep 2025 00:31:41 GMT  
		Size: 3.2 MB (3161851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464fd10f0e7f24c8148f1cd12d3e4175f26227e9b278577f58fcac3d9e026385`  
		Last Modified: Tue, 30 Sep 2025 00:31:42 GMT  
		Size: 5.8 KB (5819 bytes)  
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
$ docker pull debian@sha256:aa1dd6d2622f1fc559402434810c642a14e0458ca77dc1c6c0c590a41e64a44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48012028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1059039177be136f45a3234bc49a185db1d81becacadf1eb5c4d14b1bd6472fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d9f71093f8427b1c818151489999a95518395c2f31c8fb6ba77b08538ccc9b78`  
		Last Modified: Tue, 21 Oct 2025 00:32:21 GMT  
		Size: 48.0 MB (48011807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2680bb0dc09f40ca05444294898489d7cd83d5b790aa27d928c6714c2897bcec`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:79077db934db52c423fe9e2e14456751068a7207fc6be1523558509efe989e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba024e1c93fe29f1d56bbfb3b2ef4d168e821dee9c9be3184fd6632b28e2864`

```dockerfile
```

-	Layers:
	-	`sha256:a9b8c4ce63d0eda625790dc005fda97979d9332cef771799745ea783a504f02a`  
		Last Modified: Tue, 21 Oct 2025 03:30:38 GMT  
		Size: 3.2 MB (3157202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4feed6936b1b8a7aa94a6ae20aab7dbcfc64efac14a71441efe20bd0a44da152`  
		Last Modified: Tue, 21 Oct 2025 03:30:39 GMT  
		Size: 5.9 KB (5863 bytes)  
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
