## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:34899f3dd43a85353045a14614aaabe07833666d284a4f5f5863d1d3a1de26c7
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f7b7027dc93a0d1c150cc99f76e40d4db980dd506bf736b092ac4393f891a70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73887269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06211409eb33ac4947448465c64d937b978d504acbc4b15b49a449dbb502b2a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b43386f4a8eea1a35e7c4f34a0bb12426fd9b88216af22d7c3ee489419eb1bab`  
		Last Modified: Tue, 08 Apr 2025 00:23:13 GMT  
		Size: 47.5 MB (47545414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf061a9daba97c5d47244462ed42ef128857bde7ddf55699ef7e9fdc7b5705bb`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 26.3 MB (26341855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7cf43149634da56eea757638b0a4e55b99459bd5b8e2d730f8f3537a2c046e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4ce4696b0e10d64fdcb47444656d9f04a15ba245f68a001d75c84ecb7bf46a`

```dockerfile
```

-	Layers:
	-	`sha256:e6dc07fe0fe1cd9a60cd6c44d68af06cec8bd70d4e9e29a4295972be71500f38`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 4.0 MB (3968594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a15f9e2605a18b294f3c0cdad7bd6db319c95eccfb93c56024ba91b3902658`  
		Last Modified: Tue, 08 Apr 2025 01:24:29 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eba6adb31ab27c134cd3e27f6ea88cafd91fe39b8c9034438f7964a69614ee5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4923d53830587a77d539d025441178acac3af9e334c14b8af071e0e26bc675d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec645b8b1764e458ae4d21700842e441d914fd80d6e0135fa393952e129298fd`  
		Last Modified: Tue, 08 Apr 2025 00:25:30 GMT  
		Size: 45.8 MB (45786687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9068871a08a0535e32e79d1a45670b225b99f46bbc4e55433b3bc2d040fea9`  
		Last Modified: Tue, 08 Apr 2025 05:13:28 GMT  
		Size: 25.0 MB (25013942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75641b758be26a086004e6464cb02aea26e9544f375942bf5e927adcbdb9fc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0068093c6dc2be1c9ff8ad01e0964a5456f44bd558f9fbfae6b6c91b25ae74a9`

```dockerfile
```

-	Layers:
	-	`sha256:22aca250853d806519dc4970bc167babf6b63511d21b0363e4ba94e54df0d970`  
		Last Modified: Tue, 08 Apr 2025 05:13:26 GMT  
		Size: 4.0 MB (3976857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4127ebf8c8540e1ae5df709841a5524d5a73a2ea7dcc756999b375959e89eb8`  
		Last Modified: Tue, 08 Apr 2025 05:13:25 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b39c67bb7de548f2b5ad9f7ea0a0f211e2a8d1d50d48203278df043e10add50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68164605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f1db77ac613e5e7c5068e2f38832a0c4e1ff13acddb7f13df9414d3b760871`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f935b3012df284a962222bcccf691a593747f69aa524b90eccdcf9bed048a7f`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 44.0 MB (43962830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705c4ef1fc9cf5c68338bdc47ec99f95384a22547d22ce9113fa1a4477154`  
		Last Modified: Tue, 08 Apr 2025 07:39:55 GMT  
		Size: 24.2 MB (24201775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1983bcb28facf650db24f123adc1b418e69060aca10789cef6558114845fae0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b1de599320f27a86e0fc360b95bd62e6e062668fa5a5675de6c7b7edd895f`

```dockerfile
```

-	Layers:
	-	`sha256:ec2fe1ae0f8e7f9ae0a1669be7f0683afe72f9d73067f511ff5eceb1dc72c80e`  
		Last Modified: Tue, 08 Apr 2025 07:39:54 GMT  
		Size: 4.0 MB (3969447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4755a57bbdb681e6cc9e3c28f17d98d5b012a0dc3d01d9c145e09325e986fb`  
		Last Modified: Tue, 08 Apr 2025 07:39:54 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b039666763cddd0d240336958f4d49e81c541876e52b3afa0f51936550624686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73650572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225622767af9757b460bf48f06e944b54afd6eff198c4b578a2210ade3ba5316`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60dbfae895846be1589b057802d5cd4dd276320555a3dce75612dc628209cb7e`  
		Last Modified: Tue, 08 Apr 2025 00:25:57 GMT  
		Size: 47.9 MB (47922433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7cce4b3d3d4958fcc2ffe1fbbf0181efd0f5febf1b3b140f3c5fb190e3e83`  
		Last Modified: Tue, 08 Apr 2025 06:04:42 GMT  
		Size: 25.7 MB (25728139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d46f4137be5ec8efab8adb9a4b49f234df59c4b79bace7973e5a254ac2ea2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aecb5977c07f20c0031f6528ff70dc9a272e056cf275b1788262441a73bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:0e46af91437af27781429ccb51702ccb8b38e02093584db9bc61ea2367c0db85`  
		Last Modified: Tue, 08 Apr 2025 06:04:41 GMT  
		Size: 4.0 MB (3970125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86dc51c723da2b5174b50f5a8cfe212e003f7d8e83a21d1e7576de08deb8a24`  
		Last Modified: Tue, 08 Apr 2025 06:04:40 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ce9bb25f72d1db13f990ec9579b96039f0bcfe873b48f1254b8086b3f26556c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76319764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f69e3140767fcd1fb197300f9f49b523c8669b3618f3c9a65d2f0dcacdb5b74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:091329a1d6a6197a5d3e206472c088a0858ef7008c0ef0caa690ee6550acc80d`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 48.9 MB (48867484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fe46607c901c693e43f5e041d9582f12c310a5a19737459269da4c901faa70`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 27.5 MB (27452280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e570ce3dbf1211d779e4cb42bfeb8d4cdf319d573bd81e4082c5e5f9900f06a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b865202124d3a19aa3528540a5af74ff3f96ea88dc1802e29f916c31dda167`

```dockerfile
```

-	Layers:
	-	`sha256:2fbca0ff51f1d167e8e2c185870f43f76c846ddf4b2965ef9cfe91877fad1ad6`  
		Last Modified: Tue, 08 Apr 2025 01:24:19 GMT  
		Size: 4.0 MB (3965006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95df3d53b0112639245b468204f5d141859461261aec104904502e308b09db8d`  
		Last Modified: Tue, 08 Apr 2025 01:24:18 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e67fde04bd3178a9887bdb8f3963628390dc388ff7ac17136a91d66ac88a0d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74005715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0f3b3f8271c3b6026b8da272f22b9688abdeae7c82b686250739db7a0649f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:46069a6fb0408c39827d84c4f957cdacbea0859425bc5cee1431cc570428f262`  
		Last Modified: Mon, 17 Mar 2025 22:19:48 GMT  
		Size: 47.7 MB (47726922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024e8bce62fef1bb0a0244ed9a2bd73704dfdd7237b2039638682f562d4721e`  
		Last Modified: Tue, 18 Mar 2025 16:27:50 GMT  
		Size: 26.3 MB (26278793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49c579f657beb3d6224f9e56656d2053ecdc7b62c77d5782cadc1ffe0673c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629566828865043b2acd1b8e5eb35c74118e39d6a0a6d8f8cda93ea446b2ce32`

```dockerfile
```

-	Layers:
	-	`sha256:d426e778648ee276cf0e377a3582173a73b86c0c4e55b0f2123a496418229eae`  
		Last Modified: Tue, 18 Mar 2025 16:27:47 GMT  
		Size: 6.7 KB (6653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ca1e695bf0ea6c3ef638420576b9f2e1abcc88eb07c3910b45ab799ef057d515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79046871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff61944945065e54eaa71b7b31e51dd790a6517f4b0f772d6312e420661d01d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2152bfaf5665d7c627f661d81f1ebb038ec9b798a3becef3f95f6ec6dfa2adf5`  
		Last Modified: Tue, 08 Apr 2025 00:27:27 GMT  
		Size: 51.2 MB (51205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0924c3716841f5effee584d0edc58283639e6ed70d2000758424dcc55e8232c`  
		Last Modified: Tue, 08 Apr 2025 04:32:21 GMT  
		Size: 27.8 MB (27841786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10bb5e5550cc8080be855d33233c3d2db101132dbb6b914e6bc29d77c89a3398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca74621c6640202d32fc6f6d873a71eee688ef328335e47759792ee5b05581d`

```dockerfile
```

-	Layers:
	-	`sha256:50ea3e4675d041dda2312ef9e098a5fc2ba731bdfbebd7ad99a25fb1d6a3613b`  
		Last Modified: Tue, 08 Apr 2025 04:32:20 GMT  
		Size: 4.0 MB (3977859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb0da1a6696b27128ed4ff4f96fff15c1dadda054fd16bc727c1219527a7a42`  
		Last Modified: Tue, 08 Apr 2025 04:32:19 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:85c2362950bfb2b6928a2341b3662d7ae95bdfe895f29fd5199dc0c4c54d4d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71708104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6530ece883f52875c0a60311359a0bff116da3c786858d6da325e563ec2167e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d049c0e21a4ad6e8db102828b8d03bcd0730a934f6305fa31bc0a4e2bc6af6d`  
		Last Modified: Tue, 08 Apr 2025 00:31:42 GMT  
		Size: 46.1 MB (46072980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9e23969c469610d4b7fd0c3d4fcdc71ebcf20493b72a3bb5e5f56295ca06c9`  
		Last Modified: Tue, 08 Apr 2025 01:25:33 GMT  
		Size: 25.6 MB (25635124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b51d5335324b30b83f11521113871dcb1650eeefa45e30dc4d3dc0a48156f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8990559324b6b35ccab57ada481b07ed116dc769cef274d5e60e989a046e9377`

```dockerfile
```

-	Layers:
	-	`sha256:f180b5dc93dc401cffce2f471bd7a3b315df859d743799d6effebf80d473f226`  
		Last Modified: Tue, 08 Apr 2025 01:25:30 GMT  
		Size: 4.0 MB (3960592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60b945f4ed0404baa7dee4c5bdb123ff5a9376900b1c7709cbb927856113cef`  
		Last Modified: Tue, 08 Apr 2025 01:25:29 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:573ef29bccb79eaec4928df6314513445a44dbde01dbbe0a17a42a4adc71597e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75147204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0f1da3bb4fe21aadc809b1f2da9c7b9f1c3ab6314e087fd3ae3b4fb0b3cdeb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:19a5a2e5eb505d0c1814e6d65469ecbbf0abf7cbe214ddd85cb24c5fb088dc02`  
		Last Modified: Tue, 08 Apr 2025 00:27:13 GMT  
		Size: 47.6 MB (47577872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a838b52d3c41c71c15b487ddc0ce4cada3e3fb6a44e40511f7176fd1633521`  
		Last Modified: Tue, 08 Apr 2025 03:45:39 GMT  
		Size: 27.6 MB (27569332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4179cddd7310cccec4a3ebf9e792a2627069b5d88c64720840b5db961ebc5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3982388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c4fc928bba41ad00f0f0685300b5866fe8a3d2802cf273c8239331f5cc77b9`

```dockerfile
```

-	Layers:
	-	`sha256:98447d6a93689f01d31f72f8883c9ed7b8bb8eea46e4e025fe62081e94b0d540`  
		Last Modified: Tue, 08 Apr 2025 03:45:38 GMT  
		Size: 4.0 MB (3975567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdeea108200648db8b0c67dd296c4512e3cdcb5901119e200ab1f3eaf9d25f6`  
		Last Modified: Tue, 08 Apr 2025 03:45:38 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
