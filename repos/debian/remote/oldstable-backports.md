## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:20071634841811949b9757ee0b5b219f6f5e474172ebf9816f2a2392bff37a08
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
$ docker pull debian@sha256:cbaed2f4310efdb9e99abdffbb7a97d9c86e313711e2051cb1f187600a831901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580440f3c90400791e2e0a21768922a55a57b3d1ef53fb4fa4c26c714b6dbbd0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:15:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a23a125887fa8fc09db60d0a81f3ed4f8ef675a752abc12ebdcd5cbd4be800a0`  
		Last Modified: Mon, 29 Dec 2025 22:29:11 GMT  
		Size: 48.5 MB (48480800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d87412bd4eb51535c89fbad5438bd16b4131db0968534001d015e4a555936c`  
		Last Modified: Mon, 29 Dec 2025 23:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e6a3dfb6252c4b65025ccdfb06132f7ba449058ce1565afdeee6ca9b3f56034b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2368bef4e17a2344d647eb48d1c5f6b703d52d1c9d57e43059d61a27a545b1`

```dockerfile
```

-	Layers:
	-	`sha256:b00c051e1e0efba1e7bcd0c25decfc82845520655a10f9a8fb14a1220d1df7b7`  
		Last Modified: Tue, 30 Dec 2025 04:26:08 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53af985f9899f703810320bf4341d62a1f0a7bf04b2728cebecb0212a0f8bddf`  
		Last Modified: Tue, 30 Dec 2025 04:26:09 GMT  
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
$ docker pull debian@sha256:6439254339a6cf64223d42d432fb13869cb36184343ded317254ed1e24f7d075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e237f88ab4e607f033f54a6a4e086b7b83f8283f214f244bd17bd2d5e8c846d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7f94fc1b37afab4212698c0ae4319d802e05c6bc955e2352f583338c30db3cb7`  
		Last Modified: Mon, 29 Dec 2025 22:27:12 GMT  
		Size: 44.2 MB (44196135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76f7a3c349286e033f8d54716e99c0aeb5ba5e355b6bdf14b1314835e57302d`  
		Last Modified: Mon, 29 Dec 2025 23:14:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e3d761ecd37ba8fe96b10447f69f61bca7cbeac70392af1cecad8e9de48f5401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4761d003ddf5ff474d39e425a60a6832a4b45e33bec8581aafbdf6c3b098482e`

```dockerfile
```

-	Layers:
	-	`sha256:80ab26183f9989aafcdca7af157176b211459ff3df4885c9dc97e07edb189f21`  
		Last Modified: Tue, 30 Dec 2025 04:26:16 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b32ecbaf275caa46afad407270adaef3f03bbb10582a5be7ceed5f120e83344e`  
		Last Modified: Tue, 30 Dec 2025 04:26:17 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:02a7e708f13e76ff025f8144351160ea9492ff61122664c020f39a21f961f33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d335a983cffb96cc724ec6954f8620c95bc2e3b21fc4a8f4648fb38c312e9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d2458cede02c11076acec2916205cb8c034826c99916fd157cb713ed297157cb`  
		Last Modified: Mon, 29 Dec 2025 22:28:49 GMT  
		Size: 48.4 MB (48359151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb3b5640414489c4e7d8da05a0a36236729ae7ef5a6692b33a3f70e18b6b327`  
		Last Modified: Mon, 29 Dec 2025 23:15:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:83b0b99a8df8432a7df3e52a591b0c6fb88473501e7b31962da01a5c2b64ada8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f904a2dea48b45704decd700fd24b43ba46ebb8a63dc2f3fcca549b571038d2f`

```dockerfile
```

-	Layers:
	-	`sha256:07da0af59cce29f95715d390012623846dfdb48681d665c0d4c1b979483c03f0`  
		Last Modified: Tue, 30 Dec 2025 04:26:21 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aa8c0ef0422030ea48bec06180f3eef7ce40b354a6558ca4a7e36bdcf54df0`  
		Last Modified: Tue, 30 Dec 2025 04:26:22 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4929f5fdfca662ca27335198b92fc09d09a23f91a91f52b2719ff1ffc83677a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa84d8aabdf98933314e1f002226e1a18ecc760b30d479045591ff61d9956e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1766966400'
# Mon, 29 Dec 2025 23:14:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2453d8d1c6cbe99e4f7d3b6bda5ca9514b06bfed03f42c62ff138422ed059271`  
		Last Modified: Mon, 29 Dec 2025 22:26:01 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4493462de73c48caad4bee60ce2e422d1e0d69127753906bd08cfb51ff9f23ee`  
		Last Modified: Mon, 29 Dec 2025 23:15:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:51fcc9618f2d8cb284e5a5e0df7f0c9b440f2cbf8f5bb24d891c93c588d0a78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a6361e87b6857c287052828fa19a013a050ab679dba7375875c62fd5dd52f6`

```dockerfile
```

-	Layers:
	-	`sha256:a28adf76bafe10862ed9e4041df33db1bcdadaf106ad6cde8cb3f3bdcbcecf3a`  
		Last Modified: Tue, 30 Dec 2025 04:26:26 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e809b1bd68e279e1af0dee7e7488a94d32a437a5da0c1d443991406eabd38e9`  
		Last Modified: Tue, 30 Dec 2025 04:26:26 GMT  
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
$ docker pull debian@sha256:34c6ddb546700677b8691f85d32fed0dbf0cfad22210fd04fd43699b50187c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a86f171db85298081eb6300e3c17e7c537ed861f122fc81e71efb0db64e31a0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1766966400'
# Tue, 30 Dec 2025 01:29:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:98c7e8398662a32d03fd3b26c204c10e60b81715342f9b05d4aae2209d2b4e99`  
		Last Modified: Mon, 29 Dec 2025 22:26:24 GMT  
		Size: 52.3 MB (52327007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80be1799a2b23de6a2664f77ede31cd8ae0ff926fecf3da8d6897acdbd573e3b`  
		Last Modified: Tue, 30 Dec 2025 01:30:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2e2762cb3348a005c98c8ede92b654d1e00ed99019208fd5788c64ee1020b5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d10b22c5db65fda403e499af506eed99c6fe3f10439cf55d2d315de54dfd090`

```dockerfile
```

-	Layers:
	-	`sha256:6a8f6abfb20c8df66a66924b6ea4f6ba3f321e0014626cff1cd4acb70cd6d833`  
		Last Modified: Tue, 30 Dec 2025 04:26:32 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6884c0182c89748ee33f2186a88df62cb4d0f11fd6ab5486afc8e2d5f9099c5b`  
		Last Modified: Tue, 30 Dec 2025 04:26:32 GMT  
		Size: 5.8 KB (5835 bytes)  
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
