## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:ce83b2eefdf8af2ee771d36771f8b6a7ba32c9dd5bd6d907d205b506e0d708a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f679dfea28b543518362ad66cac6b1240302cdfc6f6253e1529bd0c0063f9ccb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130899946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5065f8a27ab438502224d3d8c878db108e01f3cc1d35cb19090300d6ba573049`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:15 GMT
ADD file:7507edfdf016128615e9ba278d471fd6d27c96436e543786b691c93b6f94b56b in / 
# Tue, 23 Aug 2022 00:20:16 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:46:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 00:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e784af754e1c7855decd29b818520a98b5b539515cd7c199c5dbceb6cc4a45f`  
		Last Modified: Tue, 23 Aug 2022 00:23:57 GMT  
		Size: 52.7 MB (52725730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06352499c53ea1415d7d7121128de838e832cbc465b145c71d05fb7b74a91c0`  
		Last Modified: Tue, 23 Aug 2022 00:54:04 GMT  
		Size: 9.3 MB (9298815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e88fbc1ce3af2aec72e131f3b876f2554849f8d6291840fbaf61b24970e54c3`  
		Last Modified: Tue, 23 Aug 2022 00:54:04 GMT  
		Size: 11.3 MB (11272439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afebddf0d45a19b246f4ff1ead1dd600b48cc494afd00873819774f29c6f388`  
		Last Modified: Tue, 23 Aug 2022 00:54:22 GMT  
		Size: 57.6 MB (57602962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3105bd239c37e60837e1152b015daee62157823c6186560f332829781987f835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126978393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa0efad72770996ff195a6185c02ae8f73060c3b553bd4d4488ad2802b5c580`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:48:33 GMT
ADD file:f83bd7c88ccdb8f7b53f9072524438c8262a71b297a007c804923fd6d817479b in / 
# Tue, 02 Aug 2022 00:48:33 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:17:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:18:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:18:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f721a266d53173a0af0b138649440b41e425660c1bfb8506b479507fa2627c4d`  
		Last Modified: Tue, 02 Aug 2022 00:54:42 GMT  
		Size: 51.8 MB (51812934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6a541c310c2e2f0c838ea71f560b2bf4a91d0e9c4c71ab80c566d34acaae98`  
		Last Modified: Tue, 02 Aug 2022 01:28:50 GMT  
		Size: 8.7 MB (8739729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928c72f00c51da560bfe1136e59212f70544fcc07732cc6b7156db46dbf7d55`  
		Last Modified: Tue, 02 Aug 2022 01:28:49 GMT  
		Size: 10.9 MB (10946664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd933a4710700cd7753f9558b1a5e9d88dbcb1fec5686f8fe3ad6a4ac1556370`  
		Last Modified: Tue, 02 Aug 2022 01:29:18 GMT  
		Size: 55.5 MB (55479066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8fc0a6c05eeef801698c54fcf6b06ac324b09b513524c83e96de3380df8d8a66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121937828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89a848cabc8d7fffe43491f3a7d15af3948d0cf61dbc0902f72a7801ffe4eaa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:57:55 GMT
ADD file:359193f5179bfdc5181bda2e05bd0b22ae4a86c638b0bbf09f289d1727fad222 in / 
# Tue, 02 Aug 2022 00:57:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:45:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:537407bee93780ba0135c6d74e62d8cee8d32e85ab926669d3cc9bedeef28852`  
		Last Modified: Tue, 02 Aug 2022 01:05:20 GMT  
		Size: 49.5 MB (49527674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21e0c1ecdb66b081e679eaee092b97020507b0a7735843a508a74b1ecb86429`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 8.4 MB (8417992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2371236f490dda856391359574a3e2e3ecf9d8d39f77649c8c6839a1846326`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 10.6 MB (10589533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503864111e2b00823bf24541ba248d5caaa84e32bc41634a765833fba8201148`  
		Last Modified: Tue, 02 Aug 2022 02:08:17 GMT  
		Size: 53.4 MB (53402629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8c68e44cc2bc98f82cb089da481771ffee0a744194b24c8dead56b0424334754
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131096553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982c5ff9f84872de496b70238b5171fb7f22861d0e123ff6ae1602403fe2ac18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:01 GMT
ADD file:66ffd29b395276f108023b4be1a449714b6fb1fcbcaf770debb7ec6910e84294 in / 
# Tue, 02 Aug 2022 00:40:02 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:22:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:22:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c76fc726ec0ec853818bf6b42fbe47810086904b89f146d4ccce624e8c5a33e2`  
		Last Modified: Tue, 02 Aug 2022 00:44:53 GMT  
		Size: 53.1 MB (53097492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446351798668b67b250456bd33621fa3f1239a40db1aa52cbae04c3c1524f3b9`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 9.1 MB (9148571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a6b5eb548691ce9ed80e732c56ffc57a9ff5c14103b158596eb92a0508c44c`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 11.1 MB (11062330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72738b07767d36266efbb85e749b932d343b20eb6acafb82341aa301f4d3d80d`  
		Last Modified: Tue, 02 Aug 2022 01:43:43 GMT  
		Size: 57.8 MB (57788160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1a6e04486d701fe9f175abed959a5794adb184ded2d14ea520fda84aa445ba9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134148274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8346a4ca2444870e8bb65aff75d4d4cf6711229035f48bacd81de5aee6ec3ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:01:59 GMT
ADD file:1c8ebe8b69a2d3c236c8a947162fab2e579f4bf01bff01695a3c46557f6c73f4 in / 
# Tue, 23 Aug 2022 01:02:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:28:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 01:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29bf8f676853094720e43096224f2ec8a31ffa3752cf7a1e52fb9e72ae069480`  
		Last Modified: Tue, 23 Aug 2022 01:07:13 GMT  
		Size: 54.1 MB (54096938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0426ba96c16ee4ea8eb5b5322685d94b842c455938234d92ca07814c6ae081`  
		Last Modified: Tue, 23 Aug 2022 01:38:51 GMT  
		Size: 9.5 MB (9475146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86201f3e5308e2da4dad080700c08b4d6a0a02c265e56c7a0cdae2889f16b442`  
		Last Modified: Tue, 23 Aug 2022 01:38:51 GMT  
		Size: 11.5 MB (11473600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eae1a3c8a2b637c155af3a0e81b010eea8632db588e887a59f57d020ad81a8`  
		Last Modified: Tue, 23 Aug 2022 01:39:11 GMT  
		Size: 59.1 MB (59102590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b21d0431bca6b1a4d7183ac3aaaefb8b63fe0a07624964800dc7a60bec965db6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129234962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf91bae60c8a79f0a9ec5a2f9ec06295d42e0872511c8b3b37ac8997b283832`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:08:47 GMT
ADD file:071fbdfd189eb16d9f6ef75de927dc676c1f54b47bc4e17163522108782b28ec in / 
# Tue, 02 Aug 2022 01:08:52 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:45:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:47:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d875d0bc6e0221f25e9536bae93056c28a4346ebdefd9847e38ca0c0b536a4b7`  
		Last Modified: Tue, 02 Aug 2022 01:19:01 GMT  
		Size: 53.1 MB (53099858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcedaf5d854c546aa8dfba8a69de72201352b43af6678144af78e6ba1b4eb4f6`  
		Last Modified: Tue, 02 Aug 2022 02:20:57 GMT  
		Size: 8.7 MB (8674895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb36366f74dff43a81dc4efc0c8dcf582b8f4dae63bff044706dcb2816f1d22`  
		Last Modified: Tue, 02 Aug 2022 02:20:58 GMT  
		Size: 11.0 MB (11041565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea48d16111b1cb59aaff2b057672e96116d9de657a96d6821918a319f7d6e2ec`  
		Last Modified: Tue, 02 Aug 2022 02:21:47 GMT  
		Size: 56.4 MB (56418644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:447ba81241eba47463c5b36c21a3edd6e4f3c6c440c50630a9091262e1576676
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141640382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478fae8b9e1bc0b2963f91a7d87ac15ef547617d32eacd435ad01354d313b2fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:16:36 GMT
ADD file:c74b95bf7c5e132f531cfa82f2087d3674d54ec0a5ffe1b63c3b2c23982544d0 in / 
# Tue, 02 Aug 2022 01:16:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:24:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 02:24:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7626a07e3e0f205ede86e25585175b90c4c7ab30a82060614ed072b13dcb055f`  
		Last Modified: Tue, 02 Aug 2022 01:23:07 GMT  
		Size: 57.2 MB (57221780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679ead450c4678e5e5e6dc20d546a04b10e34c37d62721990cff7656d8d92f1a`  
		Last Modified: Tue, 02 Aug 2022 03:12:10 GMT  
		Size: 9.9 MB (9903777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92405a109badca902d6e604ad9a407f0d91a60836b63fe93710ae9fbddc4f2e`  
		Last Modified: Tue, 02 Aug 2022 03:12:10 GMT  
		Size: 12.1 MB (12083652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bfb5cbdcbc17a1c78484f166702574839bb7bf127f0907db3f2ebf37745a68`  
		Last Modified: Tue, 02 Aug 2022 03:12:39 GMT  
		Size: 62.4 MB (62431173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:01cb9db2d699a4b3e8dc4ad559547396dc89b1ad228e765e271c03aecf0cdcb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128660767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a81c08d543805e3dd7826c316f119adba06c57f286366061d6b979d482dc7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:9364324d9e3e24a6e417365a226c42bac5c3c9589b444096a65d5bf539eec127 in / 
# Tue, 02 Aug 2022 00:41:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:07:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a5bd7c6618b65a5948f8c07805e4109ef4f5aac36711b43d0fabe6f11fe0ec8`  
		Last Modified: Tue, 02 Aug 2022 00:47:13 GMT  
		Size: 51.5 MB (51514530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c61b0b54c9dc1946fb336e5a04c532d39a45e681f19f307f477085013dd8bc`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 9.0 MB (8952435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edc88e19b9b0261e01462a1883dcbc8fd4849c5a80450a4659c246ae5188132`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 11.2 MB (11166761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322fa986d6da7624363b347b0ecc23718b41b493d8ee8b8ff0ff9e1c158ce17e`  
		Last Modified: Tue, 02 Aug 2022 01:34:21 GMT  
		Size: 57.0 MB (57027041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
