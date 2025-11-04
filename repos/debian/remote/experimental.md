## `debian:experimental`

```console
$ docker pull debian@sha256:860b46bc142e91f376a2fb9ebc2e7686de2f6ce8b8696f5b1f899e5d742e370a
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:73903288738b6916fdea802eb4c6f738038b7969dfc8ed8e021a49ed7519110c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48383531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9c3112c47fa75e55ddd0f744287028201b54c7ca5190eb09833061447d720b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:58eb02d9919ba9b3a0f5ebf2825700cc92dd3be79e955ecd0fe4ab7b3f796f39`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 48.4 MB (48383312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad9566aa5ba57775f35ec6ac5f0cd19687028c2bf5298b4837bc7c09d9c0a82`  
		Last Modified: Tue, 21 Oct 2025 01:16:44 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:2bf783409d173b2e7e14f5ed9f3b0878f7b47e2bef09e5040f10bca8be7bcc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aed0fdd8e6cbd93981e5de4625c2746f293ee8f732a90c2363f34c8d0404f37`

```dockerfile
```

-	Layers:
	-	`sha256:1482337ce48db01b02dba1eb21e4cc03faac9b81b8fdd3389603dc628c8e9375`  
		Last Modified: Tue, 21 Oct 2025 09:23:59 GMT  
		Size: 3.1 MB (3128429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63add4f11e12871620d590a8eded66b8c235ac5fc881e3e122a6b762e10022f9`  
		Last Modified: Tue, 21 Oct 2025 09:24:00 GMT  
		Size: 6.1 KB (6143 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:9cee79fb9294cb6c9baf5bed6123e8592461576e4fb8b351a27ca8464fc97516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44911779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e593e9db7d626a5e8980ba0b3d4f6e2385da739bcadad0ba93723f218a9f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3e1ed5addbb759bfc99d610b4e40410dfbff1f72a6fbec8242f16018d1dedfd3`  
		Last Modified: Tue, 21 Oct 2025 00:21:04 GMT  
		Size: 44.9 MB (44911561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631240b95c1cb4d47564d607c2f5f1af80ae67093765965c8551f48e6ea6b8c6`  
		Last Modified: Tue, 21 Oct 2025 01:17:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b54a4246f4f39804e2839f0e87a5ba40ff2fd961d3cc7b79a531290518f70d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5d0ba5f44c02a91e467cabd8fbff6fcd55827e2dc1875f9d105000cca4e333`

```dockerfile
```

-	Layers:
	-	`sha256:75acdb00aaa3aa0a6771dbc6aec3c4266ba61a1e185c4d3825a7823eb4237a4f`  
		Last Modified: Tue, 21 Oct 2025 09:24:07 GMT  
		Size: 3.1 MB (3129805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e43775cd947e47c52dfef4cc88fdbe77c35204c652de3c825f93a03c120bac`  
		Last Modified: Tue, 21 Oct 2025 09:24:07 GMT  
		Size: 6.2 KB (6206 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d4ed6bcc8123f86aa87aee6ccecbbe263ed3c53c7a1ed97b7665fc4a9d1f6113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a240e178e410b0b058e63bc47220d9617ef24a6b46daa71029291d43d1dfd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e734190effa5b1397b77abf8c8ac98748df67c72340e4e8810b0a7b973ef3902`  
		Last Modified: Tue, 21 Oct 2025 00:23:29 GMT  
		Size: 48.5 MB (48506036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05d46644b3ddce07862c88786b7d0179cd474aa6567942ba45eef5d77322e6`  
		Last Modified: Tue, 21 Oct 2025 01:16:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:1b589ce41916cc452c7b7f958458b0453d9227809ee96649bdbc805597ceb7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b7a9fd88a0622b5cd6de0a024d34d3be96af26950a200613a44fb960928245`

```dockerfile
```

-	Layers:
	-	`sha256:f340c5ae7941a7de185cbad1cbba90f2fe5cadb5f3a865d457c22d16ffed2d09`  
		Last Modified: Tue, 21 Oct 2025 09:24:12 GMT  
		Size: 3.1 MB (3129282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee3db1285c15f0eaa7391e527427990a365eed962702c670fdc5e9dab68c2fd`  
		Last Modified: Tue, 21 Oct 2025 09:24:13 GMT  
		Size: 6.2 KB (6223 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:ba87872c80718287703d0f0010ba581d6bbb00bd323d6a97c4e7921df754c787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49718393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a405fac53d09d12005a1f8606ad59ffd62b987374c482494316ca31d40b95335`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:199813e54679f363ece1e193ff94496d7355274ca4ba40a00ab7d972f02ce9c0`  
		Last Modified: Tue, 21 Oct 2025 00:21:20 GMT  
		Size: 49.7 MB (49718172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84da89cf3f6c97f5d1fda7a5b6ee2660f1b6a3e53f02d9ce2ebf79ee2a16ba98`  
		Last Modified: Tue, 21 Oct 2025 01:17:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:8398a2d979c9060d16239f8578ec3ca391924742b5745abb15d72680947fd617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240d0208fa03a52a411b8d9a34951d69840f53fbff39c4925591110982e5d573`

```dockerfile
```

-	Layers:
	-	`sha256:e21c3a8e5db8a6543d228a69f29fd50189fa4233f8102f6e17d0e4d1c5d67d15`  
		Last Modified: Tue, 21 Oct 2025 09:24:18 GMT  
		Size: 3.1 MB (3125633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d79ff17d85324f187c87d5259a2f8a1f728696a696590ab675a6f2b1afdd99b`  
		Last Modified: Tue, 21 Oct 2025 09:24:18 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:cf04b6fe3ae65d5651fcd27b4f41c5f3bafdc82688efbf3684779083e2a33e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53217787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265e7d8b3b5772fce672ad45af841b0e25d96bc9462bbbcc99f17b3979763cd0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:14cc1999c784e572327aeeb92ce393c6ff43624365a3da15c29b6b6c481bab00`  
		Last Modified: Tue, 21 Oct 2025 00:27:29 GMT  
		Size: 53.2 MB (53217568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124fd059963d91ce04fa2b76320bb3ecec97cd78e9dce9190bde106a879b5539`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d353ddd7535ce04a7053705f0150f7dad11cecfcbadf37fd25fadf20b9b178e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452d1b0b0fad3b338c4a421029af7c09bde53bfef8c474ed242d78f6aecfdb9f`

```dockerfile
```

-	Layers:
	-	`sha256:a7b1b4db397a5200a442e18d3b8d7ef66967b618a226368b1f87f136e2906b61`  
		Last Modified: Tue, 21 Oct 2025 03:25:46 GMT  
		Size: 3.1 MB (3131924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564b0b815054428b9f26c8ebe9480871e0784a0b8a1f71d04aa57e179c6b117c`  
		Last Modified: Tue, 21 Oct 2025 03:25:47 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:dbc99e94eaf2916f4b07e620497663044f28cd329cd52bdcfb1c99c8cca083b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46794483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900d851b92f21bc27aba41df6a5c037631e5069dbbf5752c3936bce6d3afe30f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1762202650'
# Tue, 04 Nov 2025 01:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5ce854dd87e3899c0d57c1835e481664836dfe75977d3564c7675f6f1ba1ced9`  
		Last Modified: Tue, 04 Nov 2025 00:31:19 GMT  
		Size: 46.8 MB (46794263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e6869944b29d41dab954188f29c3f15e94e9477d231a1d6eac2e602035cfe`  
		Last Modified: Tue, 04 Nov 2025 01:26:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:49a4a583a4dbba391386136b0bdac4d1bfe1544011d52cd17c789c330f11fbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6da0c16a8f6ac775eea9330c00cb029c8e0745fccf92537e43e9d697d6982`

```dockerfile
```

-	Layers:
	-	`sha256:9829ff021fac7e623a1c72c7711e52f5176a0c2ec8110731589160d5e2fef698`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 3.1 MB (3122164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd6cb624db078091ba0d61cfb54b87794f69e1e17d4a3984938fae73040f97f`  
		Last Modified: Tue, 04 Nov 2025 07:27:53 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:dc9c4c933f1ecefab68d54964405d84abefa771abdabf7807939007cd05a72fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48267420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a875972afbf378b1918cd430b040451900b0d4d68d4daaaf2d50903d145c8a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:330cefb397407e3787c114e91182f1ed2d6c5a2abf3cfe6d7e392511d3a8a989`  
		Last Modified: Tue, 21 Oct 2025 00:29:24 GMT  
		Size: 48.3 MB (48267200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd083a7da9dcfca5a1d8fb4710267cffc099fbd0cbe54771e9c30f9cfa43a143`  
		Last Modified: Tue, 21 Oct 2025 01:21:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:3c035ce6298fa5db824a3726bb3e0ceaa5a22f17fd83a89ef508db9b1dac8924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282dd14a51ac1c825042e894bfc2a8f87f141bff2eb65f0ee3bb4468fdd83599`

```dockerfile
```

-	Layers:
	-	`sha256:cfde6fb393ad2491d26829fac4ef8a02904d5469542eb66568417485dc36ae27`  
		Last Modified: Tue, 21 Oct 2025 06:24:02 GMT  
		Size: 3.1 MB (3129878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf089708c7869c236556a61d2ca5a66f65cc30c1efef72afc539e7fe1a0f9d83`  
		Last Modified: Tue, 21 Oct 2025 06:24:03 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
