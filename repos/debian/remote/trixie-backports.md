## `debian:trixie-backports`

```console
$ docker pull debian@sha256:a153c98c0049a5448610b928deecfbff14868bccd78029da92886f539d22871e
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:7c2ffda2e2b8f702adf5eef67cef508d9c3b3add1171e4d64795a0376669acc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f877593a2d01157f72ed50c2d37a57ebb3208bf50cbcc898bed8e5a78cf6c05`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:32:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd8cf0b5992c65905b3eb6d4832249d3eb10d529bd6cdfbd3fc9d84f25a12b4`  
		Last Modified: Mon, 08 Dec 2025 22:32:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:776ad83910da10b0df84f805743fc46fbd255584ed2f8ca8df84136bc3a3494f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5194357e8d22215014fa515f921f35db157c687bedc6065b40b4fc97a21f5144`

```dockerfile
```

-	Layers:
	-	`sha256:a9c41373a1a0e346ea83fb3b3cedc47448d12224fa1558a55bb89e7033807147`  
		Last Modified: Tue, 09 Dec 2025 01:31:59 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a01052c3f475285a2d6c969604e304f4d5aa6c553db0128dd58b050c8bfd61`  
		Last Modified: Tue, 09 Dec 2025 01:32:00 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6c7a5b38a1eea83c2efeb1f61cdd893be6133b1df5d37aa2b6b784e39d9b1eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1e4ee1d9832b76539a68fd6fdab3e48f492295e66f14cb72f30e930bf15502`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:31:13 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9879ed5d67503cbe3c10a7ea367afda40b84b3d9f316d7c7cac2e97d288ef8a`  
		Last Modified: Mon, 08 Dec 2025 22:31:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fc96c9550bdf14f2d9e6220f93db5c677940ed3fb67d635c115602ae150d925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcde225623ded4a9d3a6c86e2e834081e9af5bb0c815a519d476b65a001e3b31`

```dockerfile
```

-	Layers:
	-	`sha256:68077569af3193e80cd8897d6b3a8a3a7492117bbb5cfe6689f6513eb3f15d45`  
		Last Modified: Tue, 09 Dec 2025 01:32:04 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24f940305e805ccdf23c7e49c9605eb70beece378756a0e780869cf8b04032a4`  
		Last Modified: Tue, 09 Dec 2025 01:32:05 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:dcf1337bca773687abef4c143fae7785e001cb581a744a6d51daf6b19bcdbf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884662fd2190f080478afa4d8a98e37677b74806b7f66b8c4dd691aba2e03f3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:31:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8303aacf994e14bc9a690e20de87ea2419bc095f6dcdb48f04e52167ccd58a`  
		Last Modified: Mon, 08 Dec 2025 22:32:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f27dd100442f60acb5a16f171946163f44fd65c8e91f44a94c7ccac250ff53e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a784f4138d538c882659c1e0b5b360a98977d8ca32ec0d618f0d64f9d963166`

```dockerfile
```

-	Layers:
	-	`sha256:6da833571c6623cb9c8cd100cc1227485692b828dcf98a2b6b123c8464773837`  
		Last Modified: Tue, 09 Dec 2025 01:32:09 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f54068a3e9a38657ef87936c753aa588406125304fbbe89b79671f5d63c702`  
		Last Modified: Tue, 09 Dec 2025 01:32:10 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0263614e68ead4a6e689c846a48409a5da830949b9c43656b17a9cd38e7c5fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797f457a69f9375ca8e7813cbd8eb304e1b9af6f789f615f338d24dfc1b8c85b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:32:43 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5ada063695c84644b921c2a5b476e748422e496c2dd2bcddb0a4307bb897a7`  
		Last Modified: Mon, 08 Dec 2025 22:32:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bd39c062a07764309ef97e53ebe1c471e0821e07129c6ca2f37c542c13dbe36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786005dc7dc63ccccefef4cb1c054a792c5d9f2d56d4b195bebc90a58885f1d7`

```dockerfile
```

