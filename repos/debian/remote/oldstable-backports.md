## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:63e223d78de5e095bec37989d7643d6de8c65acdb03ec9d51c9155612c7888a9
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e4698312d21ae2f8ffb9c03b7746e501a9a26e319631b4b75fee55c81ca2d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55b349372c5d252761ac19d1996707cc5dd58bfe2f6bf24e0e11bfacb48671c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:31:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c6c1be10320722b0dd652479cb0372ba95b1cfb6c4c4fb7f7266dea791acc15b`  
		Last Modified: Mon, 08 Dec 2025 22:17:38 GMT  
		Size: 48.5 MB (48480744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e96d68fa8b2cf489820127d4785b7f4db46ac5c6e2830a419aa78ae5340144f`  
		Last Modified: Mon, 08 Dec 2025 22:31:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e08b1a2c5abba8339fd386e8fc2a233fa36d3c9ed3de783d9543d21125a98e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63565324370e579f294c006ba15fcbab7334e76b7af7cd50ab47fa1b61acf4cf`

```dockerfile
```

-	Layers:
	-	`sha256:3180ea7120f7f9827ec24e762cc942eaf40c366d53b7690b077b0bcf3b17d518`  
		Last Modified: Tue, 09 Dec 2025 01:28:34 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e8e7a25bd2216110cfe1e1707781fe7fb0b0c63b39df877e55c465d2c112e8`  
		Last Modified: Tue, 09 Dec 2025 01:28:35 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ea729bcea81e27571c69a7d7c882c06494de777f2033e1a593e688634a31a6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa61303081af9f634d961ce2272da436c8382f81150c7b6e688f49c4b87f6eb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:29:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:70e4091df05bd888ca0e85d5c1b5eeafd971ba6178affbbc50a0ee30878cdded`  
		Last Modified: Mon, 08 Dec 2025 22:16:54 GMT  
		Size: 46.0 MB (46015806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aca66f657cba83f35d425b303ae87c5f21cb7088d24afa65845b2d900302958`  
		Last Modified: Mon, 08 Dec 2025 22:29:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:77241eefd2cc2b7a7573ddc10fea0b4990a87db39a1dbe8703bd3ddafaf22f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d75efb90a0a8a1ec2372e8431a14a6f2a28dc9c949ff7ae31d6fc097cd59aa`

```dockerfile
```

-	Layers:
	-	`sha256:3dac64235754bca9f1395286a6243157c202b8d42b83ff09650747a10c75e362`  
		Last Modified: Tue, 09 Dec 2025 01:28:52 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54be151f4db61bef7e746a1aa571e33b17022657f0812fae353d3dd45833de00`  
		Last Modified: Tue, 09 Dec 2025 01:28:53 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5e8f4e0eb2788d69aba418450460caa9c0b1ec6639f3925dd44fd8ffb88a2553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b356afc91a42af88e4209539820d918c411714848cc4741afdd47cc8368f5b08`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:32:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b407eaccaf84fff5e22c77a143990509de1c7ffc64faf79b2e058d850e1cd51e`  
		Last Modified: Mon, 08 Dec 2025 22:15:33 GMT  
		Size: 44.2 MB (44196069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1bb6cce5cf615d6b5df9b82cc07fa16c27f8a81cee825f466540538b88e9ce`  
		Last Modified: Mon, 08 Dec 2025 22:32:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a64c369f60153aacebcf925a77b3b92c35da428060d8d44aeacbc796477a7f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a632c1cf37598af84eb5bd35f110265be59a9d6ee4c1dcf0ade77beca31af1b`

```dockerfile
```

-	Layers:
	-	`sha256:356fbc9cb41e3ec4daad05e261e3aa91126b48f5e7462696c815268bd34100b5`  
		Last Modified: Tue, 09 Dec 2025 01:28:57 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df25bd1759154fa802053186b4cd67bdc9cb56fb1a28bea99cf27e3c8727b44`  
		Last Modified: Tue, 09 Dec 2025 01:28:58 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:abdebb9054962eb184279b3bc20104702e3d182b1c1acf939610bda51c272d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b1197ab37262a70762b87c8bc30401e03bb592f17539dc33c7c0111eafb47e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:32:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d7a74b86500342f4649d565bf70a3e3684cec40996b8d395fcfd9a61f1a14729`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 48.4 MB (48359074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622ef3abf17c44bb4c4cd3c419758e8e33c354967534046c529079d3b0ac3e7c`  
		Last Modified: Mon, 08 Dec 2025 22:32:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:19976b5287b133a850b2f3d4d0664d0b232226088fd96200604b6946e0e54f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c459b10c9cb11b1e48c621ef8e37ae89a1fd3094b1453ccfe3e56049f30b4da`

```dockerfile
```

-	Layers:
	-	`sha256:992052408b847c0ee7561f73d82acdfc5e13b18b51caef47d03c415ab4dcac3e`  
		Last Modified: Tue, 09 Dec 2025 01:29:06 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d866babaee787152328bacbf98ba6344dcbf561552d6b76b5e3e81f38750932`  
		Last Modified: Tue, 09 Dec 2025 01:29:07 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5ccee92b3880e2df3cc4a597da7ae9579addb354add9fb1d9729d827989d0dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3742af1f3764073e6ea3aa2be615c815b8728b0b2670b626a84284c557a73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:29:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ab8b89ec0f65405720f7179af92a80e2f293e832b91f7c8aad9fbc35e67628db`  
		Last Modified: Mon, 08 Dec 2025 22:16:32 GMT  
		Size: 49.5 MB (49466825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5a62e8343da6436c6ae952759a5dda46888aa6edda5bb3510c0ff488bef446`  
		Last Modified: Mon, 08 Dec 2025 22:29:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:753d2a545d92f0b8309ed962215e31c9c6972f4737a158e9e71c1ee5d1760e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb813f7a4ea9cf3fc14889dcffdac29d03fa7dfbb1b6fac8164704792c299ef7`

```dockerfile
```

-	Layers:
	-	`sha256:449d9e6cbaa7b6826476f44d966df53f0cca2510c3efcabaa486819a1be25474`  
		Last Modified: Tue, 09 Dec 2025 01:29:13 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcf0e7f08ff207e692905e259021893014c10ad21f73a20c090ccbfcc400e73`  
		Last Modified: Tue, 09 Dec 2025 01:29:14 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2ed0e68afd1f5b0895d56f314bac5818773a051d58586ec2f258f56ed47d28bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebd87f7117a6fc3c79ade56d4fbeebcf574ce3b1cc6af01132e127e64a5b029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:30:53 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f98aaf8ecc7a00885601d6b8a20464fed88114a07193f40845fe8927088d2809`  
		Last Modified: Mon, 08 Dec 2025 22:15:51 GMT  
		Size: 48.8 MB (48760901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b62bd384c2823b7cc20e42669cfa06aff611fd3bdc714618159bd7939038a4`  
		Last Modified: Mon, 08 Dec 2025 22:31:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5ced270b793fe28f2a8109a45045882d754f602eb8b789ddbda01cff991849cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598a9610c63fdf8d1b6405403bdac45dcc1e4b0ca1d17eec67f8457b74ec47fa`

```dockerfile
```

-	Layers:
	-	`sha256:00097528cf17f09a3f1175a26a545de109e6e48feb55b3b6ee143a436fc4c177`  
		Last Modified: Tue, 09 Dec 2025 01:29:18 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:531f319d772139cd7d064e23e70d70ac1d2779ba33d227d86f70a9f92845a5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4901afdac478151eb19d3df1296ab7ca96de6ce652cc58dfeaf50a0f1679f5f1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1765152000'
# Tue, 09 Dec 2025 12:41:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e798c4d2682a2511532edd3a84d9d403e8ba5c182f1753721fbfc2601b233d0e`  
		Last Modified: Tue, 09 Dec 2025 09:16:50 GMT  
		Size: 52.3 MB (52326979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad9fc2f3e5110203f59130793792ad9f4ef411fec69a3da47b6181519cb0548`  
		Last Modified: Tue, 09 Dec 2025 12:41:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4ef6676d764163dee68c116d670746c352f0fdde8db689c58052b145d8cf970e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9971a363f8d6cda2eed37674eb526672e44f59604ea44d66b215b7c620838276`

```dockerfile
```

-	Layers:
	-	`sha256:beaac164709e7ce2195fb3d4f8c78200cfa8eafae0442bed88c96c3bf77c2989`  
		Last Modified: Tue, 09 Dec 2025 13:24:30 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e5d576a41e3791b0667fa3cf7ed2d9bbce27222fdd372bdf706a18d6644243`  
		Last Modified: Tue, 09 Dec 2025 13:24:30 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cf3d35ecb230922694a27a71acc74d3cebb3a417972bc4551ce34911cbcf6f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d01df1c91220b6b68e759bf981e3788cb1f3e5f9ca8663623d05343a4dd108b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1765152000'
# Mon, 08 Dec 2025 22:28:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c10c600be448d911f221e44bc9c90c9921f87db419efd60a4fa9b0b8ff93f004`  
		Last Modified: Mon, 08 Dec 2025 22:20:18 GMT  
		Size: 47.1 MB (47137667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94884ffb06e831f2a1f73cc2099e3b44120349e5996aab6e47bd9385a25a8b3e`  
		Last Modified: Mon, 08 Dec 2025 22:29:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:27b0f9c4acca9f31b179f0266abd9b0b84d96f768a0fc02704cfd85fcc5ef12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b920094ac1c56540b86b7dba6e6fc0d5dd1f5de646717caa419dc58a17fc88b`

```dockerfile
```

-	Layers:
	-	`sha256:86bbaaa9b5afbd8267e77722aa0333f0da4d6e40be53bdbe4d197c760c86d6f6`  
		Last Modified: Tue, 09 Dec 2025 01:29:26 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0011ee972075a438a048e45b3c52d9bb73ea42178d9ab1b119ecac92b214cb12`  
		Last Modified: Tue, 09 Dec 2025 01:29:27 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
