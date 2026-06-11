## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:2cb1ffd28c57d74722fe49bd9bae0348676e55ec4f3a33243c7fc62e298635ea
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:82b3889f2c7637b2128a54f69d2c3c04296ff392df13e806de9bf1d63ba47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48502265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6667ce939c340bf3cf905bc5939db81d832bb14c5610e358b8fcd7473b30f5ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a686970712580ac4d61e3a65f2e455cafb3d11645fbe6bc3acc924256f63b`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:df96ea7a17e4af5bc70c03880f96bde15ac076145c7cadabe7f0f3b85a8d512f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770e1531038f9f428f3b0aeb1b03fbfdd68914fac8791e76ebf959f4040c653`

```dockerfile
```

-	Layers:
	-	`sha256:056475c1bb51069f740942d21960ad83cf9276d93c55d4ffc3b58c5e75fc91d1`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 3.7 MB (3734110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9302099b7d2d5607a0865d6feb15f5d44643d70e8ccede4fb2dc384994beaf`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4263903d8cce16ea939d5a5e8e8999026e4c003ba06ea42770f241b934b19718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46038412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8fce92982526fca7861d67b429c8edf0ca2ea3ec7dc30b83836055b5cc168`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3683b8a7792857dc507c3398919097537c8d564a235824e722ff16657599fe21`  
		Last Modified: Wed, 10 Jun 2026 23:38:13 GMT  
		Size: 46.0 MB (46038189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad149888a7977abb391f51604be4b50e777e17fd02e68fe477b2a423b53e101c`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02627ddeae12c6f260b560a8efb1c1191643e2537820539b5ab84c356d945c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553e3730adf1e51ede71d205f2eb6d4bb840f707c8c7369d83ded1dc52a4ed3c`

```dockerfile
```

-	Layers:
	-	`sha256:82b1d3060fa3e215808cb9c3613b0a0d0461e1fdc35c272174cc30c4c9270813`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 3.7 MB (3734311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffba6aa195fc9c1e7f0a4a3df992338cb79dfc3cccd78c0cbbae409e902b61a9`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:76c3a4cdb5a49d966a59a7e255cd94c33a8ff7d0a9689e73b8b89e482263d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cf0e4d5856f747cbf58cc6f7989141afb00a0f62452543baa4ed0cd9f0e58`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd062a844a2aa95c7f7fd9f55cad2cc75f32547e5923b093a7ea04b6e7583b`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9eca6621c47b22798a51d7424ce707053a60134dc26f8dba287ba7fe783dd680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48fc2ead00a91178698f6a4ce2fd8952ae37ae1ec075f690b7858b20490f4f`

```dockerfile
```

-	Layers:
	-	`sha256:e1286610e5fb02d7563e7f2050f2c1732ab7d438e91cf7541814ad5536b0e93e`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 3.7 MB (3736289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a19786919cc815fc76b6a0b4df4082ef86d2783ea45503f458391d749149d2`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ac8012b067e7d4349e0f9336f5727488448c674e9b5ffaff5a4b2fb9b4f1401c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22fee9dab22a294d0ddef2b1f9b7c0a3db64cf2cf03faedf3bada42e877558c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc5f2e18f1c90fce9b0f2b04c5dbf8842fc1a9a270534f703c4e0f6e3eb3bbe`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:88dd73a3df40e4d018cad35a190e9a5e3c424cdfd5fc2583bf5f41d3c84a3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4558fcce5c6f5a7bbed856ecba4129c841cd8edd1a21ac2bb8276ea46c17bd56`

```dockerfile
```

-	Layers:
	-	`sha256:0c1f9297424a73e669cebd30bcb253c330d45292fc8d80d13094d945c3483200`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 3.7 MB (3734325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532a02f8d57625f967976a3dd3011175266878bac2298cccdd32b17285bee72f`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:03e49d6004ec99d894c4a1734e71fa1df6101fa8cd6d15d396892ccd6e8cef92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49491429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d75ca6b0d86826e5eb7f7a23d719b14eec01505ae814a05a4f5e91ee21a6284`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942f9a8189c30c46d07a8eb10f47f227b0f30f35d1f9b5748baa050bc83aea37`  
		Last Modified: Thu, 11 Jun 2026 00:15:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7de31cfaf3d4d58ed90f8509d660352ef0ceb4e31584abef762689040f0bd75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a8a3f43e3b9fee9bee7d918850353c6103302b523c87d0144faec75687972b`

```dockerfile
```

-	Layers:
	-	`sha256:52fffa91698723e62848d200053bfbedd28008041764be00b6ba69b6ccadcf3b`  
		Last Modified: Thu, 11 Jun 2026 00:15:21 GMT  
		Size: 3.7 MB (3731306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8898af2b5b0aeded2b2d540b336ad34a081cdc01c58d8de32418c0e921de3e91`  
		Last Modified: Thu, 11 Jun 2026 00:15:21 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:507ccdcb8c40c056a0a35f102ab8d2747ac09d5adc97d5ea2077c44a16356821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48792934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebdd1b93d9e89fd9dcb1ce95863fc191384b6c37a35467918a82f4c6f1b5c49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b0faa1d5e2e28eaccdc6eb999f69ab8358183a85912b3dee27c1996b9daab`  
		Last Modified: Thu, 11 Jun 2026 00:15:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8a7533a96e7b745ad521559f7de2b749acf6734bfa930d8aec068ccda86b3f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84553d888d8f09d4d0fcd0f73e4897112767e66469bf247196b1678fb81093be`

```dockerfile
```

-	Layers:
	-	`sha256:5d33073099d17ed400b8de92b4370b2b5c761bb3c2bd57073bc4ca8aaadf8278`  
		Last Modified: Thu, 11 Jun 2026 00:15:17 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3919f22f02a732d94915823610a6ffbc306cbcc10b6e04424b86cbcf86fdcf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52340425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b72c19c2e3a5704bbfe9db13f7c7a990fa74c2e55a237b2e989cbbc818971e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:55:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e6a83ae481c028f8d592cf991e230e52f5b5bbd822c515f090f975e19d3161`  
		Last Modified: Tue, 19 May 2026 22:55:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:31b92c65dddee42ea61dec324df1f0113786c2982c43f198b3318d8dc61482e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704215ef4da14b1145340a570ae8ea12ce3b836b6d83cf445d4e106663bf8abe`

```dockerfile
```

-	Layers:
	-	`sha256:17cb67cee7e846f731384cbbf8e8c44cb3ed31884de354b2636c938e9bd05e16`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 3.7 MB (3738450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2b312dc2a4ee8be4b6f8c7b94d331c6478acceee82e664eb3a8d1dbd3086fd`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:7b462bb5b8c991015009486252f97fabbbb4a59b1daa85dcd3409e08b1920e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc12ae3e05787a38f259fa81c75f54bed4ed38a7bd501c7d915555fdd88de71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d3d3a71f7004d09a8d4eb3adb6ede6d8b84af295b1926e505f0d7ee668b228`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8b0db300109fb5ac6daa21cccc2dbb3b5fbc779fac9f86d30a545a693710890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09056e3569f7f196ff536fa5a2ea6467e021e366044e0d054330a0c0f4a19e7c`

```dockerfile
```

-	Layers:
	-	`sha256:dd78f0fb2bff561ed920b66c1d2a2ecf98d0229b04a8fb7e79ed004686be11fe`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 3.7 MB (3730948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373b50ebcbe9d06fbcfed37b21199f79563b10825a592e9a53ada9df202a21c8`  
		Last Modified: Thu, 11 Jun 2026 00:14:56 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json
