## `debian:trixie-backports`

```console
$ docker pull debian@sha256:7363be8e61a9d938ae4ddcbf784016bf81ea93919c38d0d51d6472f0446d3a94
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:dce00543bf66059aed84de18cc530fa3fcf6834ab1abc5a7c24068f3a9595700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52113781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81081aefa7d026495321f2a00117199e15055b71c8986e1811d67061e14107cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b26bff9b493995697b6d64d062df29ea646e78ad90399c244aafacdcf254d6`  
		Last Modified: Tue, 03 Dec 2024 02:13:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:065aa3f5e4fdc7506a6f393adb130b732600696bcc4186a82044e1d28f51febb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700855c1699e9ee470822d4d209cbf7c7e271194f24e988317cd7ce667a238c4`

```dockerfile
```

-	Layers:
	-	`sha256:8cd7670238a7ef8900c30197eef6d074a91b8504932ba2ed00525f03b274218a`  
		Last Modified: Tue, 03 Dec 2024 02:13:44 GMT  
		Size: 3.2 MB (3246355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156a0cb7b5dc19164478e07d4fd4bd8e19e5f7f3f3130e134d9a7c36a1c8ba2d`  
		Last Modified: Tue, 03 Dec 2024 02:13:44 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:18c7bf34fe20a8fba84b30dd861f6f9ece3c47a73778a7cee3a3322651de9f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1d486c08b4b8c94082a0ae0ad676609a66a53965726444958046bb59ebce34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adc28be87574c32c64609eaa03b3333a11374bed510a203bb2d0aa1e1f033bd`  
		Last Modified: Tue, 03 Dec 2024 02:19:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dcab0ac1d74a5532ca03afeec69ed0ce4b74b58b76ffba46c7a65090e6e0c43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e687b7ebec48ccc210704de8cbc60748bd0f00d8b78626882f987694eae5c982`

```dockerfile
```

