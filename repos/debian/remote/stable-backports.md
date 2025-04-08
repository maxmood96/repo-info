## `debian:stable-backports`

```console
$ docker pull debian@sha256:0dbfea37d701043095edaaa933afe1ecdede080ed62f3af636380aee7031c29b
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:768c08ccd6a4bada62bb7fab664773b15f88be1c61375b2663d6fb80d5f978d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48490768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ced7dc63dda021810f936e7c96f790b0d6cc55e7dc1a8e8e6f4825cb6190e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3bbf9ecf9546d553ca5e16fa0f737d1f296552025619d49f174447f830193620`  
		Last Modified: Tue, 08 Apr 2025 00:23:12 GMT  
		Size: 48.5 MB (48490546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b21de470131836fa8192579e2463a531c8509eb62b9acedc4cbf7ed06ca081`  
		Last Modified: Tue, 08 Apr 2025 01:11:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4969dbe3f659a4985655b79b2b7c18ea6a8d86cde09f70ac42a87b71439d09cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f87f37d3bda79652db60c761e5775ddfac91a1f666df60f299edd84cee965af`

```dockerfile
```

-	Layers:
	-	`sha256:d063c34cf98c71feec6a344727ab40f1588adf561851b7acac135f10d503c77c`  
		Last Modified: Tue, 08 Apr 2025 01:11:29 GMT  
		Size: 3.6 MB (3620568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175577432e2a47c70f1f7c16167443cfe5f0a3ca86e0cc7d21fc0895ecd9deb7`  
		Last Modified: Tue, 08 Apr 2025 01:11:29 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6e3ee666848d73ee121bba1f78bc180229916597158f0a7ec059096f9d7a52e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e364b4cfec36332563cf54021ae2c18ad517366288cb8ac7151acecbe65e69d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ab39667381605b78d4af1d10b1e65ec09916d612264ed8c9dfebae06c614c244`  
		Last Modified: Tue, 08 Apr 2025 00:24:07 GMT  
		Size: 46.0 MB (46026192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69375f6fa2071fda27b993176bfa6a54c2fba881dece84e4683890eda39ddced`  
		Last Modified: Tue, 08 Apr 2025 01:11:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6669c1cc796117f28c1ee8da3fc894b4b1a33ae9b213d874aaaf2080340feda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9d49eea1ba0ed69401c3993a488438bc9c7622b1ca562b78e579bae835de9e`

```dockerfile
```

-	Layers:
	-	`sha256:b62fa9994e6e789e7611b88c07984eefd26a1788988f65447b203eea3e39e588`  
		Last Modified: Tue, 08 Apr 2025 01:11:54 GMT  
		Size: 3.6 MB (3620769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f3edee53c9f635dc41af83375fcd2d4b276076a4f93176899f8ee268cb9f2b`  
		Last Modified: Tue, 08 Apr 2025 01:11:53 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2143cb49fb58d833d76dd1fbebe6cc45436e45dd93a8f10b94bc0f407a79ad2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa62c6b49340516a8d0f821ccb56a48741f7248a13c6df3133b53692c7ad10e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:661eca3ece6496e9b21d0edc6256f81e8515ecdda0d9900a8396eba3cba7b1da`  
		Last Modified: Tue, 08 Apr 2025 00:25:12 GMT  
		Size: 44.2 MB (44196773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d581bd0bd4584ba7a5a6928d50ea0f436244f71dc226a8ba7560aa3b387418d`  
		Last Modified: Tue, 08 Apr 2025 01:12:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:af28f527fe533109a1343e7924ef90e2faecee0f3c6ecabb273e5f7236f23ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecce4fc2cc48d3a91f0f8bbb766e184269566d78236eef599e7fe524f08ea073`

```dockerfile
```

-	Layers:
	-	`sha256:db9a68d89f93299720281fc839d68b60712cfa8429e86e651b1f0bd661f16988`  
		Last Modified: Tue, 08 Apr 2025 01:12:37 GMT  
		Size: 3.6 MB (3622747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b01c3a4511e5a41e5bd44a563a33d23c4bcc2f6e54518001fdd2cc4b212df2d`  
		Last Modified: Tue, 08 Apr 2025 01:12:36 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2436323ff4a509d7adbd259ce6dcca53fd71a5b634814cb1bde0c32c5b944507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fef9802819d2d6b783564143276554a9ba9257473eed6c701a83c7168922bfa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ade8a8aa6963eefc8877077abea366b25ea74090eb670960c883c5a2423d4021`  
		Last Modified: Tue, 08 Apr 2025 00:24:59 GMT  
		Size: 48.3 MB (48327471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8be9ff64b9494099b9dd82b74f438ef0fbd8ffd315f01d2c0dcb33e487f162`  
		Last Modified: Tue, 08 Apr 2025 01:12:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cf550e28fa7bc50d7c5ff5485bc7a8956c27c2a6b58eaa679fc13615bbb52af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feff2a5920c3bd418cafb29e374775c9a86abcb8af71cac0609506f492e2156`

```dockerfile
```

-	Layers:
	-	`sha256:440895eeba2f0156935368ac288752f045199e4781a3a047a091b796c9ccdc3c`  
		Last Modified: Tue, 08 Apr 2025 01:12:23 GMT  
		Size: 3.6 MB (3620783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6565b9d587e48a6487548d03bbf40b2dd71a7f1e99762d42a89eac78bf5baf6f`  
		Last Modified: Tue, 08 Apr 2025 01:12:23 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:0778d499c218688a0d74fdd726624e8f119d6a16ef4850755ae5fe12fcad0a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc312834bc26d70fd2223be994eca1c3810ca9561f732e80d49c3e3e214c346`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f08c089bd058db661cc0aaa7496f1f099819e0fdbfb5d7e7dd796340c4d215ef`  
		Last Modified: Tue, 08 Apr 2025 00:23:14 GMT  
		Size: 49.5 MB (49478136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e27555b4a62c06e3deaf2fb5d777f45c01492a5d4383ba41ee77d4bb3a3531a`  
		Last Modified: Tue, 08 Apr 2025 01:11:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ac128238a49808fc1311e94c42d7c8c90fd7d9240b022e2a8e7cd38a4b56797e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3522b38c8e9c16b3234c891754c647155f954418dd2e2f6a8bbecf601cdfcf5e`

```dockerfile
```

-	Layers:
	-	`sha256:14d71369e11b49c3fed0f8c187597d33d075a9cda6bb0200f5b97b473abf93af`  
		Last Modified: Tue, 08 Apr 2025 01:11:46 GMT  
		Size: 3.6 MB (3617729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08e19d9725206e7de060e4a785be65c00a65bcbe174329ca22c6a0e4adc51a9`  
		Last Modified: Tue, 08 Apr 2025 01:11:46 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0dba5a5f7bc44788f98028e4d62a55d62d7bf1982cb790b9d60234a68aeae508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2803c4bc49872bb2baf024d0544246f6fa47c15690ba9aafa14cf1b43d3fa293`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f49a95b0f27c85d3c9040ee9a8dca47971939c5d574ffc75af012d8c88819b4d`  
		Last Modified: Tue, 08 Apr 2025 00:24:33 GMT  
		Size: 48.8 MB (48774860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2c2c15d5da80abecc63e4883069ac85d78c6647cf44b7c7dca0471d1cd39e`  
		Last Modified: Tue, 08 Apr 2025 01:19:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9accf864ce5f5818207eb5a90615f9a9c82b0701721bde36b7e73622a28b1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44344be8a383b52813bb6620df9e1ea5feb516d812695e0ceff66fc0383d18fe`

```dockerfile
```

-	Layers:
	-	`sha256:16cc004e596161d7d192bfc2d6f9ec45e9b542ff2252b2bf28debd4b9d826fb0`  
		Last Modified: Tue, 08 Apr 2025 01:19:07 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9c0c4a37d841a3db97969153b0cea9292fccb46e638937424893dbcdd41aa29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cd1e37474f6dcc927cd4c1d926cd4274c1eb0d4dde1a83766e9c52b9cea07b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bdcffe401ef215ac9aab131253f058ffa492234c6c39016ab5641f7a13eab735`  
		Last Modified: Tue, 08 Apr 2025 00:25:27 GMT  
		Size: 52.3 MB (52331653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dd990ea22376363ee4235d3a5848fd06e20630fc06eb0f2de527ca215cb0e9`  
		Last Modified: Tue, 08 Apr 2025 01:13:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2a6b6c1bb99be2a368ce85ab159dee50fa1c865b064a8b70a8e7cef8af6e248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f018f4540d888dd592836199dbac80bf0eff0add6b3833d855b9690524c2a69`

```dockerfile
```

-	Layers:
	-	`sha256:0fa41077125ef390f58500284454ad3e0e8c9df2781c204d4faacb60ba53b7e1`  
		Last Modified: Tue, 08 Apr 2025 01:13:01 GMT  
		Size: 3.6 MB (3624828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7330cfbcac70c735e574872bd586d4fda7ea80a8c8bddb29a32bfd708bdbe125`  
		Last Modified: Tue, 08 Apr 2025 01:13:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:f422bae082092551f25c11e702b03281d01c48d4d282a95dd1542d881f8763f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47151216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2124da38c23c043a29bbdb0f0ac086f0c38bc0ac218b41e92c15bbee81433290`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1fd3367bc64b6597c7c0580928ebeeff322934db4ec2bf3f0554e57ac5f476c9`  
		Last Modified: Tue, 08 Apr 2025 00:25:29 GMT  
		Size: 47.2 MB (47150994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2a6a30ff9308a2e16cd205602645f918aa7fb9184857ad0303dc720238f0c`  
		Last Modified: Tue, 08 Apr 2025 01:11:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8eb31895a94e74bd9dee608fce754a34b9781e974d93cbcde1358e4f764d5827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942006f763e13eb4abc7dfe08909e82377b168fc9d292a6a8c509267a32f2e97`

```dockerfile
```

-	Layers:
	-	`sha256:3669310b4bf98772a4824e0f1d62f850494787541d66b39009dcd03a38e0b386`  
		Last Modified: Tue, 08 Apr 2025 01:12:00 GMT  
		Size: 3.6 MB (3620298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7db574632a4de7b28dfe29354f9813f24e11495326b68f9686cea9412284d`  
		Last Modified: Tue, 08 Apr 2025 01:12:00 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
