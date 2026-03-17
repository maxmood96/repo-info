## `debian:testing-backports`

```console
$ docker pull debian@sha256:f2523ad893fd82741328ef22714ddbe68affecee61cf5a9bf8230ec09a869520
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
$ docker pull debian@sha256:c977ec5c53faf33f90f81827e70794dfb7da863b9b1a6e3ca4221ec8677b3fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48625313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89792f729338554f5e911bd68ed2d78859e806dad7bfd52115a7bd8640eb32cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:18:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bdf93a2879f2008840b5f624f2c4c1f23c3eff5c5c1ecf008ac6cbe78630f3b`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 48.6 MB (48625090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a792141ad08803e494a9011147718f2ce1dadbd18f26a728b91f2d46f04ae9ef`  
		Last Modified: Mon, 16 Mar 2026 22:18:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3d78b4042de7869a6ff97faac1ed937eb566f096aac1a6abcae46d9ae1e6359b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6c10ac302bd948e59cea33f006404af16dce383e27ece11ef6bf50a8e9186d`

```dockerfile
```

-	Layers:
	-	`sha256:9e976a67179bd32c36ff5bd5cde4c9bbf0ecebf346636b976a491c4ba9132f5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:17 GMT  
		Size: 3.1 MB (3143336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dee3ce4a402592b4cf7472efcb15c0b2a96ca6f93889202fdbc893d8271d51f`  
		Last Modified: Mon, 16 Mar 2026 22:18:17 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:647e7146246cabc233252f1d580ca5c5ab6c336330183571506e65f1ca0bdb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45555446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a94724f75e943c190815acada95641074144fdb97e622675c5924dcee7f2d97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:18:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cafbab07fde45ee03ffe592b53790696e45251b063ec05251ab946878723cce5`  
		Last Modified: Mon, 16 Mar 2026 21:53:14 GMT  
		Size: 45.6 MB (45555224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fb7785d0ca18d0323833b4d5dd387606df16da569f77e426cf958eee98ec0f`  
		Last Modified: Mon, 16 Mar 2026 22:18:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4b8c082f6af9a2f875942a69388d50310e4dbae4c8e36e118721dfcd1bd803eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f667fc0493e7d04f93808d0d00019c43145ed7f432f3b4be19805fa9eaec69c`

```dockerfile
```

-	Layers:
	-	`sha256:cbb698288a68f013782bc4b6324ab2677ea993266059e8706d72932e0cf0af93`  
		Last Modified: Mon, 16 Mar 2026 22:18:14 GMT  
		Size: 3.1 MB (3144698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3154bfdd66b6ef950a02343e69a9a8a40f826d3386b50adb6c63504b2f1d87`  
		Last Modified: Mon, 16 Mar 2026 22:18:14 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7f69c69058cbf03728dea7cc949145d8a5b7cb6b6e17608397db9486acacb090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48659278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d126c47c8ab04aad3a5e85bab635ed809fe6703ddea113090351c7c50e20fe4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:15:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:12fcadc230f71b86971148dec79ff06c30c49aa5439d1eb5f527c324c9b378da`  
		Last Modified: Mon, 16 Mar 2026 21:52:52 GMT  
		Size: 48.7 MB (48659056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa233e13a541a6949f9b669f09ef2578e5b91c4790e50e59aa1ad5b38ec1d4f5`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a98acba3414dc0da8910393ea55e252aee3a1c869813622853fd76242320e5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ec2f741cc699533fb5f5516db1857ec5c630c935dc04d4f8c2a2b5665b563e`

```dockerfile
```

-	Layers:
	-	`sha256:3575e10f61467b8dfbf66b99f0aa1ff363b6bd34386da05d75247bc2b161ee77`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 3.2 MB (3150102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8afe7265b9af192fe3767487fbe319785c037298ea9d58b37902663f48a5c38`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:8902ec4268d8083ae54b01af2da95f46eb0b90f2ce4576aaa266dcae8d52dda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49920091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2db8ba6effa59daa20890b7c584f5ac7bf34bd03182756c03cf0b7be2f37cf9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:16:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2f9ccf5293d55acbd853621f4e56d2a15a17b5277bba7afab5b460dd6c5f522`  
		Last Modified: Mon, 16 Mar 2026 21:53:26 GMT  
		Size: 49.9 MB (49919870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704a95fa03ad8b6b47bfdc6aad908139244f011358d72f51142c723fb0585fb0`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8118e9d67502c39f7ff07f8c79525879aa7dd724285b7147f4ad4dbd7c82f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb1b9012784ccb2bf3ba8f568a66c3dbe61b4a36009266b04f83f1fd59c1663`

```dockerfile
```

-	Layers:
	-	`sha256:dd19c52939df1f4e33622496bd3154b2f1d50e6a630607252f557882406f06ef`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 3.1 MB (3140539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8dd114c79dad13ad9112a8a7be05190594d336ff18d3c954f887fcafa27fbc`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea377890dcfcb16f0dbfd1aaa54a9034225872a7c85ed64c981e23b13cf8d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53642008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5afa48122ea14517353bce77f3ab8b8c7d1ec88d544a43bb47200cabf67e42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:54:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a9c7d7625b810d130976f4d65172bc2e59635199240180b43a17644df8a7c067`  
		Last Modified: Tue, 24 Feb 2026 18:44:39 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed84671a97ceb4d69bade2803d1ef8bc3fd7d496ad22ae9b6b40ae4f9d2ccb73`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9902febbab3cd27e9e44dd510870d150aaf125e79680f08cdff08c37b1321d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75018cfd2885acb7413496918a60c6f330df44b979e0da98101e646c443708`

```dockerfile
```

-	Layers:
	-	`sha256:6106d6752cdacf41394aa840a6831cbb7804c3eb4cf6536e1a2b2ba6256c31e9`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 3.2 MB (3151079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb56fbfe1370a67ba5926aa938840b3cfc297ce3f67472dd7d6f7254455e0b9`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5f6d5604e0ef22348029f3057e262655affd3116c1305e9b3ebfe2eb353d7117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ce3412e2adbfe439edd986d6bc3d59fb910594afc92e08775830d85e329123`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:22:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1ae2ae21b0f1521497ab28d47ad15e8b14e56f2bbe5b3ef82df0b03e8bdf5be9`  
		Last Modified: Mon, 16 Mar 2026 22:05:45 GMT  
		Size: 46.7 MB (46721466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750f04028c153fa038de6a07e4a5ac2e87e03bdfc8ae0185bdfb654320257dfc`  
		Last Modified: Mon, 16 Mar 2026 22:23:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:35b8a86bc199140fa0ecdc163df8f72d9e865b1731394e90e80cc9eadf60c4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51e4791a9ec8570edae0f9053c02041acc98c60e37463b57333b8a0e6a39c36`

```dockerfile
```

-	Layers:
	-	`sha256:d403745033d06ae6878833208536c6c46dc118e9f744b697bff834e0fd01b9c1`  
		Last Modified: Mon, 16 Mar 2026 22:23:35 GMT  
		Size: 3.1 MB (3134838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0dfeb8e5d683340ce8d62e01ceda6cd48066b04ee05afe364828f706343563b`  
		Last Modified: Mon, 16 Mar 2026 22:23:34 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:0f41dd52196da0cf5d8a6e4ed82f0c5fc009e2e7e3b4bfd7f64ad0c49daf28eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48334843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e60cbd02867598fc69937a03d56459c0bd8d154f341bdeabca1c8a26afce70`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1773619200'
# Mon, 16 Mar 2026 22:16:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:86061245e560c9a63c0fbedc08ed9a258a537380494ebcd35a7a03910bcfbd2d`  
		Last Modified: Mon, 16 Mar 2026 21:52:35 GMT  
		Size: 48.3 MB (48334621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2776628cfad0a8f55132c4435233f17c89a73faa870e30f4f86ab522ce0d3c8`  
		Last Modified: Mon, 16 Mar 2026 22:16:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ddff5724e4c5de1cc7dca5c9a58d91011ecf6708a0f4ba60c1c1f4491cc01e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7799011c83f579d381a18bd2fb35eb1a80be74bce9d96062bc61a4fb113e51bc`

```dockerfile
```

-	Layers:
	-	`sha256:6f9f61f0e32a7f5ecb049e66618f8796368422589ded260d56edcd38c238634b`  
		Last Modified: Mon, 16 Mar 2026 22:16:12 GMT  
		Size: 3.1 MB (3144787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6f08f3622eec0f149e3bc5a7489e051eeeb99ad684f5526354924629e5667d`  
		Last Modified: Mon, 16 Mar 2026 22:16:12 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json