-	Layers:
	-	`sha256:000647147a2eef14b7ae804c425956c9df4eaa78b24bb602e681c5d48c38ae68`  
		Last Modified: Tue, 09 Dec 2025 01:32:14 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:430dc873b88ec3b23ee15f6adf2251c7df6ef21cf94485a86dc44ddad72f8da2`  
		Last Modified: Tue, 09 Dec 2025 01:32:15 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:cc330b9ba792bed94acd61a37923bf6272d7e420071a987a990d3f6805eb23cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb98eb6cfef2f58610cebf30678b8040b10fa3717733984d42bf80a7537792c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:31:18 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69d2dfda8c9c74f489e75b5955f4c568a0bda3e670da3e5f1b3ac92809351e7`  
		Last Modified: Mon, 08 Dec 2025 22:31:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:43d295205e160674c74015db18908db154a9521c4b9edde0ca117b7403094c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2c5128686fc21ae3426e987e876fc15a549362fd923f95b22ce4618bdae4fe`

```dockerfile
```

-	Layers:
	-	`sha256:23b19953284aa8d72988cdccdd7a1ddcf241a24d9d18fdc93609ed907f32c364`  
		Last Modified: Tue, 09 Dec 2025 01:32:19 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08516ca14bc16cfd18bcc12538cbaaba557f4a29c5da6edead0bc823d173f43`  
		Last Modified: Tue, 09 Dec 2025 01:32:20 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4fd445c590bd900378c596a78229bd4e46a463ba56d11c9cdb0352fe9601e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53108702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027697ade21e01bbef815b7ecf9a950b3f7777d95718a3f1b0c063071b4840e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:18:15 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cc577e358269ec956b5b755cc6590b8271f94efd5eb99125879e693ed6037e`  
		Last Modified: Mon, 08 Dec 2025 23:18:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9ac5d41fec9c7691136a0ae0539e237e656888f1732ab49cb06dc14e03756c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87abeadf0f05784ff195a9764277d27e1fccb922912469b3a3ab242b4e83d6a`

```dockerfile
```

-	Layers:
	-	`sha256:68141f51588d5d62a1927b9e1baff1c002413a0fde75c87c443343ea24e2e39b`  
		Last Modified: Tue, 09 Dec 2025 01:32:25 GMT  
		Size: 3.2 MB (3173529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b09a25fcc0ee73fafcc2f06dd06a2d8c908c10b542eb89b60e8b67fc5be92f`  
		Last Modified: Tue, 09 Dec 2025 01:32:26 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:3dc1fd9eb778b227be367d6845fa9abb625b33b9efa4c88efb76a01b64669b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ce49057bd31229d8cb4d7ff9083794e8537f51bf5f65e0f1ce1c54b59c908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:10:54 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12dff1e7bb487d7ba3caccd3b878e6905eeb0a06e4e4a46924ad485df209d8`  
		Last Modified: Tue, 09 Dec 2025 03:11:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4c52917c221b9c72c3d403d0ebb5a7d7e78f5bb19b79803a16ab7ce5cde4d35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2091d425f4117b1dee640ba049e171a545c3f1f9a22c99dc56bf1964c27539e6`

```dockerfile
```

-	Layers:
	-	`sha256:394f41fa5b863eda4492e97d7772eeb8015ecc583f93b8e66ceebf13328ed08e`  
		Last Modified: Tue, 09 Dec 2025 04:26:33 GMT  
		Size: 3.2 MB (3162341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6598d87e003e9b3fff781d948f7827bd2d7ab130d4ce505d34a9cff94b9173`  
		Last Modified: Tue, 09 Dec 2025 04:26:34 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:c60342d503c4c2c11717d83fae88d2581669d8b6cc52afee90d2992b861c8552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6ad8fb06aab927bfe169e9981fbe4820d920841f491798ac1570a5848470f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:28:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89309beff901776e6846a2a3b57e2bde31e849617a42bccc607f8b349d858089`  
		Last Modified: Mon, 08 Dec 2025 22:29:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:00932d9ef0000393b2315fa74c9017f68a1c204eb5dd471779d7c8dbc2143dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be911abfe1843e60337ce3b6f45a339da7be72e5910bb9e618633d1691f67b32`

```dockerfile
```

-	Layers:
	-	`sha256:551da3ce804f8fe809a5c3529df4cc762f568b71befe3bba6c7023f5c900ebfe`  
		Last Modified: Tue, 09 Dec 2025 01:32:34 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f862f7d4900a9d76602c42c8fae555a62327130a50f6fc892b6abe34941022c9`  
		Last Modified: Tue, 09 Dec 2025 01:32:35 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
