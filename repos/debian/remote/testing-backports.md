## `debian:testing-backports`

```console
$ docker pull debian@sha256:202aefc38f811de0d6e599510a5cdcd2ba4916e8b4227e10016f8f747b043af1
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
$ docker pull debian@sha256:79c12355e35116e28933b92ebdb0a4438280d5f27a739bfc7c068d5898164635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48830280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628f7fe70a452ea01da287ee51d49af2df78afe95d0aecee5a4c14d0cf20a3ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e82aece8925851cd125cda205a5f722be8e2b918d6f6178dae37c8a5cddc74ef`  
		Last Modified: Mon, 29 Dec 2025 22:30:46 GMT  
		Size: 48.8 MB (48830059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f8c89f2578819b88753835a915a31fa47e5da155e994eaef3770bcc752a97`  
		Last Modified: Mon, 29 Dec 2025 23:15:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60ec240967cea525f3c679f265dcc64642a1ad46339d80ed5dd253819053b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095a47f4633844b47e4b0d6ac745396aae6e99064e9f5fd5b854b9995c342d6d`

```dockerfile
```

-	Layers:
	-	`sha256:d6955c12c8a035e76a9aef9088d0a689e0f132bbe0f859a4dad66d0873737b5a`  
		Last Modified: Tue, 30 Dec 2025 04:27:54 GMT  
		Size: 3.1 MB (3140082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a055316c57bd40d178c5606c65c44924d8b0332d4958bfed5094eca80c141f3a`  
		Last Modified: Tue, 30 Dec 2025 04:27:54 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9767c667ec850d2655bba05063d43bd9f9c621f0f48d7bf7dd631805b1e16bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45130028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70ee6fd8c81e3a49e778b93cbfc649f86e44106aedcc9cdf494d1c5dc501a0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:15:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ce39ac6788a51e8b13d4a8dd0b9b5fc9f3b132f6f7ed2e7fe2821b965beec0ee`  
		Last Modified: Mon, 29 Dec 2025 22:27:50 GMT  
		Size: 45.1 MB (45129807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8cbacc51e181a95c21a3deefbb9da69b4f29b1e725e74877f63a91708e3068`  
		Last Modified: Mon, 29 Dec 2025 23:15:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ea6857de2695b9d8e7838e2d2ff1b20bb91d9ec9258e361e0a6314ec51dcb518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5651572eaba0555b572632ccfaa90b0be749f68cf709d2d43c890ec04df7`

```dockerfile
```

-	Layers:
	-	`sha256:949573e5784a784ee59a42c05522961417df2a32af7b2abb0b41b92e73f8e303`  
		Last Modified: Tue, 30 Dec 2025 04:27:58 GMT  
		Size: 3.1 MB (3141450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c868064ba20fb160ea8f5b833852fe810ff4821b35ca17cecec0698ebfbd3e34`  
		Last Modified: Tue, 30 Dec 2025 04:27:59 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:214b9977f13bad7ad98dd8a06947af9f5539d8b52b493714e21c8f5b206d6e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48832217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b3988242353c9ee4e77ecb01287b3a070a6d6745b57e82ef45d48cfb943cdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7e1126b01c9de189d1405152c74b9a40a3f428e4a1cd28f6a8d42a9464c64c0f`  
		Last Modified: Mon, 29 Dec 2025 22:30:45 GMT  
		Size: 48.8 MB (48831994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a99152a31db96f4597ed52c3b563342dc84c50950912a03ddfd47f0cea845ba`  
		Last Modified: Mon, 29 Dec 2025 23:15:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a71a34531add46eda8efa2b2aef2f7eb99d87d69b070981c56fe5edaa4af2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e1e4598d9baeb3a5eb0058eb3cf989f40847b534bcc6ccd280ce09c32db463`

```dockerfile
```

-	Layers:
	-	`sha256:0d7bf9264d55bdb976f1760d0089a3b69016ad9f6c64fc8567550dedea13de65`  
		Last Modified: Tue, 30 Dec 2025 04:28:02 GMT  
		Size: 3.1 MB (3140923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b8f34725740d478303a6cd02f99ae20a63e784acc7109b1f782d893978aaa5`  
		Last Modified: Tue, 30 Dec 2025 04:28:03 GMT  
		Size: 5.9 KB (5861 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:6d1187c53e9b57411985bec1ae1b3007414a559ad071e3711b977224424158c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49956059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b28413ee534a70b48487c7a4b5c15953861b69e7b346120897045e6710d5923`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1766966400'
# Mon, 29 Dec 2025 23:13:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7887716e98e7f5701d50a3bf307f9111710d24b1094712029d4f793523eb4f1e`  
		Last Modified: Mon, 29 Dec 2025 22:27:10 GMT  
		Size: 50.0 MB (49955837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70406897a79cdad4b6e426085cadd8ac22c8375e967c064ab9100a73da3a704`  
		Last Modified: Mon, 29 Dec 2025 23:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6cd7522f30dd17d3a345b8334aaea707f7078b0b2acfe41de6bb27cf11838fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2364382cf2b0db170e03768a8b75c32de45e996be69ecb95622131bdb8eac7c8`

```dockerfile
```

-	Layers:
	-	`sha256:8661e889c0c4812aaf2e03a062e6025014c30570acf8848cd82fdf063a36d166`  
		Last Modified: Tue, 30 Dec 2025 04:28:07 GMT  
		Size: 3.1 MB (3137286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a382f6740420cd6a27dc5dbe20705959fee478ad492022a3b98692b4a68f32`  
		Last Modified: Tue, 30 Dec 2025 04:28:07 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d38b97bd7b7128cd95afb336e9ea07d28f8a83f873c3031c2c367d3c89994dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53522337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c761da3be7bd7435a777f030a279165f3f8518a7a4ce7bcde580dc2565ae2086`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 16:10:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5a75c60b8a87177661c6b4e6d045cd20aa06dba288dc0ccace27182fc9ab2ac7`  
		Last Modified: Tue, 30 Dec 2025 15:10:00 GMT  
		Size: 53.5 MB (53522114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f688ab91f4422830ab18b038bc776477ad7fdc51da7a02ca9a8f5021e37257`  
		Last Modified: Tue, 30 Dec 2025 16:11:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bcdb281fb021477f322bc57a3797e073651d80237dcc0cdb6137e14ae05634dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df088d1d8800f64ac3d37a623bbaca165132c361889b60abafada468c22e7254`

```dockerfile
```

-	Layers:
	-	`sha256:99e64e3143956b16adaea23f70340e402e2559ae932139b74822c4d3c6e68856`  
		Last Modified: Tue, 30 Dec 2025 19:24:57 GMT  
		Size: 3.1 MB (3143585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b52a5a3b3d6e07f503f62c0828fce531fd8250571e23d5ef9b4a13417432a241`  
		Last Modified: Tue, 30 Dec 2025 19:24:57 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1ab30cbc4f0bffc41c095f0d8f63d12ad3ec5face8b5e63fa286444a79828ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf1796f0ad5f931211119362bb4cf6e261e702ca1460fdb471bbe5e07ca0c83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 01:21:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ac562d1e1ed2e5b1e998606fe04229233216c0966cda12231318c26d0697076`  
		Last Modified: Tue, 30 Dec 2025 00:46:20 GMT  
		Size: 46.9 MB (46883498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a2d3e94ff9461c509fa9c63690f4b3e0dc70ebbfd40f9860e90fe92cffff8c`  
		Last Modified: Tue, 30 Dec 2025 01:22:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f669c0d83365f3d3e957883d2cd74468ca229f0a2ebb8926e24f17258209a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eee289b872ec1b8167bc22b6f09cccb5c57435a7cda305711ea46ff33b33a76`

```dockerfile
```

-	Layers:
	-	`sha256:fedd1674626ff306dac2768a48947f85089be9a78ffd2e592d5b462e8b3cd409`  
		Last Modified: Tue, 30 Dec 2025 04:28:14 GMT  
		Size: 3.1 MB (3131580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9e093916d57347823e514e8b39c33caea5299bdf6f2e0967ed081566a47aad`  
		Last Modified: Tue, 30 Dec 2025 04:28:15 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:fa21cb1e7d914a0d575437b526b8cc67798e37a5692980c3352a86e084fdea3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48397775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f69456efa79e8a11314b2a9079d5c1fb46d14b73e4b57044744daee0547fad4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1766966400'
# Tue, 30 Dec 2025 03:22:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d80a003d64b5d1f3f24e1220fdcfc94ca6acd0d70e01a648724ee4bd7b9a4035`  
		Last Modified: Tue, 30 Dec 2025 02:09:22 GMT  
		Size: 48.4 MB (48397554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65df8bf5c7ee69e79b0c48be6458bfb481cc7b82f8c57794930c3aa81ff9ad01`  
		Last Modified: Tue, 30 Dec 2025 03:23:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:546f1d9ed58d262a0ce535365b3d44a4fc9f9d058d01453a742458b19f5fa446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039d9bbf767a5bd2e4c1867ed6c24a73c2cc69a2f7145081a34f3eebbf3ca627`

```dockerfile
```

-	Layers:
	-	`sha256:a9eae77906d86d054ac48ed89804888547057ff11791a0a5f7c9c7736ab33a81`  
		Last Modified: Tue, 30 Dec 2025 04:28:18 GMT  
		Size: 3.1 MB (3141531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a412c2c7fcc847ab8bf3c76770b545732baf6557eccb04dc7e9519b29645a6`  
		Last Modified: Tue, 30 Dec 2025 04:28:19 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
