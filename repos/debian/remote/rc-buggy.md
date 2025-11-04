## `debian:rc-buggy`

```console
$ docker pull debian@sha256:bde2ab490cbc5bb6f6c975a9dd272bb3d051cd4ffc7476729c1cf35832e77f8a
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:9cedd3b6284bf78b8999cafe0d0287a9a42699452942b2fdca926e2804df8abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48383531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccdb7cd6523852652f4c014119afac799740ce0faa0ef03e56b9883d560aebd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0109e113813179139279a81c95f6a3b143710afb074beb6c0a8d6586c49f0356`  
		Last Modified: Tue, 21 Oct 2025 01:16:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:12e1f92d6244a6bfb9b38c0f469736b68ed36d21620e920ba5e03fd99d6bcc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec94c09d7dda97bf28431da17ebaf2c520ad03ad66deb960fad6ed24ece15a7`

```dockerfile
```

-	Layers:
	-	`sha256:94ffb207e897f3d3ccb874d66f1823ad712e97527d2ecf58084bb5c65f9fe6b7`  
		Last Modified: Tue, 21 Oct 2025 09:24:54 GMT  
		Size: 3.1 MB (3128413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b467ff034be7c5df73d9d795879ce223174b5ab6fa18d4db13f3eb8bb55981e`  
		Last Modified: Tue, 21 Oct 2025 09:24:55 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:3955f305f1520548bcc76742a2b0c5a244b78f2fd88cf773578fabc0aebe155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44911780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e236118d79df4dd7b2f49224d2a7385d07d736f86752eaa24b811058967d7e7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d46bd548fc78deefe00dfcd2b559377066496f2d6beb8d1543970d5a2164151e`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 44.9 MB (44911556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad1a91f071fca0115084b714a554551feae9bc9889dca9786a45b5556bd95d`  
		Last Modified: Tue, 21 Oct 2025 01:18:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:aa6a6c99db04085fc47bd1425b5f686894b71d539d21575ec146393376c1d0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32166cb6056ec957cf9b3956029be089ddcd76b112cae503b4e02015c80b1c5f`

```dockerfile
```

-	Layers:
	-	`sha256:4f04f58a5fcd8757ef828c048807cea399b31118ce9f9afcdef6a195ede2bd91`  
		Last Modified: Tue, 21 Oct 2025 09:25:01 GMT  
		Size: 3.1 MB (3129789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08dc3b840f7af2bbb29fd9c3ac9e6733156a35662d95766e5e06a4883781473`  
		Last Modified: Tue, 21 Oct 2025 09:25:02 GMT  
		Size: 6.2 KB (6163 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6e78647d37ecc0627e41fdb46b0f9c0488511c95a88e76dc7fac2ed534af647a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f58a716525730d38a24d21e72ce94e6a6af5cb18428f0ed8873cbecf8f8c89a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5386d93ad39ae7c8259d35a113b1100cf975b2b8a8d77b1e04f298c003197a`  
		Last Modified: Tue, 21 Oct 2025 01:16:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:ab4588355e4bd2c2fa8d0b49e9bbafba337a456e99c7baee0e3a814d280f447b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f9b1be17a8a3e65b800d2be7e2c5ca81af96110b156ef9f201a40429223d0c`

```dockerfile
```

-	Layers:
	-	`sha256:433b10df1a6b18acdde625edeb02867f5764b394dd200dbd68b6290b4e70388d`  
		Last Modified: Tue, 21 Oct 2025 09:25:06 GMT  
		Size: 3.1 MB (3129266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54877d274603aa177479c8407f3d528c965d90cc02a2d03dbf379653b5cc5f80`  
		Last Modified: Tue, 21 Oct 2025 09:25:07 GMT  
		Size: 6.2 KB (6179 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:f4c63c9156cea275abf662fd508cc04651eb9f7343d4e132a4a7311b56944e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49718391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c4494925630311dce269c31c6ec3d6753f777616b2846d4cdbe3bb8e69e0de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c31308b8539e675ef4a9fe10511685897ca2f36bc92bdcdfdda075804bb357`  
		Last Modified: Tue, 21 Oct 2025 01:17:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:80f01f8069b103bec40725d090f2b2514ef21bbc52fc3afb0e1918429049904b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435aff64c36c7465524aa16b1f2e8b5e92aed510fba694505da88e2aef000fed`

```dockerfile
```

-	Layers:
	-	`sha256:bfe3f3c29910b304403408caa013d42da813088e74231c0e66171dd64fa6c2aa`  
		Last Modified: Tue, 21 Oct 2025 09:25:11 GMT  
		Size: 3.1 MB (3125617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ead60a985e91716811539b22313da17d0016def58799e778603add2831ae3d`  
		Last Modified: Tue, 21 Oct 2025 09:25:12 GMT  
		Size: 6.1 KB (6076 bytes)  
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
