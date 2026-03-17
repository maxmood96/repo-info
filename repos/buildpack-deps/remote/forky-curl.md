## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:b362368092c98cdd5840967b4ade8356d29b9be871adbc38bf4a2f88d51bc280
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42a22e0d7e15f304ec93ac2c59b860f18776dbd136011703ce120a0e5e0c6644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75673590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d6e9df6b700d83a23d66dc1ea67a4a1aedc8405559ee1e5e3a0caf3fe36f87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544a38ddd1390105762bdf349d1e32b7cf1a9f82dddf930c31b8042b03c6965`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 27.0 MB (27048499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d40517680ebc3525e1c18f155e719891a7a59995ccac5e12b7b2e10e9803ab13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4082007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632dd37d9c59762be87ec12b21a5682f4d2afe3cd538bcdfd3e68e27bdb5454a`

```dockerfile
```

-	Layers:
	-	`sha256:a5a0f1d8b6b795d78325dbfa67c32336e3935ee54ae0ece15992b33a87f71fff`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4c7a26a062cce8673a32b58edc9f8e8264c88b895ed4c26948d1be4b44571b`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a49f72256c39d2a7a2d1637d87cf28f194c186ba08845e1ae5ee0c0f543f910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70291000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96debd1f90fc718dc16253fe7266fd8e7ddfd74c7b648fa5da40ea5fd3fd288`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e808829cfe5315cd67981f1a90877f9ceed482400b0f64a9a61a5068bf2e2381`  
		Last Modified: Mon, 16 Mar 2026 21:53:22 GMT  
		Size: 45.6 MB (45555225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3a3183174d50dae2f383480aa0bee03715dc30a220abfb476587db07c5672`  
		Last Modified: Mon, 16 Mar 2026 23:20:29 GMT  
		Size: 24.7 MB (24735775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ac19b5431c057f6cf0efbcbd565a053ecc60774a61a7642e24336d2e7072812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49479ad8610bf5882c20131612b0a3187d32ff27bebdeb03d622e2325a7eb90`

```dockerfile
```

-	Layers:
	-	`sha256:17fb4a7ce7b7db1d6ed3e25be8d59257169806603d7039620fb83f809798056d`  
		Last Modified: Mon, 16 Mar 2026 23:20:29 GMT  
		Size: 4.1 MB (4076726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0614c88647a3cf31b15c793c1b1a24dce3e81575e955e0ed555289d74b9594`  
		Last Modified: Mon, 16 Mar 2026 23:20:28 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db73609e03c4454f1c75f3d0b1e87d21f277c2d9fa9761307f27ec978255e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75003649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad1e097203b7e6bb7b436827b48db9dffd243176e51ed7d2dae4e85a1f09e45`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873916964a227a18ebb04ec1f407f168a33886e300682cbd4848c61bc623f448`  
		Last Modified: Mon, 16 Mar 2026 22:40:19 GMT  
		Size: 26.3 MB (26344588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fbe20e198c509dc3ae2950d2334dfe583fb852137629bd2a3d506112c91b59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275fa216ab048d7cf2530b0911a65325a7699f78585bf380e1043e81786173c8`

```dockerfile
```

-	Layers:
	-	`sha256:23cdf2792776b8cc1779d0c79c76d80d8e5cbbb6d3545823b532e6333d26459a`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 4.1 MB (4082692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ada82aa35df6dc3707de9d75a5943ef642f9f0673c506b23278096fa6fcdaf8`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9d3fc496d7828b648009589771776854dc88ab6ee1afb2865efb75b640b95d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78230283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8832ec330e80e68084228ccacb4f7299caa9922ca9473ecc9a7edbd71f8b109c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63597877e9ce45a8d644c87f2edaa1b6f60b392c0f8a5049196e27710801057`  
		Last Modified: Mon, 16 Mar 2026 22:44:13 GMT  
		Size: 28.3 MB (28310412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8d618b29f6693119cd858d62415fcca5c9abeb56814459e74a25225b1de9d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabaebb77814f1145520553e0ff100e784830bdada3ea88a7441aad12334b402`

```dockerfile
```

-	Layers:
	-	`sha256:8523515d067a17d6f1e0ebd113e91f28ade49b39788b242aa452c5f6ddf3a2ab`  
		Last Modified: Mon, 16 Mar 2026 22:44:12 GMT  
		Size: 4.1 MB (4072343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a48fdfd5e27133c8d4f828e68da5a3fdf88519b39565f5f49bc4350069296`  
		Last Modified: Mon, 16 Mar 2026 22:44:12 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fa109280e8cfd5e4e59fe6ccb44d2cebc5f4daafb97d0f59a5793528ccd88d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83197721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db983c997c76b046b08c64d40e1012659c6e245c1fe27dc9bc88c316e552411d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1773619200'
# Tue, 17 Mar 2026 01:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75936ac254db13d0215c75f5fabecfedea28136e3ee0cacb89bd8884668a56af`  
		Last Modified: Mon, 16 Mar 2026 21:51:49 GMT  
		Size: 53.9 MB (53863314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e0924d7ad541b2109556dcbe1d5d7994260b154430061685df2536f4aafd6`  
		Last Modified: Tue, 17 Mar 2026 01:50:07 GMT  
		Size: 29.3 MB (29334407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b67fda30bceec37c82e06f70584a0bcf55b0f01a43ce5a2139d7e834e0c342ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a788c62e8e5a4d95971a44d86db2c6addf2dbbe2e76b2e1cc58d5354454114`

```dockerfile
```

-	Layers:
	-	`sha256:c80990e9d670fa1a1301cc3ec75e0a421001423ef73cb737f345906f573d1176`  
		Last Modified: Tue, 17 Mar 2026 01:50:07 GMT  
		Size: 4.1 MB (4079091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9800203e8998737f19628b60ba68ac94c5f148492b9bd137dcdd35af4006ca`  
		Last Modified: Tue, 17 Mar 2026 01:50:06 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:975d9381587ce6aea81d26de04bbb50a01d26e1adbe437e89e6cf01e358cd0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73320869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05038bf99ae775d947eb35f3d5a4f21e3ae5ec9bd4dad1214c5770f3e7b2d6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3fb5c15cbddc0ebbd7afd8ce992f6bfd6f0d5d4b1d5f4e672c5fc7451f1119d`  
		Last Modified: Mon, 16 Mar 2026 21:55:37 GMT  
		Size: 46.7 MB (46721467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059cd42e31b5d0cd1848f67940ca871c5e491654382eb483e7231a6e0aedfb85`  
		Last Modified: Mon, 16 Mar 2026 22:28:45 GMT  
		Size: 26.6 MB (26599402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd807e7bda091ea2ef64187193526d724e60676788a71179d0028b33ea0e37f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd81c6cac2e374f106f47bf5d5e3a97ad18fea81b38fefab76caabf6d8260cc5`

```dockerfile
```

-	Layers:
	-	`sha256:ffecca908a353bdaa03405b042d507080b131b4b4376a7b34a0c26c5b5cfbc98`  
		Last Modified: Mon, 16 Mar 2026 22:28:42 GMT  
		Size: 4.1 MB (4066934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8dfbf0d9c3de45f54648517ff279f8e0f690fa91dfa562fe7a99b7beb3f5ac`  
		Last Modified: Mon, 16 Mar 2026 22:28:41 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59b1eadc0f737db6474b1be5a68c063c2cd35de493d781e56404957a6622f344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75165883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5980345854ef312ebe54928e46cbab2b46f66802aed5f5d2a4ae432cf4bb3dcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f87b2d0069bddaedc5a87fced2f3e4651a654b1dbe947403a098a2d5a2045522`  
		Last Modified: Mon, 16 Mar 2026 21:51:42 GMT  
		Size: 48.3 MB (48334622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b950bdf154265cdadd06df13c221ac2b053459e6309c7b38bd12f5bf75dd0`  
		Last Modified: Mon, 16 Mar 2026 23:45:01 GMT  
		Size: 26.8 MB (26831261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eeea3bb4945e2ed1886dd01ba605bf44881d09016d7cfb5259a17cced5c02eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9288aa06812f17254d6be242fb44cc944be2111ccb2411922f6ba7a43ad25e`

```dockerfile
```

-	Layers:
	-	`sha256:55e912201b0e5991ffbc34488a435aaccfc6fc2afe5d5e99f9e58377565d140a`  
		Last Modified: Mon, 16 Mar 2026 23:45:01 GMT  
		Size: 4.1 MB (4076647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22229a332aeba9ab28f808b9b32671b033ed8f08a2a9939d58487b96fe2c27dc`  
		Last Modified: Mon, 16 Mar 2026 23:45:00 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
