## `debian:experimental`

```console
$ docker pull debian@sha256:fb7a1c0ab566abbff88efc821bafbc1d51744b7d405d8a9f776539a1df16e0df
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:51cc6fb4570d174e48b4d032b74e51916a5fbe50b34baa4efa57fcf1f4c4d32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47450809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5573f0ad7ce45550d954f71701d84a793c758efba5c41c2553bb82a55f2222`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8869c7957b9ea34225c35bfb9e98a6ac6d36f895cd5118e1f0cd013f347ae169`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 47.5 MB (47450588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bc1a22912249e2f91515260362b12cb8a71f30809ca8b4f14e8a7d21b48df5`  
		Last Modified: Tue, 25 Feb 2025 02:11:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d99e318aa6fbeea00717608d40eeb9e4914e688350ac1b289e24011fea5d1095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908c470bdc27635645cb4a7553f9641cea685ad174e240554604de6f8689698a`

```dockerfile
```

-	Layers:
	-	`sha256:b9da1743fcd456cf23f7917fdc26e7a2e959dc1010490b5fa26d31132a00441a`  
		Last Modified: Tue, 25 Feb 2025 02:11:59 GMT  
		Size: 3.0 MB (3049866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059d7f3d760681400dfe82d286d495508d1e1008784116ec04e013ccad00d93e`  
		Last Modified: Tue, 25 Feb 2025 02:11:58 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:207a3f3c3ce75a69854858260fbeaf3928612f5a8129a6f58ea35a5651c16e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45692178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2777eacef718816188213462a5389a29dbb7fb52e3ecb46fa2c5170e80750928`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a7fa539b509e103b4de3469d6d71af5bddfe8f86f9c82bbc54d781559802d89c`  
		Last Modified: Tue, 25 Feb 2025 01:33:59 GMT  
		Size: 45.7 MB (45691959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4f16e434ef368138110969284259625a3b37873868ead89e00c64ca716f0fc`  
		Last Modified: Tue, 25 Feb 2025 02:21:07 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:dae248eee536e79ebd6baa12d45eb74c2c31d9cd44be3913d64f20ec1b3ebf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f60dfdf3064f46aa63d839741fccd66200d1e1ade339820b5cba16ad3cd07`

```dockerfile
```

-	Layers:
	-	`sha256:dbb17de6808f5ab4cf800b6a88332aef0a7237a7daae5165c37b442e06f28c59`  
		Last Modified: Tue, 25 Feb 2025 02:21:08 GMT  
		Size: 3.1 MB (3058089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c55b3be26f49a46ab04f6bac7684a982b22d441f7086de4f89bf3712cae0bb`  
		Last Modified: Tue, 25 Feb 2025 02:21:07 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:0c376382b0c4217e8f582df2f575890e8c88ae19c4628a4c2b7dd0618b3a2eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43880526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f3e5e0f5c5cc75c267b37b85e24f7eeb85f74959783050e06f6f0d21c05da3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1bb46084c9f8710f46fcd288d4e322b7e082710b149bba1f630346c4c281b28f`  
		Last Modified: Tue, 25 Feb 2025 01:34:34 GMT  
		Size: 43.9 MB (43880305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7611d45575f6a665cda3905195e73d9a4328d201e939bc35b87484fb8ad5aa0`  
		Last Modified: Tue, 25 Feb 2025 02:17:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:e646bfa7f6637793d03f63a24d0acaa19e97e9bb515acdcf665c889ea7cbdfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4bb37c46377da10eae786fa2c618923c6788abece7ca00a2d515dca0aeae95`

```dockerfile
```

-	Layers:
	-	`sha256:dc3eadc3fde52a61154f21261ef2cc9f5e99b272cd92282e5dc32541319624f6`  
		Last Modified: Tue, 25 Feb 2025 02:17:01 GMT  
		Size: 3.1 MB (3050599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d05ace3f8cc7d5a63903594bcc2190a6435623c85fc7e9aaa897b6311325b2`  
		Last Modified: Tue, 25 Feb 2025 02:17:01 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:07a21873b5325fefd13b0c45b5cfd24eb5239258d3d446fd01f096cc6097cf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47842823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc4fba37723a3bbd12a6a6730033dbb394e7a48cdbc1ac9c29d5c74cfcb9f49`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:15f21ccbe181e4e794f49ca6b756c9a60018a3c9ac4821407b13989f07ebcabd`  
		Last Modified: Tue, 25 Feb 2025 01:34:18 GMT  
		Size: 47.8 MB (47842602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d00d1ff78a2327ce04b9e7b8c4bbcf5345642b1810ade4c8db105cdef1aa84b`  
		Last Modified: Tue, 25 Feb 2025 02:17:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:f28b13480cf4a1fe599eced5855f39871dd7a6da347ecefe18df315a7403859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1923a973c6207b6bdca27525d554e9309cbd5b5516bc197b619c00ed9ee35e`

```dockerfile
```

-	Layers:
	-	`sha256:44070cf76f386f50be54e94376a234f5c6ceca176249569eab15daeccc74e964`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.1 MB (3051357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6b8ed1f79a4e29414b644f037e7e1ea7ce371f9fa91d6fd23b4a622e5ebefd`  
		Last Modified: Tue, 25 Feb 2025 02:17:46 GMT  
		Size: 6.2 KB (6223 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:dd20763a1e5dd49f4a887c3f2bc2760fc7a6f1db5d68bda81aad60a7240a2994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48863381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80404ffac0105fe7b45c6d692dd55b35c4c42fe7c1621816c204576344194f8c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8a8eda04047bfbdd4652b1137ca527913a5aba61c68507b0a21280646646d380`  
		Last Modified: Mon, 17 Mar 2025 22:17:55 GMT  
		Size: 48.9 MB (48863162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee42be05a6614d4c296bc80a12b07f2c9e39cd77d6d65f00022e249a2dcd6274`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:37636542ae6ed26235f30392a7d312dd7acadf8d0223711cd5196ed6990486d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6421637002c3c4af86d8fadd91bd2c0e2fc81fba65bc03d86876f5619a415e7`

```dockerfile
```

-	Layers:
	-	`sha256:0ac6be62ab1e09110e169335b6d248d5593897f455aa517e1715c6575435d179`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 3.0 MB (3047254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37eef453684567f501bad82c9130e2bd2f135118b800a044684a89a9693cc282`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:05f2df145a749ecbe85c81d28e122c411b14fa9471a260714f32125b7ce0fa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082d8bd063a002066c16ed10fcbfc60e276d916b7ab6428799b43b2343a823f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f5c22e99fa395921458e65707e9eb215c9a58e04db7307805c3dc2a0e81bba2f`  
		Last Modified: Tue, 25 Feb 2025 01:33:58 GMT  
		Size: 47.7 MB (47672875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe3682babb42232cb106719dd7d03f0ffb132a1d256514c87b22174a9f462b4`  
		Last Modified: Tue, 25 Feb 2025 02:17:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:c7166e4b750c5a151ed9815eed841c7206602375a972b8339a288746997d816f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1649d259076754dab7189516fcbfb1544401cac74bba944fda9145fc1b09670e`

```dockerfile
```

-	Layers:
	-	`sha256:ef155badadd57552d714bff018929039f084edf12b12351725fa1f8c139579ae`  
		Last Modified: Tue, 25 Feb 2025 02:17:25 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d238f42f1c71aae7910cba39b190c61f45538044a20de69fc3a5db59748ad256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51110179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62ac5f7e48d91de4ac0d02a365f0317e0f45caa247b32d85e3a37441eda0032`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d009ef4d968e864e983ca4d20e5ee2d5da49f037225c876996dc2a8aa0fbdbf2`  
		Last Modified: Tue, 25 Feb 2025 01:35:02 GMT  
		Size: 51.1 MB (51109959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ace5bb1c6a82baa105b92f24f8996958a237483d9bcd60f051816636620305`  
		Last Modified: Tue, 25 Feb 2025 02:16:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:be0618bcb14481de98889d65a40f5205e34b3e61bf026e89d0a0127de9690923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3065030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670c7c6e8bd2252a2033ce4acba8cb5aae1bd27a0f413d1b9a00ac91a1be8417`

```dockerfile
```

-	Layers:
	-	`sha256:6485ab817329b210ac354cd72774770bbe504838d5c61ba7287a6d5a6ef8c29d`  
		Last Modified: Tue, 25 Feb 2025 02:16:41 GMT  
		Size: 3.1 MB (3058855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac39719ae87ec21e036d5ca9b45e86322740ff4865002184976a635d181a49a`  
		Last Modified: Tue, 25 Feb 2025 02:16:40 GMT  
		Size: 6.2 KB (6175 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:8d0cb0148f815411e68914e25bcf67710ca50688676c8859c9f891dc0e56c83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46065646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b500f6bbfc91a2225856e457f264d3512cf50f9a76858515b896b6f4f005096`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fd1df93facf99bea18e885b88274ce89ce70c9d47da287851c48c0ca674f271f`  
		Last Modified: Mon, 17 Mar 2025 22:43:00 GMT  
		Size: 46.1 MB (46065428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce198f8841bb89c17692e87cb9eee495f831e3aa2a2f9b0f825f74bf8bd84330`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:69bc9b0008b9e75b2e3e1c06de177250b1897d8807f08369eadd2c2b3a2d88d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256c9855699399d1199003b296583af0447abd398482c738995ca376a0ab0a10`

```dockerfile
```

-	Layers:
	-	`sha256:3cd073ecb6b5ff2df3e0f880cc93de86ee146dd7e18ca72a37395ec4826b1895`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 3.0 MB (3041961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10441b60865782521214ae68df0ede1290760d125e5f004d3ec2207fa3ddae40`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:27fa1ea3d7764dedcade938c6ae7deaea88108cc402ad1e4c53cc6e5c2b4ab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47498764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ec788def23156396e296541940607f8bc91fb34ffdac37d717cc591ee35f04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0975d0131135cb09c2d7dce89e32e677ea70ec6f1d4988ae94292bec2a691954`  
		Last Modified: Tue, 25 Feb 2025 01:35:51 GMT  
		Size: 47.5 MB (47498546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b4c65cb7b6468663990e064ccf2ea0dda37213d59d474e2f5c849a06fdadd3`  
		Last Modified: Tue, 25 Feb 2025 02:15:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:21c992b7b1225a466317ce729fe164c756d20ca61c641beead36be57d4b3f63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3063023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716edb3b5b4f3caaf944cc1e5b41b7d52848269fa26307b38554962b45a9528d`

```dockerfile
```

-	Layers:
	-	`sha256:ebb7301903cfe414a7103386384c72498b7465faaf4c3faa9916fae46a8a5a11`  
		Last Modified: Tue, 25 Feb 2025 02:15:34 GMT  
		Size: 3.1 MB (3056879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f45e8e9e863fa3fe2c00e29a62c4a90b31a5d2e2964d39cbb62bcb784ccf866`  
		Last Modified: Tue, 25 Feb 2025 02:15:34 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
