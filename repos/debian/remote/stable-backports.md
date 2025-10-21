## `debian:stable-backports`

```console
$ docker pull debian@sha256:7c6d119d9c4b02b8ff581a7774c2728801f0e7fd580b8dd8e5d49657be538939
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:da980cebfb4383a4892a2f95b62b233103234b8a29d6c059f45fa1eb1fe848f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49284851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687df0c30a835d3e035814d00d5fdf501d2fcaba3296c97853a9e3bb48259ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a1d865bc2cbc03af4eecb96149727facea254a73137e774f5041eecb07a31f52`  
		Last Modified: Mon, 29 Sep 2025 23:35:22 GMT  
		Size: 49.3 MB (49284631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f6476d7b7b24b618ebb7267396d788e0694e566d9bc2d893435f5fdbf9dd7`  
		Last Modified: Mon, 29 Sep 2025 23:47:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5b8ff1dce9a1855dc773061aeb5342bfc2f90bd6dd546314b06993636dd70d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98436aabcc1d723970f92151bd7967f07486041303f9cc5a57ac7eae5df1198d`

```dockerfile
```

-	Layers:
	-	`sha256:179dae4cd0bfb263f1267b67ab8d01c071b6aa08b459d613813a3d98b4bb564f`  
		Last Modified: Tue, 30 Sep 2025 00:30:31 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5759f94ddc731721ea331f042f8899d82b216614c13b0263b4ed6e971b29035`  
		Last Modified: Tue, 30 Sep 2025 00:30:32 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4cb1ea063c64a975a84614bff9e32480530b5c0a2a273dbcc5fa7e85b33fafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed947ca2fbedc49195edad41d2a8d17a394adf942ba00a531ab3b3754b53e09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:80094a5578dc7efe1835710a1036c601b497627fc6edd87572c1921d489635bf`  
		Last Modified: Tue, 21 Oct 2025 00:20:41 GMT  
		Size: 47.4 MB (47448773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5adff649e20cf479ef1652f568fb9bd8aa2944317e1ece77d93edfe89621d7d`  
		Last Modified: Tue, 21 Oct 2025 01:16:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fe7808fd83496d101e0ce9af9d81b3435f8b13b9d28f5ffd47419aed7c305faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4141446ec95ccd2324d46dc5cc673cdae6bb4488dedacd67777a7999ead4f3b`

```dockerfile
```

-	Layers:
	-	`sha256:e99f4413ba76608dc180f1e2b06c6bbc29347bcc3ceaa953ee049e6e6bde512e`  
		Last Modified: Tue, 21 Oct 2025 06:24:47 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e9e0557c7813531045824055e502e84271cb799d755651213a677ff9833d65`  
		Last Modified: Tue, 21 Oct 2025 06:24:48 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0e2434fe5b7ef98eb802afe746c7e5137ad907cdfb97e199cc72d5a66ad5e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fda7cb9c8c99757663d47c2c5159506c749305a613f83d5432e5535cd4c4a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dd26cdedcb5a26641c601cd55df184a46de3242898466351fbab2e0a2e910745`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 45.7 MB (45716140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6010e3934f8e4f740ec82fe7b2a6ce5c01a0a1c78efca8ee32edd71c1b8a836e`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d974ac1f9df18be7633292bcf007108328d6e7874a1fb095d5e1e9d7ad9f7ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfdfa778a3974e52ecd20a0ecf5698223cd5000c5005c7793fe1f09bde56121`

```dockerfile
```

-	Layers:
	-	`sha256:bc372be43b0e63066610bbc6469bf540e62967bb8d350f3115671c111354fba5`  
		Last Modified: Tue, 30 Sep 2025 00:30:42 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479d981026725f1cafc31eefa6a7526822f9bfe63c2665829956d5618ef3f64`  
		Last Modified: Tue, 30 Sep 2025 00:30:43 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5d67c95b97712d8af9c8fedf03ae7dcc0b8c567fcc984b14fdfeb7cdab846f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794e3d7058b0c37258844950d458d3d3ffd443e16b7d4c5c1b66f11367ceea9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ea1fb054c1694119de48ab87827d654b58de87d7b24f19b97f20bceed0351589`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0783ef4a35c59afa669ac4e7d87987d90ded2e8a21157c1c74f9a095c3d451f1`  
		Last Modified: Mon, 29 Sep 2025 23:48:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6e91fbfb01fe995e674fbbf662451928e0f8a34a0868d00f3e1fd05cc3ab422d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9811cf3f4c439a16e8b4b98547cf50a3234f5cee0d3e6aabfbecdf88a69d2290`

```dockerfile
```

-	Layers:
	-	`sha256:ea149fe9fb08ff1976ee49bd9540e88a0565e5714dc2340599c2fe8cdf2fd0ee`  
		Last Modified: Tue, 30 Sep 2025 00:30:48 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e9ab51c2eaa643a0e181c254b72ca5352bb1f91e0797ce6c5ebf8c56647b7a`  
		Last Modified: Tue, 30 Sep 2025 00:30:49 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:2c5a1a3357aac8ea5e96a734fe731780021cc4855e67980cf5807b1545436323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93632df1cb8e14a167581dbc9fa5613e6a02bab6a5f22f73347fa9012ab6550e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04c256590493e5279994c2b667347046decd878edb6c369fa049519209f18f21`  
		Last Modified: Mon, 29 Sep 2025 23:35:31 GMT  
		Size: 50.8 MB (50800228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66890eed937553d683336c68e5ad39212773f224702b61f7a097d884705b417`  
		Last Modified: Mon, 29 Sep 2025 23:47:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1d42888945865ac8392cc59a8daaea8ec8f3ff3f1578768a9fabf400bfef6199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694dc726c4f8b9539c432080fb666de28354e1b4ebc46b2ea71eb0966df1a1ae`

```dockerfile
```

-	Layers:
	-	`sha256:0b6de5c9440b16270aca8235f6036d3f37a95a6d4d6fa3bd9766ab69aa97d57d`  
		Last Modified: Tue, 30 Sep 2025 00:30:54 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e34a6328820ae22720f984477dd6ad0de1e4de8ef4aec3e6882679e312c5ae`  
		Last Modified: Tue, 30 Sep 2025 00:30:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2ed85bf8dc961602c912a03992d48f722a88dcedfb2936acc9060bc24fa7e9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43d54c709127f916fd01d4026380910f4738cb6d87d2e2d64b1f5e12b75629`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ca94fe6a275d41a3b12e4c7e00cee592d38d6155166afaa561b4cff2231ce178`  
		Last Modified: Tue, 21 Oct 2025 00:24:25 GMT  
		Size: 53.1 MB (53109480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cbd16019fcfc11d5304fb60e137cd43ac9ab20bc2169f5df05eee4afe88042`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2e984b6a3a691eb338ebba4826fbb5b98c3c5d1cb15883c3774733e2bd64a769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cac4d833cb6ff0f4300a5e2910a2fb2b17d9cb38f8d0defceac3ae455ecd1b5`

```dockerfile
```

-	Layers:
	-	`sha256:69ecf7a5d0878a17e39071d31864f45a75721660fb846cb46c3f84636804c386`  
		Last Modified: Tue, 21 Oct 2025 03:29:50 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eeb143e68340d6c437d5c5183a2be1a98f80dcfd907ea564e73c252b7806ff5`  
		Last Modified: Tue, 21 Oct 2025 03:29:50 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:26fffa17bb22e52cbd9bb64dac4b13a72adc7cf90cf2ec63f2eb371a24fa8b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ae9722310ccf265b835740b3b11167c2827f2a1af1e4d1b740e78b9502418e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b348b7755bb5988098c7f7833dab3d76ff29364fac9028ad5ba6b2c787de6101`  
		Last Modified: Tue, 21 Oct 2025 00:28:41 GMT  
		Size: 47.8 MB (47770305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d702afa00cd6be80e07517c4ad1e6a373352853b103455b5117c059164746`  
		Last Modified: Tue, 21 Oct 2025 01:19:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:857fcb14799ec0a314dcdb5ccbf34a173fb4d051d01dbf29d467752a7a75e751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a128a676b5e6455a6feece72b63198bfe2b678efbf5121739a05756cd2279628`

```dockerfile
```

-	Layers:
	-	`sha256:186b93a088319dadaa0716de15c1d562afacaf63222c3fdf71cf2cfad34c9d0c`  
		Last Modified: Tue, 21 Oct 2025 03:29:55 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27666821aee25b91c6c152e1657771e241da1920b0812848c0eaa6af84f7808`  
		Last Modified: Tue, 21 Oct 2025 03:29:56 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cc912186db07cdc73d1ab39a122fb53cc9a6a7dc1e602852df5ed7c442cc79af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac7bd81fec7f986b41378d03c4939271c7a0c1d6905f10fbf980b1cdb8bb91d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e1220200624cfdd58d57667ccbf998a0f86f915373fc900482a65672f078f95`  
		Last Modified: Tue, 21 Oct 2025 00:25:36 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e9c8204480f013c60ba96d3d3a69d32c3826ff5385d07472180b0d262e2178`  
		Last Modified: Tue, 21 Oct 2025 01:19:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c550dbd5211ceeadae1e393db15aded05ab293d879b50a509cf9a8a1a189b94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9a844ffc9849b5eee664ff59d356e4fabfd28cadad93e1576cf8d72a30be97`

```dockerfile
```

-	Layers:
	-	`sha256:dd45a5efc37443c772e90e3b801b55a83a6575f226765879e021a16eb6fbc2f7`  
		Last Modified: Tue, 21 Oct 2025 06:25:04 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7559f65f9a24bb59614743b66c467ee725c1aca744ed27d6d304dd44094689c2`  
		Last Modified: Tue, 21 Oct 2025 06:25:05 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
