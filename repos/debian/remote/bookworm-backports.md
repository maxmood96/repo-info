## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:516e988f1ec8695aee181660da8eb81bd17a463774c9d050d8647cc9b8564e52
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:ddcf23f76a17d71235100e3484867e54f3ed086c96f7f8ae427d94176abbd4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7683bafd7ce33ec565ba8c5a4379f9bd16583ed4a12519c857f0b149931599`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f8e6fb888cd2fb29745dfec0d392250c721d3d77d95ce4bbe6eac28ca10bf`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a7a33f2008973d1b02d667716f6b0c6d13bff88b734e190a8f6ae24e4863f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6eb1be26aad29ebb44fbe938facea1c05d6d22550db27e9f631bee9f18bc095`

```dockerfile
```

-	Layers:
	-	`sha256:2a16fbb146389af7e2c762bce6768edc8b791a1c21e3611f022e1a0177fc1be2`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb3bab0dbb5a17e6163a4f64c425b29fbb2ea45672ab58fb2d006fc967a3a01`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f9835386eca4a347056c4aac29fe3d7de4d09d798ee76ccd4d4ab1f2b5533c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107fa661a1edc70cd770ce9264377b1ee751119cdd443045e34d5f7d151b4b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:14:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a889e82787049133d77ffad9b735ec4a592f071dd0e1873ff586ba91994e03fb`  
		Last Modified: Mon, 16 Mar 2026 21:51:55 GMT  
		Size: 46.0 MB (46021486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84a00b985a2d00e61671c063ad74902e787c9db5f886a5e98d668d04e157824`  
		Last Modified: Mon, 16 Mar 2026 22:14:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9e50993370e330ebaeaf102ef9b7df68dfed0ae96ef11a5e86f62a36aee43caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac68fd1401382bb306a75bf672b582ad32c3d6cac85bd6821f4fe751f1cbd8`

```dockerfile
```

-	Layers:
	-	`sha256:d94b97efcf06cde2d689d9abdb29fff23ec1a324f2c28b846a0da3d6ad307785`  
		Last Modified: Mon, 16 Mar 2026 22:14:58 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062cf4c0c89edfcf92f65d5b54c9697a778b2beeea8fe6c51d1fb8cd7bc07527`  
		Last Modified: Mon, 16 Mar 2026 22:14:57 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a34f6e225232a088d1aec42d989f0fc78557bddb43d57fab021d26cb52660f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bc7dbbb875d3ed1cd84d2ebba4facb6e008c1a5f51444ef9e1851fcba8e65b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:17:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623d9cf9f83cc840a450d40f04f5cd0d623846976c6237d88ca9b681e0535ee`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:def80fa75db4e717134d7b8fe6b68267d83405feb7838806116d01e69821a7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463e001acc151309b00525861b232cde0a5b2ee83c810a1eece183b56497f9f`

```dockerfile
```

-	Layers:
	-	`sha256:4619bf6292031a4a3e1a03619d62e1ddd33120c9d8327231cee9155781b43245`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de54d2689a2e3309afd2f760dbb2c2be3e664e5debfa75e490a440374f188687`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:aeaae79b547987978726ac161e90967531dee6da3cb849b907c5dab6f93f976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1cc22e362fa440cf0394a46fdf9d6e888bbcac1d331c9d2ff1e9f19b8a71a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f8e6fb888cd2fb29745dfec0d392250c721d3d77d95ce4bbe6eac28ca10bf`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3349cf87d80609950a6daeacfaa5e8cd1c122cdf13a36cc4d32dabe21a2635f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef19699ea507d2eb607da5eb9765ba9fe769b9de79bf1b9cba913cf986cabdb2`

```dockerfile
```

-	Layers:
	-	`sha256:f532638a6eaf733de7ef783f09b315cd72934b03f6ce94e84e3563d7384af66a`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd24251d14fe7226ce646303a8859effffd7ad90a63f94688730e5a2c0c39a4f`  
		Last Modified: Mon, 16 Mar 2026 22:15:09 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:a1918c7b0a70715c549b4c65a6f18c4693a9501af49b9d970f69a522797bf59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fb197434b0d7ffb0f307bc7840cb6d698047ae3500ff198a24bdaa6ce1f2ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bad37246a99437fca124f7a902428edcb71a4579f76b68f5b20b7d0b2a414d1`  
		Last Modified: Mon, 16 Mar 2026 22:15:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e83f98562dc8cd0ba1010da9deb78ff37818ab7ca5ad498f973f3209f76b1e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e551af41610a9efc5112b1efab90cd002f67f150b37a1765ded190ac4f5b33e6`

