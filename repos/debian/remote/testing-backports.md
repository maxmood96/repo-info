## `debian:testing-backports`

```console
$ docker pull debian@sha256:69d0bb0ef6f12faa116c922c54848ad51a3f55a07392a6045169241867ec5f13
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
$ docker pull debian@sha256:4d67233b377c97dbc503f1e0b4762c6dad94d5589129bb753bb1762a575a9fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27015aa9e3f32168bb96173becc046fa764c0a2dfd2252df202a9864c2ffb084`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 03:57:49 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a9f04603368790b1114219c73b70b85fe6a8ccd82e5a3648b0b0ccaeb92a19a5`  
		Last Modified: Tue, 18 Nov 2025 02:33:33 GMT  
		Size: 48.5 MB (48500435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296cd40c80b1be2b2e813b205fee7cb7afb1aa951dd6ffbbb8b35b20825787b9`  
		Last Modified: Tue, 18 Nov 2025 03:58:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:34bffb298f39f2fee3c8428479f00e7bffce24d737507d05eaff4c4b831d0cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48461353737a2acb3d4c3bc31c304cbba1034a94ea68d372c7bd81086707d9e`

```dockerfile
```

-	Layers:
	-	`sha256:5a06e3c281fdd6d41dd4f5ae4b0aac9ad9b9a9e0f4d3ae6eedd5621942ecb79c`  
		Last Modified: Tue, 18 Nov 2025 04:32:13 GMT  
		Size: 3.1 MB (3129537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3634d95663ca6c1b69c55c6d5a78d998563a575e9ecf6def82c79e3c7850b45d`  
		Last Modified: Tue, 18 Nov 2025 04:32:14 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:db5fdf8ba67d08c4cbc8651997beefa028bfdaaee2492fee79d01fb896dd3c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b025a07e9f4a0183ebddc22a4c78015808bbccd2d7581ce2501ee588533ef21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:20:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:33a39ef1a30f6b8cb59d8128b717055eafd7e59a223a3ad134f0261080c409c5`  
		Last Modified: Tue, 18 Nov 2025 01:14:15 GMT  
		Size: 45.0 MB (45003763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01db803efa0cd8bc423930beed6153c2c3e5155680709a4b7a9863a0ba9cbf`  
		Last Modified: Tue, 18 Nov 2025 02:20:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d4b441958c9255d88aeb6e0f05012bea8780e4ecd324a4a10abf9162fdbebf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfce1e9281c30d14243301733a552aff737639e313e7f18ac912d5d2f6e931ca`

```dockerfile
```

-	Layers:
	-	`sha256:080713917ec4762a34a1d034fe5b7cab67ff8afba1abb2623d9ee8c1d8348810`  
		Last Modified: Tue, 18 Nov 2025 04:32:18 GMT  
		Size: 3.1 MB (3130905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5882b8fafc2972e01e38641910b41598bb6b2a284514cba343a9bfd2c1d75e`  
		Last Modified: Tue, 18 Nov 2025 04:32:19 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b6b2d7dad3c77f4263e2c2e298f9fbece7f0cb270470d86ae6566613df5f815c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e6aa604301fe2aaa206bab1a008057bc635e4c9a61fef7b3596671eae8f5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:16:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f49467d8cd4539a9c64ea7b5c2157fdb7eda1d57099abd6444b4b6f73295cf55`  
		Last Modified: Tue, 18 Nov 2025 01:14:22 GMT  
		Size: 48.6 MB (48591185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163b10a474e460b1baddc6abc01d45d038bb5c3398467528ef8dcf1c25e15e35`  
		Last Modified: Tue, 18 Nov 2025 02:16:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1fac0ddbcd6a62fab008272bc55043da267ebfa6bb6797912beb3a93740ab647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98a2b15c6ec3c15a010883d6091a5d1915709895ff643a0bb352e2c765489a0`

```dockerfile
```

-	Layers:
	-	`sha256:5bd4a1d62879cf8f88ea734066bdf3f6c601d178584dc64f862aab0fd71e2941`  
		Last Modified: Tue, 18 Nov 2025 04:32:23 GMT  
		Size: 3.1 MB (3130378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12314b085f95802c3a239574bdd2cf0c138dd83dc25d97e8dfff9c3321f95a7`  
		Last Modified: Tue, 18 Nov 2025 04:32:24 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:09ba48a6aab45a51318eab71dd701e7847ba7d278b40aa4dcce2815ad758fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9745d5765fc7ae82243c0d3ddfe8e030217bd004adfd11a90a318e977ba594`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 02:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1404c940473e44843d0b36ed588f649ad241384074679bfc06befc51812e1934`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 49.8 MB (49832239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b87437df145cbf84bbcb510fa2d35ae25944af5cac0e24c5789d0284b6cbf6e`  
		Last Modified: Tue, 18 Nov 2025 02:15:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a30791fcf045296efccc5d2981f4e6e3d540c7c7e9817ad5981ff3b3149ad473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a44c1220ff4cdd0a62bf250e4ea3c486c792622e095518e6b8ab213d835c7bb`

```dockerfile
```

-	Layers:
	-	`sha256:d5f93f707763fff4256fccd50d9efdf230b30cc9a0fd30c073cf669b0201a980`  
		Last Modified: Tue, 18 Nov 2025 04:32:27 GMT  
		Size: 3.1 MB (3126746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:423fdea617bfb3b637490330ab79f0bfb8ba8c465fffc4b0954e691e44a43c96`  
		Last Modified: Tue, 18 Nov 2025 04:32:28 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8258c68adfdb812c2e5399f7178f55a60b099c5345cbe641a29bde364a135fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53315460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc07b349a4ad2f3be6aa925e24af0f3ac1b3f564cfe1d1757d8d72e8dc87729f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 01:19:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:174727ec3d50f4bd692245f2ee33064dc9c22375cca6dc7eda65e345ac6d4927`  
		Last Modified: Tue, 04 Nov 2025 00:19:09 GMT  
		Size: 53.3 MB (53315238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce8170373de8db877e8afdd5cd08294602a82b36d099078436b037256d5bd8`  
		Last Modified: Tue, 04 Nov 2025 01:19:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:632c95d93fe68ed0be457a9ae7cc164a09675f859d44b3b7fc201d1bfc73bdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580026f109bfe22a6e641eb3d6a5ce92769f95764449626c0ea1e77cbd4e0337`

```dockerfile
```

-	Layers:
	-	`sha256:fbb390ab2cbec1c8f23621243e7db2c297c772d4a03cecf67e45a7713bdd050a`  
		Last Modified: Tue, 04 Nov 2025 10:29:46 GMT  
		Size: 3.1 MB (3133030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef8b230ccafab662ebfa649b878daa9b3885837d97821eea97dee6255d0b7ed`  
		Last Modified: Tue, 04 Nov 2025 10:29:47 GMT  
		Size: 5.8 KB (5820 bytes)  
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
$ docker pull debian@sha256:ca3fee9aa1317deb96e1901e3509a79a15f53f6363a6831fe45aee2cdf34d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48343283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59b28ab144eb97aaeaa5c39fbcebf6f61695bca3d775bb5ff2280f3f1505f0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1762202650'
# Tue, 04 Nov 2025 06:42:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e99c0da2e97fc60ed941b2b64ad1209d58000b6a2e554be98962ab3f543525bf`  
		Last Modified: Tue, 04 Nov 2025 00:18:40 GMT  
		Size: 48.3 MB (48343060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38caf475179f5703f67d64f0b5daea5f7de3b953d1e03f96675bd084091b7cc9`  
		Last Modified: Tue, 04 Nov 2025 06:42:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5cf698e0c10efcf3be017496cf06874b8efab33cbc87870dd4394750eb589c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40853b12090f86f2b3d3817822a9b4dd642761aa8da29ee1e1e376b5070a6c55`

```dockerfile
```

-	Layers:
	-	`sha256:2eba15cd86435051041397e0a41b8e5ddab2792bcd555a09f3e4b5fd800c5214`  
		Last Modified: Tue, 04 Nov 2025 10:29:53 GMT  
		Size: 3.1 MB (3130990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e44e37c645bcbb92da641a264907ef5acd91a71f94604265080196911c608f`  
		Last Modified: Tue, 04 Nov 2025 10:29:54 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
