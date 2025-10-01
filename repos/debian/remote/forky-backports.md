## `debian:forky-backports`

```console
$ docker pull debian@sha256:b47918edb14e1d163c71e1a31609762336fa121970f018dc982dff3a7b6c9c65
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
$ docker pull debian@sha256:23e34f1f1792748a551b9a111f2508980d8fcd1d5a334145c5af66c3b22c30d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54751102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dada28b80bfd614a6a6e46d220fe7e54b2172129a5a2dfb2b9cb112d8da2041`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c998caf3e9e3602596b17377df87ed145d1ff51c75338d4bead32fdc1773c859`  
		Last Modified: Mon, 29 Sep 2025 23:35:22 GMT  
		Size: 54.8 MB (54750879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7304b8035fe6569695aa5f98d960290eeec170d6be5aaeef071596bc85a635a`  
		Last Modified: Mon, 29 Sep 2025 23:47:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f53978410c7628080e2b52cb71abb161fde8063d4be0376785827454704fcd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1ee183e60503ede542b380007d9971da81f287f0c6bb9ca4d7c97e9012df00`

```dockerfile
```

-	Layers:
	-	`sha256:e07b50009ee3af69e5e7fe4fc7b092d97a1d0ccb9ca0cd389d649bd2478bb01d`  
		Last Modified: Tue, 30 Sep 2025 00:27:10 GMT  
		Size: 3.2 MB (3168149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029ac2a540305662499a7748dc05d9f28d3256d1b979a0382b660388d0de18b7`  
		Last Modified: Tue, 30 Sep 2025 00:27:11 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:061ea159ffeb4504bfcc1d80d8142ee0c2bd969f2738eb91c6d1141d9de9da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47970315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0945ba54684a93a2d94838cd77edad0312a61dba24a497ed14660ab4e1be0e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:db7be57cb42d3da83b1f69e7698442aa575eac43cfb6c579690c32c4f1cc1c22`  
		Last Modified: Tue, 30 Sep 2025 00:49:36 GMT  
		Size: 48.0 MB (47970093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c6976fde7e52ff63614c2a323ae125de2e67016f83d0c093f87fa4b2c04518`  
		Last Modified: Tue, 30 Sep 2025 01:24:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a34f47b4533bedf4e6176362f6c9ac1c8f2b094d702d075a62ddb253960a9e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f78caa9db8096f1f5b1b1d2bb18b7385e3975df5a90939bac03105c6dcbc51a`

```dockerfile
```

-	Layers:
	-	`sha256:f416b08b56124373d91d8bf0e34e17c3030245bece12b9ca3cdd6bec75ebd43f`  
		Last Modified: Tue, 30 Sep 2025 06:33:17 GMT  
		Size: 3.2 MB (3156951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be64ca71189b59b2de2cc67dc1ebd765a91790798390f43dd2db50327e86b350`  
		Last Modified: Tue, 30 Sep 2025 06:33:18 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:d59d8087790cb94ba2e6a4fadde12110061da1342988bfbeb82ccf09d286a734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b19f3fd9cfcbc738c18c4a8acdc1fa7eaaa5bb44f5e3f1b2511237202f9af0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f12f0b09af6c73f5ac02ec4057426f99780ba4cc2b7ffa5da8754ce19dc3c40d`  
		Last Modified: Mon, 29 Sep 2025 23:35:21 GMT  
		Size: 49.6 MB (49576014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4589daee2ad11613eeb9a5f4f23f144f7efbb68d65853272f5a5b7fd2852a9d`  
		Last Modified: Mon, 29 Sep 2025 23:46:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6211de5677785dfaf6a790d8d8191d495a2b85c1ea232e074f0eb0b16d8374cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d6d7359da3fb40e039c09fca6f36e43b37dffb0e806ea056747ec2ac906056`

```dockerfile
```

-	Layers:
	-	`sha256:843c4c55262870215f76a84fe3461f4c2d7eed584bc50079cffb64cf3d5aaaaa`  
		Last Modified: Tue, 30 Sep 2025 00:27:20 GMT  
		Size: 3.2 MB (3166089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5999f2e456d72eb258b7a4677e5eee6c8830f2f3383c5a165d3319b5788712`  
		Last Modified: Tue, 30 Sep 2025 00:27:20 GMT  
		Size: 5.8 KB (5821 bytes)  
		MIME: application/vnd.in-toto+json
