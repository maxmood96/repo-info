## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:44b79c59e495ed53cd6c30f2dbd135f4b87c7d1d2613a55ab2c393fce501f868
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1d6bd5b73c1e25690c8ffe35ea5343f57fe4ba4ae4627184151b2f84511b58f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75697956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a697028c8f9294dcc049664fe94313c58591822ef1a6d13de738de70303ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e7f09040bcd4eed376c1a5f9491753b37de5abb58b8a75ba459283597e98a`  
		Last Modified: Thu, 11 Jun 2026 00:42:43 GMT  
		Size: 26.9 MB (26918682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf9d781f4f4a64e15b2cae9928b96fe2b2c746e88940780a52d498b471e0f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2076f7ba44c80dd8c2415f31ece0ecc848c2cfe492e0e6d339397aba57bf9619`

```dockerfile
```

-	Layers:
	-	`sha256:401c7d29aa38e4590e42fa17128f910a98b3a7383dda26097e15b2d964683f70`  
		Last Modified: Thu, 11 Jun 2026 00:42:42 GMT  
		Size: 4.0 MB (4048957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5c6d68b644a91b4d906f34782e8ff35211befaa5d948b518a7926bedff63a7`  
		Last Modified: Thu, 11 Jun 2026 00:42:42 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:56ff4a2e1d5f58810021c2c9b10265d4c4c703116ae349564279231eb3823f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70256194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b8f3da97e1a5550b5e0843ca74726230499fb74723b7654061533620d91d37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd14977d91415ae0c2f3a09dcc1dbfa071bbc9d1eaf7ceed6655fe0e671e8d27`  
		Last Modified: Wed, 10 Jun 2026 23:41:34 GMT  
		Size: 45.7 MB (45676562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f62967a713e6868315df8fff6281864c11e6f1bf85c4ff4746f06a1c2c7935c`  
		Last Modified: Thu, 11 Jun 2026 01:25:13 GMT  
		Size: 24.6 MB (24579632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7899a37db2723f2d5f79cef4b264227ff64ace7b7205ce9240938066520ab5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab235d161986bdbe8f0d449756e28a88366d46522053eecef2efef1b33dd97a7`

```dockerfile
```

-	Layers:
	-	`sha256:43a72fee82aea5a4201119d50d98577cd81c406f557e4f13fa88d325211c5668`  
		Last Modified: Thu, 11 Jun 2026 01:25:13 GMT  
		Size: 4.1 MB (4050444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4de2109dbe89a9622cad02f4f8a50ae0926d71f6519797883e023ffdac2fe92`  
		Last Modified: Thu, 11 Jun 2026 01:25:12 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:62f874930f9a4fe26946a54ae9d23fef34cd59f0d339a2caf622a7e05cedc5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74976426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738b7273d147ec05574fdc119b7f33640b21b3060775869b6ba96ddfdb6b8c23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:44:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ebeebafee761b67c6633aca1ce7141531b193dc4a7a4858fb1b0cd75f8462`  
		Last Modified: Thu, 11 Jun 2026 00:44:25 GMT  
		Size: 26.2 MB (26180818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c84a7284129b371f2ed3d2c227c6b27f1a247c0217bdf70e9d51750635651f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4061168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f8a11587a45f66e3415e8b1f2bb8ba06ba43150e3eb0de80b2a2360eb9afc1`

```dockerfile
```

-	Layers:
	-	`sha256:38582bb92da554036b1f5922ada2758f858e707974045313701a5f72d7021845`  
		Last Modified: Thu, 11 Jun 2026 00:44:25 GMT  
		Size: 4.1 MB (4054316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588f90a6efe3ea9f9b690ec20a59f4b46b474d77d713d132db8a3c3a1ad15272`  
		Last Modified: Thu, 11 Jun 2026 00:44:24 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d161507fa8f6a1a6e4fe50ba0f1d45f7a3c997092a1b46b0e8634cf9345a2e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78241741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904effb086e487426388f3fd42af57d60747c49612dcd84490655aacaed01002`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efb4928ebe54ee107e6463403a2a4853abe521d8dabe3603a0df92499fa85ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 28.2 MB (28164931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d5927ebae3fa7de36738fafb233e4a0c23baa7e8905e486c97965a78ed12f9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b50980b8ede8ba47c25a45c946a930cc9d8e98b28a6561d2e87c4843096601a`

```dockerfile
```

-	Layers:
	-	`sha256:3b75d944f9e4dd142336c514a515668be2b9fc1112afbff4b42e8a90b4fe42c5`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 4.0 MB (4046067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1c86227abb54ce198e26b4de1fe828e8d8e656e40519304042160874da865b`  
		Last Modified: Thu, 11 Jun 2026 00:45:10 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e59d4a1cc7bf2d9cccb2cb8b74000e9aad4b5738a77b83db3a92d85c40da06c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83389746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23c234428286e8dc259b2a67d0392189cf93ddfee226f25a0ba1e70cd78defc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a6e9fc5fff5ecef539442636839ebbab04ed9b3cd7caa39a93b1023297047494`  
		Last Modified: Thu, 11 Jun 2026 00:22:03 GMT  
		Size: 54.1 MB (54103105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ae67043641e8afbaed6931d7c5b7fbf2860dd1ffd02c08f3ccdcf4f71c0dc8`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 29.3 MB (29286641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a768843970cc5a5c1ec40372a84caa397db30720c9da9936ff2604496398380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43003b6ba0a062ba2a740500e50bfcb4ce18d4079842bd4ca16b9a1e7bab0457`

```dockerfile
```

-	Layers:
	-	`sha256:d4a631d8671cc5c5eb944f74b1e55b6d19fbab3c432346aa817c6430f002e75d`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 4.1 MB (4052801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657505c9093e3fc1b5b4ced68a1537c7c953f4bcc136771c43c130d7c16f7d72`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0667033362d6b463fe6235c993be673382f0ee1749384d943391a3eccbb68a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73285352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79475f1c6f62d30ca1c3f37ab42af5322e9efe9350dfbd0ff7807331eb9c2207`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1779062400'
# Thu, 21 May 2026 13:54:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233e2e85000f46d884ecdf2b81662e2915ae4bce2cfd6a573318e4ae99ee6839`  
		Last Modified: Tue, 19 May 2026 23:36:02 GMT  
		Size: 46.8 MB (46833187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa3768beafc01f566f53361a18d9c7150398a0575500ad1f3d3da15fa52ceea`  
		Last Modified: Thu, 21 May 2026 13:55:52 GMT  
		Size: 26.5 MB (26452165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b75148b515b8ffdee20cf823e741ae894f747d766c94e99e53e9d9a3b19ac02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4065860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ac5c27180f312595218fb833efbcbf5c9b0dacd09cbe3c34033fb4851d8345`

```dockerfile
```

-	Layers:
	-	`sha256:8ffe4ab35d6cb5261bbfff35c1563746ea7d30b81517f4ce15ca1a2f3fd70009`  
		Last Modified: Thu, 21 May 2026 13:55:49 GMT  
		Size: 4.1 MB (4059055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5e6bbeb2b614b360a50971e2476a3078cef59405e6c310564d43f0cecdad4f`  
		Last Modified: Thu, 21 May 2026 13:55:47 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:27f4ecc897aaddc77218422e3e649e62f8351bc099f59f2427f557682766cd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75193222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdcbdd5aff190911ffcd2194c99661529928e318e0811be84930d176287bf4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5198203a924daa24fe6af49f715c31ab29dfca39eea778fa09abc744d2bad231`  
		Last Modified: Wed, 10 Jun 2026 23:41:11 GMT  
		Size: 48.5 MB (48513108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede4a9f8d2cf16954d7483762c1a757bd649ba11bd48dc0e08d51861877f2e58`  
		Last Modified: Thu, 11 Jun 2026 01:44:12 GMT  
		Size: 26.7 MB (26680114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d5e269cd0e98b04b2abed7fb77af4b92258bd7537619514a50241eadc596cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7238538e9b09e77a3196ed010fefcbabe1f65125ce457f1796d7c6375f9ee5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6ad4053c76a432e23ca544a33d949ac5e8d6fc3363d5fc5588582593d09eae`  
		Last Modified: Thu, 11 Jun 2026 01:44:12 GMT  
		Size: 4.1 MB (4050369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b70ee98f753c18bde8a0f46eaac33ab85a55a7216e021207276277cc980a36`  
		Last Modified: Thu, 11 Jun 2026 01:44:12 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