-	Layers:
	-	`sha256:b9fddad302602d46331a4051fa7009fe418360ce79a9717183b0b01ae4b75376`  
		Last Modified: Tue, 03 Dec 2024 02:19:41 GMT  
		Size: 3.2 MB (3249177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26aff92083332406fc16748adcf0fcb6cdbdf6148ed88d83eaa0d32b494a4d14`  
		Last Modified: Tue, 03 Dec 2024 02:19:41 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fc8ef4e01e68dbaba4278a0739f704a2cae07335ad5241b18ac347d138aea7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46679869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c7362b33c2ad47ba3ee615df1755e3c59d64ba4503705f7592bf890d43620`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d281798b048836343243fe6726f9ff1be168cf366b9db5b2e8a89cdc990d7b0d`  
		Last Modified: Tue, 03 Dec 2024 02:20:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b0d035d21f4243a4eddbe74a6b3bc272ca5a06cf10ac77d43fb462fee553dc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edfa9fa33e92efafa89525db5058fc177c0ae43e9a368f9157864204dd6fcb8`

```dockerfile
```

-	Layers:
	-	`sha256:961a63c7292a8e1f4c96bbce37a4ee2dd02a1eff6040503d87ad79631aff0a3f`  
		Last Modified: Tue, 03 Dec 2024 02:20:17 GMT  
		Size: 3.2 MB (3247913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41a01f76d916e07a70161b0a36e8f6d25e579f6d7895854bc2024e8cb49a65c`  
		Last Modified: Tue, 03 Dec 2024 02:20:17 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ad03623171d8884ab202ad0dc741c711f19adadcff21c9c04fbcbc77c091e81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52341073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5aa36f00bcf57adff9c69717a0b83e98048f8287c6f6bbe04a94a1316b7a84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3f1ed3134fb41bf3c586cdaca8e87e3d84b5be4719ae94104e088351f58ec6`  
		Last Modified: Tue, 03 Dec 2024 02:19:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cd2596fdaa0b74668a05ccb5bbc5f0b8d46e78a11e8e566024d48495a3879222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3257102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f5ccdae107cfe77fd298f47a69e86f56137b111dc4d6f579142ae639697a58`

```dockerfile
```

-	Layers:
	-	`sha256:06ef767f87984d100db7a3ae5bed37b2bbf78ca38a8433da1299618a44f1c73f`  
		Last Modified: Tue, 03 Dec 2024 02:19:36 GMT  
		Size: 3.3 MB (3251207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75cc0048ae819c17287fd4ee6f23368d993b42730f4da3e2121dee7b4cb712b7`  
		Last Modified: Tue, 03 Dec 2024 02:19:36 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:3b27cc6d8f2e7d1a359f8a632e62042a99307fafa8365369378ee0566bba1d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52956506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193ba511e22ae47948a136262a643ebfb027392a6aac3ccc484de88d3683335`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf339cf2c2bf45b1d19cb5320cc64d1dedc6fe55bae4684af9ab2fe4a8e03ec`  
		Last Modified: Tue, 03 Dec 2024 02:14:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5a06035fd0fa0b920dcdf597df9413222f1cbc1e02700c2558395ea428d6253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caf3e17a3dda551a0d52417b0bfbe5409ec8313077288c5b63c3130baa9146f`

```dockerfile
```

-	Layers:
	-	`sha256:5a3503e0ddb934ea69b4b64bd496ed58c0531db137e0f8075de3879660a214cf`  
		Last Modified: Tue, 03 Dec 2024 02:14:10 GMT  
		Size: 3.2 MB (3242833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ded1d36cf8bfbec60a29599be0175f45a0ccb8c48129b6a6e6fdb364aece3c`  
		Last Modified: Tue, 03 Dec 2024 02:14:09 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7247b5dcfdd2b2e34bb10a1507475bb8a34d512ceb35400448d194cc3ce57c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51440149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389799a0d9d9ad04527d0db17260f0b971cb6f102cced2ef4e45bb82aabccd7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568f17a9b515033aa21fc842bd3333f9b04972d060b793be35c5317c3cd55b89`  
		Last Modified: Tue, 03 Dec 2024 02:20:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c775edbc66fa7ee455387f960115c1483c1671cc0267faf975620eefb5466b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa76c2be43363d0dc44eba1dc85c7ac0a7182ecdd2e6d86c7c6a368b60c77979`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee282cb4223202f37330f8c118f273da565de57c256908624a95426da0d7d4`  
		Last Modified: Tue, 03 Dec 2024 02:20:31 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c17ad4ab41cc0f2dcb0aa51acd54effac2c6c4e38a8d9d273866c62cf3d3d65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55955896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfaea97941ff1cb64372ae8a5b2677c41251eafa5024a373ae3544f5e076a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0481a76498823eb15c8fdb92509f76e393b5fa0a324d4fe06c0255e06f78073d`  
		Last Modified: Tue, 03 Dec 2024 02:17:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b889d37ccae3392d6bee5bf2ac3f7391cfc918c376509b67ad763f65f03cde53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067d97b4b404a300dd53681701100b1986e94e8dadd860c5d2c3f269c5b0f6a8`

```dockerfile
```

-	Layers:
	-	`sha256:fcf85b36223a6f51d0377c2faf466fbf8f653ec141575b992bc9256f0f1028bc`  
		Last Modified: Tue, 03 Dec 2024 02:17:13 GMT  
		Size: 3.3 MB (3250054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ec3972089a5ce7753c4bd43c4259c1db8a2b550c896ecc11bc76eadbc10055`  
		Last Modified: Tue, 03 Dec 2024 02:17:12 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:93f58a1f6163004203266ff13c5d151c8d61d08680149f04e0d34ea46bf653cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50615286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c673c2d0b22d6a0918339b8e295846966062ae70c85d5bbd234e08490d7c1fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:758bf82feb19a3477451e92c0cc7de2b281e4c03b2e4688fc172a592db81eb9b`  
		Last Modified: Tue, 03 Dec 2024 01:35:35 GMT  
		Size: 50.6 MB (50615063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1637627c1a825535d7804cfae4a7ef2429f489147470c6a4d294f52a04149f64`  
		Last Modified: Tue, 03 Dec 2024 02:44:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:961ab5ca246ad9adb096b9ab61b35f6cc980781fd359928ebfee40480b571471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54980839fc60cf91bf20d8dc86182b8053108a6b92280f2081230433071d91b`

```dockerfile
```

-	Layers:
	-	`sha256:f3361f8713a6b25b67652a6cad130514dbcc7c14d6093b7927e99c95693a9a39`  
		Last Modified: Tue, 03 Dec 2024 02:44:39 GMT  
		Size: 3.2 MB (3239777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0d8e6c67c482f2804f59eb16d66bf295cb6b6e32ae86949e07fb43fe9404c9`  
		Last Modified: Tue, 03 Dec 2024 02:44:38 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:f24d467c1b1b38d9cf08e47462a4d5264f8f855f7bf5f37e6a0a429df063566e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52069629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9073af31f6135a7bfa20c9fe69a39513254c725fe01fa9a59fb320e14b9c5553`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801842f7e274681a3f8f4186d78a81c5c9a25f8657846a6e4262a8fa17e36fd`  
		Last Modified: Tue, 03 Dec 2024 02:15:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:44cb6051848ca1479b4b30056945926b4062b1edfdfaa0eb2727245f11b8595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed04af99c164ba7845fee770ad1f108907275b2a059d0e5d94cb450363c68b75`

```dockerfile
```

-	Layers:
	-	`sha256:04defc766597fece5335f423bfb115d30b4dc8f9294de8c79289b4791564cc39`  
		Last Modified: Tue, 03 Dec 2024 02:15:49 GMT  
		Size: 3.2 MB (3247951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830dee1bb6659e150b2769f99be508087f7618781b1f49818d1d7e1914bec884`  
		Last Modified: Tue, 03 Dec 2024 02:15:49 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json
