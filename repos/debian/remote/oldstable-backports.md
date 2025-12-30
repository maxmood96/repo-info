## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:fd4709e9400b86afe787070462e569e314f7992fd31774c236aa68b324001d73
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
$ docker pull debian@sha256:88739a4d8de860cbe0e49eb067b9aa4851393456f5d6e41af01869d5b44565c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c625920ae691de07ec1b35d0b3258b21f3a34f69821844043f082d8d92f55ac3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0b9b5a63d25022f65fa71e2b2ed2f9c3589e3bce96843415521a0b64085da784`  
		Last Modified: Mon, 29 Dec 2025 22:26:08 GMT  
		Size: 46.0 MB (46015876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c73ab8bbe2ef1b8a9aaa04a501742e05798008e44846c9ce3b8ba984599cb1`  
		Last Modified: Mon, 29 Dec 2025 23:14:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fb24cd96d8ad605b247f31a68efd4acaed31b246445409e8bd979a694f300601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f81b7596352056eceec68a38c4bd5c66ebfdbb9151d048ec653c553942f7d6`

```dockerfile
```

-	Layers:
	-	`sha256:773eb3f0a2162f1c7c2fbdb3eb338d1a518b504821c771ce4e16f5b83ca942a9`  
		Last Modified: Tue, 30 Dec 2025 01:28:34 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e7d57c305923792bf7ef1c942b10e48d3e5ba9e91683a0cebbe6ba4ac67eef`  
		Last Modified: Tue, 30 Dec 2025 01:28:35 GMT  
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
$ docker pull debian@sha256:ecc7c589679c99f353f8b5b4d7f0043a604ce8dd3b7ecba05ed55a25b6a7b8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b4ee8490debd62666c218e7feffd0663e8fdb5e35003eec38dcc40620d43e2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0cfcc53f3a0b6d486d719b47919432b20947d4257f119a5dd5e82507c7d80e0e`  
		Last Modified: Mon, 29 Dec 2025 22:39:15 GMT  
		Size: 48.8 MB (48760931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8616693ddd64c3a6046fc133832b18f231949ea166b6545c5231e6c5905c6`  
		Last Modified: Mon, 29 Dec 2025 23:16:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:41de53f383ddb7e6aeffc62071bf83e31cd654e9101201c14634ba8277331b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3500b3ab3b4eba0f0d17ccb7f8cf35c65dec00304d6980a4afda241ceb96b4`

```dockerfile
```

-	Layers:
	-	`sha256:6f2c5a63db1d72fdf232c7db49542f12409ec9964d956431e62cedc2ff36f06d`  
		Last Modified: Tue, 30 Dec 2025 01:28:49 GMT  
		Size: 5.6 KB (5633 bytes)  
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
$ docker pull debian@sha256:9e8a16c538c3ed9f110c85fd0d188fe2329b0d041c1d5ad3023a1c5575963173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2401514b8b073279a631d0f4b543f8a12ae94018cc41f75af8d1b48d34aef7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8abc9079b54b674a1c69ebcc2024246653bbfc62d6c28868383c291720eb23fb`  
		Last Modified: Mon, 29 Dec 2025 22:26:11 GMT  
		Size: 47.1 MB (47137731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970b10acf3ca351233fa806fd35072fe7190ac5d42c68a0e9a22a5087dd5e2b`  
		Last Modified: Mon, 29 Dec 2025 23:14:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9b97969db80d9a9967b01218620986317800feff93fdcd83d53f4dcf881d0835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0bf8ae2ff690f99bb07a8579e5b6acd3b3447b2e86fdc93865786ad662fbbe`

```dockerfile
```

-	Layers:
	-	`sha256:6efb1451cc57e7fb1b6831756888645195f3a723192810e24525ca2f42326fd4`  
		Last Modified: Tue, 30 Dec 2025 01:28:56 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890e59f759ad31aa70678438d2f3b2d04caa82ed33e6c364011a810a27926587`  
		Last Modified: Tue, 30 Dec 2025 01:28:57 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
