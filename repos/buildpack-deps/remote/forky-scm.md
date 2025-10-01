## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:b915bc4e1ae762b46b7a68696469601fefe9a8d03b4ae1d4e55808433c58fb5f
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5559e1fcf0d35001220f3e78f057bbd57ef4e41a8f90600e976089869d4011fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144125566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97abb5f3b65d9b2ce114da86da43fdb5d485588944994b6edfd5478501de8229`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075219ece41f099ca8ada652efeda87c6ef755098af129d14764aea953222807`  
		Last Modified: Tue, 30 Sep 2025 03:17:10 GMT  
		Size: 25.9 MB (25851839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf321420777749b1953b35d223d4252c4f58791cfbd9906817af3697f147d98`  
		Last Modified: Tue, 30 Sep 2025 03:18:15 GMT  
		Size: 68.5 MB (68536909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00fc51c0d6ff86d6ecf1f76652e3988d124f1c85ed2b24ede14284965988d50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199bf70331e7cbddf559b646a3ff3222ac79df34ab2ee8d760ce6d184e11fc0e`

```dockerfile
```

-	Layers:
	-	`sha256:56a5c6ab97f6362b6d3598233d15118431e4a25d0ce29964b36ca4b2eca57090`  
		Last Modified: Tue, 30 Sep 2025 22:36:42 GMT  
		Size: 7.8 MB (7765483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f1c32a7345a77f1e0dc9e6297a2c4e2fa2a29166eb2d63a513abf909d06c9d`  
		Last Modified: Tue, 30 Sep 2025 22:36:43 GMT  
		Size: 7.3 KB (7308 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6965118dfeaba01a4b52100f206c8c72ad1513fe112a8e7b744a75be2f19572f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132820795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3e19f1a165fc0ac1bc607ebdd96e615c04abc4afc5a23cbb396ef7eb4cdbf0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86adee590a893d066c841440cd9d1bbc41753c40fc6a723dd85c4ca79b9b96`  
		Last Modified: Tue, 09 Sep 2025 03:20:59 GMT  
		Size: 23.7 MB (23664786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed6e10bf1b9316986fb492bbe0bac3e1cf59a04a08869527f7e66262ef8c0f1`  
		Last Modified: Tue, 09 Sep 2025 04:45:46 GMT  
		Size: 63.2 MB (63212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:416907b2cfff7c68d21d3f11eda3470eaac4f79e9901a5296fb1b3b8af1a223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb78783840cef248b119d9309081bc9f8380662ec394ca8f11cc13ac0b22818`

```dockerfile
```

-	Layers:
	-	`sha256:e33ffe92671e3b1f45903e45bdb25193f014356947df25072d6780d13b54c0ec`  
		Last Modified: Tue, 09 Sep 2025 04:20:42 GMT  
		Size: 7.8 MB (7771507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530085440479fdcdec639575d25f151c342492c06e9092f0964d60cefbae733e`  
		Last Modified: Tue, 09 Sep 2025 04:20:43 GMT  
		Size: 7.4 KB (7372 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98f3971a030ec04c585db789c9bf941fed13ebce02cbf669ba34489d194048d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9a0082a2951e85a77c3b2310b9d8e4e09f3df22b7ae7c058d3365d4bf4fd9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009e42d3323422f2397c63e68313d31e460dfa892d093803cd931e5199733e2`  
		Last Modified: Tue, 30 Sep 2025 01:18:56 GMT  
		Size: 25.2 MB (25209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde70c2343e98e974396577ed833e905203bb8d9de40b076f03dd816afd1872c`  
		Last Modified: Tue, 30 Sep 2025 02:14:07 GMT  
		Size: 68.2 MB (68179749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fe3f109daf1ead65a8b459a6bdbff6b26ad31fd8a432d3c01a8da3ccab35033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7780535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acf1af5bf3a0d26c11ec627b2447632eec07253b791ec381bb363b12f792bcb`

```dockerfile
```

-	Layers:
	-	`sha256:60d45375e2b61eafc76853974f61035bbad5069680e3b7dc268bd743962dd182`  
		Last Modified: Tue, 30 Sep 2025 13:23:52 GMT  
		Size: 7.8 MB (7773146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d88811b43f5ba231168a051b377003176fc625683544c4fbcb51686a4d116e9`  
		Last Modified: Tue, 30 Sep 2025 13:23:53 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f32e40c74fbf0446547ec526bf84d331471c26b47e7ab9395e6cc3900e121bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148442778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668d2da733cf9e804a9a34df229e07096ddd3672e0ab36df1a0da11e837edb58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf114b881a561e278525714169b788115fe512463f3cf36ea76912c59a87cb`  
		Last Modified: Tue, 30 Sep 2025 01:18:44 GMT  
		Size: 26.9 MB (26896436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ce394ea3b0f58521d466c625f21c99b1a0c4601ea3a202665effb24b708c5`  
		Last Modified: Tue, 30 Sep 2025 01:19:29 GMT  
		Size: 70.4 MB (70426922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65d86a107fa5c722f95631794417505e7666ddc103444cc317f77095adf8aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cefb9ae6ee7b5b0d02d2298fb7557e7da959f777fafb5d5a1658310a7355467`

```dockerfile
```

-	Layers:
	-	`sha256:149ff5729ce956245c002f762ca286a30d5e219be9371914d5699fbd67d6e428`  
		Last Modified: Tue, 30 Sep 2025 16:36:59 GMT  
		Size: 7.8 MB (7761633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2378e7fa288955fd7432da39cfb36ed7a1b1480a02fe8de0b4a2760b7db1af`  
		Last Modified: Tue, 30 Sep 2025 16:37:00 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71fa8638405f8f8417c45baca4fc9282959137530128eb747a65f058dfe8dc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154042382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acda6ab9f8de7e30a49e5ca828b185cc5b86351cb37d01b8e19b90c434dfb579`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4e4a2bdd2295cd2a4f3315805533676c7f12dc54b360ff3c285c5614051d45d`  
		Last Modified: Tue, 09 Sep 2025 02:16:14 GMT  
		Size: 53.4 MB (53391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a918fedc73bd98652f37087b2219a9384ea0986c8affd0a0d0679091c621a`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 27.1 MB (27054637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a37b1c09db430f1439f2b1593baf02b266038e8525ca1684329d8133359a2a`  
		Last Modified: Tue, 09 Sep 2025 15:26:09 GMT  
		Size: 73.6 MB (73596047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6bde21fb3e5fd84bfaa0fe0a55b16609a869f7d845c5523356fce0f2233d53d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7785452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e34773966e9e0efd7c16da77836b1d16296ca40d0f75abbd7946e5b762d5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0097ea21be8310102794089081d6fd228f902d2aadedd55fe64c1fce55495c78`  
		Last Modified: Tue, 09 Sep 2025 16:20:14 GMT  
		Size: 7.8 MB (7778111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24f5d69da6ed5b7b38812e7fca910407aa2a43241130aef573b9f00083178cd8`  
		Last Modified: Tue, 09 Sep 2025 16:20:15 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0b72e05a9043fd421f15cf9d3e8c071b660f4773f8c4f0f2ae0417c408896b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140208407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66a78dd77b25c8e629306a3563c4ca5c5ec79be95bda89aeab9fbe00e3ad56e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b69968429eb7c4ddc55330629f921afc4125b1edb6cd3eb02edfe67c09cb248f`  
		Last Modified: Mon, 08 Sep 2025 22:03:44 GMT  
		Size: 48.0 MB (47990884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afcfb97f0f574c8205b47fdf227a9c9ba730a3a1ce377de450a5ca2828ba055`  
		Last Modified: Fri, 12 Sep 2025 01:39:01 GMT  
		Size: 25.0 MB (25025845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e67756886f1c8cf9722970b775438594a7ea05fd03804456510ee3f3eb18e`  
		Last Modified: Thu, 11 Sep 2025 01:32:48 GMT  
		Size: 67.2 MB (67191678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efecdf94fe06ef12f6fc3ff9712f830199ac6a430f699eaa95e334e5708ab1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b328633fef76d9152372419e96366c021f46a3eef9ed7460f53296b68f86d502`

```dockerfile
```

-	Layers:
	-	`sha256:03b0f41c990cc19f91484ca43e30070ca21538c0e9fe7af6109ba8e0dcc375e1`  
		Last Modified: Thu, 11 Sep 2025 04:20:18 GMT  
		Size: 7.8 MB (7760814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209324594531a1351b94b815b2d92b371bbda42843f2d639f46b5c3b0d9d1f90`  
		Last Modified: Thu, 11 Sep 2025 04:20:18 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:45d155178d15af214067fea0cc7406a9212f55d837efeaccbeb7b76b2e78ebdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145569336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d90f73552e909c1f081980d3fd1fdb43d352039f6f648af927def9e2e14267`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d70c4639b1bb56ca2bfa88a8dedfb6d14d5f6a857613b672fef601229bcd766f`  
		Last Modified: Tue, 09 Sep 2025 10:20:05 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23441d4a53386d92d68dfd117aef1e221cdf7c5c29e7c8841eb200ce14f89465`  
		Last Modified: Tue, 09 Sep 2025 10:20:02 GMT  
		Size: 26.8 MB (26840296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aced33c6860e9f1fad4c8609ff123d675ddb56caf85a90370df68696f49dccdd`  
		Last Modified: Tue, 09 Sep 2025 11:45:43 GMT  
		Size: 69.1 MB (69145858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1927b6886baaa12d583c07bd3957b00d933c2a9d246f4c1d1e3a90836d6485d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9986f730a2ad22e08708fef6cbce2cbb7d3396893a9eaf9228340d08b65ff47`

```dockerfile
```

-	Layers:
	-	`sha256:0364b402dbe367d69623cf41e55bd900e4a84806ab76e0a42bfd38292c63612c`  
		Last Modified: Tue, 09 Sep 2025 13:20:15 GMT  
		Size: 7.8 MB (7771921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806df7b1cdbaeb23ac062593b7e336e924c4d42083c92db8eeabb9f97611074c`  
		Last Modified: Tue, 09 Sep 2025 13:20:16 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
