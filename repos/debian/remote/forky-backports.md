## `debian:forky-backports`

```console
$ docker pull debian@sha256:6543a2de22a1e1628bfbba52f0dd73443a57b27444da33d40e0f442489197858
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:00052778970684383419528930578712f0d6085f1c12b0f683e525187987a5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49737041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf83a8097b0063d551ffeb99cd87502f9cffb6b2c149e07a00da515944da213`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6c286e2fd7b1d660937f47e01bdfbbebbf572b731cd40afabe976e47c6e524`  
		Last Modified: Mon, 29 Sep 2025 23:46:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fed027c65228deb48b41fc99648cdfb8671d959e05bd9e24f71a7dbcd47ccf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519f900f364277676d246631cc2d626a4bf5daf41562003c23a2b794f48fab74`

```dockerfile
```

-	Layers:
	-	`sha256:1df8648015c4179a685e12c9c411d8c6aa50c49a9f70b010712c6609f8a96c7f`  
		Last Modified: Tue, 30 Sep 2025 00:26:49 GMT  
		Size: 3.2 MB (3164642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35789808cbae0255a39331c8cfd4586a55758efee53ff8942a4d55dd6cf2a63a`  
		Last Modified: Tue, 30 Sep 2025 00:26:50 GMT  
		Size: 5.8 KB (5821 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2f55cc1095e837269ff905bf1460528f1680503809fac23111e8760f3b5266bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d6ab42b9ec01bd70d01a923a2ad79a79daa0565d6033303f39601825e8433d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:43934bcb3ccabc44fd5dd6a6383f81957a551493c079cc1ab7f71f687b26a8cb`  
		Last Modified: Mon, 29 Sep 2025 23:34:21 GMT  
		Size: 46.0 MB (46020847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3681916cbd085d3e0ac877844a03f729f6d97092d382a1f63c104a0a745a490`  
		Last Modified: Mon, 29 Sep 2025 23:52:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18585a5836b4856197978968c5233505a9fbd614173cb5ba68883687251065ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02913ae4cd943042212b672cee79dfdf0a1dcaf6425189b028d202cd55896afb`

```dockerfile
```

-	Layers:
	-	`sha256:3840213b54ba3b1602ad13a1d4fc97ee3ba5538da4d744dd3f5a1b483f824fc0`  
		Last Modified: Tue, 30 Sep 2025 00:26:54 GMT  
		Size: 3.2 MB (3166016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b804bb7f8d207c3f798108d784ea03a71a3f2521e2740979e0d56f1a9bb41f9`  
		Last Modified: Tue, 30 Sep 2025 00:26:55 GMT  
		Size: 5.9 KB (5877 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6bde1a2e2d5d36bb0d15b613023f392510512d4dccd6ea9a1f8690541285fd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49880099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d6fbd6f569387c6648e63849fa8e62f66f19b069ea9ca7f73a43545f7e770`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244298ff15486c8d2db7987480eb1beefa2c5d4a4fb13c5c304c0fa299955d61`  
		Last Modified: Mon, 29 Sep 2025 23:47:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:786ffa49bc8631875cda6f0c6a29b2eb914c2ce688dbea7ddbe90690b8046403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96564184cde40a99726dd532c0ad3df72098240f3ff40eebe2d128d31d21c31e`

```dockerfile
```

-	Layers:
	-	`sha256:08725c2391639bde9084a8d5ee60fda89433393e2f9b9bf3f28cfaee629f0b40`  
		Last Modified: Tue, 30 Sep 2025 00:26:59 GMT  
		Size: 3.2 MB (3166123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175f980a6b8647dddbcd7abb3fee2023d5dc11f4c799b0d06cb4f7c411b48bf3`  
		Last Modified: Tue, 30 Sep 2025 00:27:00 GMT  
		Size: 5.9 KB (5888 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:5064872f8169f374ba5a9dbd94d48e7c282f2206cfe591557fefbd203a8dd27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51119643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c785828632ca7fd4b30779999c4c28261806d3f24aa90291528caa3f657d2373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2abc7d128125a1f8847d71ee5be04b887d0eff0080c538f483744ebee5bb9`  
		Last Modified: Mon, 29 Sep 2025 23:47:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:68b87937ac1790716b74a52062fcf7454abee06495fe74cb153413ac84a0ab79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a4e577676f1e8d711c34ef8a97f82a62f42f5b172e7b4f7623d63e7a0cba89`

```dockerfile
```

-	Layers:
	-	`sha256:be5ea50e4fa7ba8c40a7f0119984189f67c3cae88ed05ad555234006163e602d`  
		Last Modified: Tue, 30 Sep 2025 00:27:04 GMT  
		Size: 3.2 MB (3161847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a1206dfdb9ed9749bba906ad1de5ac8311f497c9aec2af100c2c7e89b96b15`  
		Last Modified: Tue, 30 Sep 2025 00:27:05 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:db3e0914d0b9a42275f06c96ab88d3a4f388fa3f0a39a61b19960c185f8d16c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54876019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641b50734414fcd79630a90c739048cf5f89e8e65976ef3579cb31640ec8672c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7d4356e03351899ba9f4be32ba46e679bea4702bcfe72d9b6fe6e31094e1e6b`  
		Last Modified: Tue, 21 Oct 2025 00:20:47 GMT  
		Size: 54.9 MB (54875797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f8aa66e99c92b69da5df402c468a30928d4e0494bcea3611685a99d93bf1e`  
		Last Modified: Tue, 21 Oct 2025 01:17:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50e5d6bd7ced01eb949aa097bc520b70d58538ffd6eb2a1623abb9bb3629995c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19445356f55d310b3c3d38d58b0039cce33ac934fc21168fb3d4b7b2b48ed4d8`

```dockerfile
```

-	Layers:
	-	`sha256:64c9398732898f20a356b762393364267abcef051026d24d79b4f2cf3c601d2b`  
		Last Modified: Tue, 21 Oct 2025 03:26:41 GMT  
		Size: 3.2 MB (3168396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a167b3c99972300dc801a1740ccfcc3fe10521e1cdbf59e9be7ec35694ec8eac`  
		Last Modified: Tue, 21 Oct 2025 03:26:42 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:4ae96fcef554f38834687e8df3a9df721f160281a7b4586e2b3e4ed05b7b7e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48012033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5d6564f61489e55df864b3d20bc0cbf3560de9a8067e974a6f7f65685705a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:900b76287341e8d31ab6f7e93e1704f0b3f8f921cc26e9b52c61d9ca744682fb`  
		Last Modified: Tue, 21 Oct 2025 00:21:40 GMT  
		Size: 48.0 MB (48011809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31924ad070758999f178f24474833970ca465a0b22ec64268b71c38d24746c1e`  
		Last Modified: Tue, 21 Oct 2025 01:17:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a5ac55b31a81416f473b4f630046130e6a67429eb24a36916e104c6b3aaf1750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da873096cd78b4b14a690a34d0ae01e8270f40c988c7f2144df2a6e774ba630f`

```dockerfile
```

-	Layers:
	-	`sha256:ba575357188a268c17af834c8823c71b813db1e6a5bd78663382b7f123d7ea34`  
		Last Modified: Tue, 21 Oct 2025 03:26:46 GMT  
		Size: 3.2 MB (3157198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e9029434df035c9975268de58a70a4996ad61f490d59d7ea24810be7960e41`  
		Last Modified: Tue, 21 Oct 2025 03:26:47 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:da0021dde99c6942cbaca05874090c59cfe6380ecf66db9aaaea59a471229bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49621011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71496646729e3ee5f6420148b58bd7a5afb61c13066c1895e4131469674c32e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c17c2477a00887cc596493d4aa463fcafb677435d66760d41166feb0acd2773`  
		Last Modified: Tue, 21 Oct 2025 00:22:26 GMT  
		Size: 49.6 MB (49620788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f29195d7a7e858a3f3f0ce3e2fc228048975901399a899415d0ea6ce17e765`  
		Last Modified: Tue, 21 Oct 2025 01:18:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50d5d9e57fb78327d7c0d9eaa97224d7f53c637cbbadd460f37bb260a82ccffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d45d36c06f4ed5298caaf5bd8aa765be9ee4227ad5a7fdc0be0dbd010eff56`

```dockerfile
```

-	Layers:
	-	`sha256:db2a0d3a9e0fe8a950a94cb77f4488e76e888fdabd51ac37c352f59b4dbb6621`  
		Last Modified: Tue, 21 Oct 2025 06:24:15 GMT  
		Size: 3.2 MB (3166336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64444ede407510375577a3242df81498fce6e9e4a8c1ba39c3b0d5ae8c65ff6c`  
		Last Modified: Tue, 21 Oct 2025 06:24:15 GMT  
		Size: 5.8 KB (5821 bytes)  
		MIME: application/vnd.in-toto+json