```dockerfile
```

-	Layers:
	-	`sha256:ae82a770f5128dba3d41b0c0fc5f975f48e66ddc4ef246b01d2a97f4f3f75ee9`  
		Last Modified: Mon, 16 Mar 2026 22:15:45 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241200b22a5b4e27eb96ef4dd005453cc60d1d267420b01ac01504e1dbf1926b`  
		Last Modified: Mon, 16 Mar 2026 22:15:45 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8c1d223d81a66f6afab237e4307695a96e79c4cd5684a30632c47257094fd381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b9a4bde1dcfb5c9ead53863c72d2cf9f1e1326b71de57674b12291df1d3fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:17:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55bd01c42402ce77937fae9abfba9b351fd4b3fab7f1f58eccf5b2fcf0ac8978`  
		Last Modified: Mon, 16 Mar 2026 21:51:11 GMT  
		Size: 48.8 MB (48782288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbda0f48ee2dee6657212f8591ade10a4f1cd760ecd2efc95e20114f01c6dc`  
		Last Modified: Mon, 16 Mar 2026 22:18:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:845ad86563bb7590da68b70b4bb769a8e9ef10bd1b93c80747dae301ad4ab12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8772ce11a2bc33053c609d1512b4491105c8801cbcd1b62ea389b0fbb09987cc`

```dockerfile
```

-	Layers:
	-	`sha256:6d89aa3ab38b4ef3668f7db1324751fdd336454459d9f3969e109e15a2d65813`  
		Last Modified: Mon, 16 Mar 2026 22:18:13 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6f69989b578f04695b0660b84cbe6302749ad4d0d6a01258e4ad2d1be9198e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e403e25170b6d2c0900d1fb71cf5a314506dbfd153fdfb92869b76b1d161661`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:33:35 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad733660bc585c7cbc866b401841f73450a81b5cceb98f7cf3450703f85a0f3`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3b061e36152b1d55493b345a3289f4e522bdd90374e5bbeed6e309e302fb77f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d682183b749a34f7219001298d84dc8eb9bda4f9f70900bf81dc618c6aa43199`

```dockerfile
```

-	Layers:
	-	`sha256:624cb20e45b04a1e426cad13f89ceb907e54df116cadab0bf80779203746f6cc`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468b243ec52a01abd5711b497afcf7a039bdbe1db5b1460b30f2303cf4e30c21`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:003b8fdf4899488a6d3574c617e8b335049e12ab4a6d9780a0c072a22a902bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70f2e2c0c504937309b7255adf85640c784cae9384fa008933ed68b73ddc4b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc51b2343d4c218d164cb2e908eb5bd841e8547a0989351175c8f2e0a0f38da9`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1048a583570aa2763b2e05164884d68ec5f6e295c1ff8cafccea9d0e7bb80c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69935c0d8c835d915c04ebc20506c6be383ddbeb0c2c3697f54b6e79a9c85dd6`

```dockerfile
```

-	Layers:
	-	`sha256:360e2d26d69ac3ae08ae4ec512a4bd914a45f2eb329b9a77e48966e3719b4a2d`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb55353f039931535fd65020284cafcdc3626df135a1d3cf50288046d44dfc1`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
