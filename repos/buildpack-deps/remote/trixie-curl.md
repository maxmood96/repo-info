## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:befa41103e023d23c4de97ac54ee67235660e01480c4731d7a3cfb69ffcb0784
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d295ae1c869f95a9f9e9061a82e02f11b4dfac2f37c0dffab94812804855f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74919245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c23e19bc0c99d184f5937b6ee665851244b6e1cf003a964820a5e86d996c7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6670ac6a207ed43b14d9d5a61c9bacc87aa29186a0d79da3c2248e5a8aacec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffc037b978e483455165db31e5e264a741818c44eb7e29b4bd2824a88821f3`

```dockerfile
```

-	Layers:
	-	`sha256:2b57adf0f4c82e987050883ef13d96d1fce3bd90bccae51c5244e0e3b75969e8`  
		Last Modified: Mon, 16 Mar 2026 22:38:24 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d35fd21bd4267eb25532b8a0ead8c72e9a82c40ac53c42a005edae5d7bac7fd`  
		Last Modified: Mon, 16 Mar 2026 22:38:24 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1cb84cd7a5cf81910bef7a4d31f825a8d9ba95873b4a5a2d63cda47a671f6516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71824815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c747679763d2ca9712bc9d0c2b670a851fd97f8e3ffa9cd955c262b68e98cbc6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a10acd8de7c2ea5feeb4bbe7b5147fdee10ce64d8ad5f6db26957ab6ab82a0`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 24.4 MB (24364203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:afd701dfc856d16e165b1f300e544a50b45ef674d683a92d9706761b60097683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997b4e4acfa51ac0b10772fc9e92e819401659912789c67cd4476a1149e1a173`

```dockerfile
```

-	Layers:
	-	`sha256:61adfa449559b7cbd23027852e105b851e24f39b1bfb0ac0be4f5004fedee469`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 4.1 MB (4122941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d650f8f865bb4290f411318bde69f318e88c0d2f42c4bdab8dd491ee85ae99a4`  
		Last Modified: Mon, 16 Mar 2026 23:17:06 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:26ace03386a0e2b0d218373e26906112167510ff860fc1355361a6385845f397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69369660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6affcca781375953176597340da0bed33f06ca0b45962c1da60ce46c205df49a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc6a08171f2d3110146343e7e0dfd05f04e224380e78100811189561ef273978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea45fe48e619ec1521e67c3d2ec9a8a47c54ed8190d2c9ee93853369b504715`

```dockerfile
```

-	Layers:
	-	`sha256:7aa51cb055ace8a92a211fc43c28cd21688c68fb5082f4a13a8f22c5531dd9ae`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 4.1 MB (4121452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280ffdd893d23f86530d85e4bd2af6ecc8a389716f40a0fd5cd2cd998f9e4ef9`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:056fa0a98cb8f5808c95eeb4967dbc50036cafe75ce2875b3325b2c9b80f73e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74688681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3e5250f8046bc00960d54b931383af2c84ab5f75f2a9585568c88e81e6226d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cef1888616375ed979a8323d00f43f5bcd6fdf4507d0bd2635bc19abe74d505b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630f8811187fdea307ec9021f9b2da58f8e523c5c63fde9dead40c16e05704f4`

```dockerfile
```

-	Layers:
	-	`sha256:1cc5b60f2be86a956d5caaa4af14846e911999e0d38bc6540885c7fc911f4a6f`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93293e9c3241943e492b24138bee6be2dc03cf23c2aab4a419ef4540c7877fa`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a8a7fa0b52917b08fde8ffdbf1cc014a920525ea68c736a435a62dfe6a0db50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77602331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2885a54e159286955fe6b3a4cefba2ed9821b81b8f08ee1785de58c0b2565e9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd4b4dadc2476c05b74fd72c6fd200da823ec7d541e55cffefcb77d4828ce1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb6301ced305c8a42d13af5d792660ddad1b1d28e79e314a4e8a56430710c1`

```dockerfile
```

-	Layers:
	-	`sha256:e95f0a3ecbbf8074650b996616a71c43bd847233ea7d7747d77d45aad7cf5b85`  
		Last Modified: Mon, 16 Mar 2026 22:44:30 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f07fe89164916fbec34d335ec8e736fd5f9ce6c3d5e5b12842cf337064ecfde`  
		Last Modified: Mon, 16 Mar 2026 22:44:30 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:be176a58f115b90c87ea352c2a8fc5826653932740e5838225dd4ae046eec4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80131741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7009e3e85a791b64500c74e0f8a12e0ddb6c37aa88f846b4e6317178429e2da2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1f79e1c0aa5a36734c2edcad458ea854e220500e2d1ddecfc27c4264bf5d711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697fdb040453ca0c2c9c9d536ba065b2f3579b206e8c351760fa15d88c7ea17e`

```dockerfile
```

-	Layers:
	-	`sha256:e07bf18a24fbe5ab11331283a10f3af86b91ab7cff5a70c943fe313b4d76a014`  
		Last Modified: Tue, 17 Mar 2026 01:51:11 GMT  
		Size: 4.1 MB (4123799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ef62b2d8b8bc66078590f1925780a5a11f167903006ae6cd47b2161520a354`  
		Last Modified: Tue, 17 Mar 2026 01:51:11 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e6b4104f26aa4967098803051f6e4b6ff20a0efb80ffdc2d686b5806eacde1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72747253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1889690a77155484cbbda4dd5055b0c5933298a3db2696cbb370c9a3494f6c24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c19a85cf63a6c80473b61d997556c1bb4697bb028d322791571302dd49a2bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bec1f2658efa493df153136e37a3878914f215131e8ea04c535ab1da252555`

```dockerfile
```

-	Layers:
	-	`sha256:72d6e7905677751bae114d3dc175472ec2c7f28d95248598c11a8df9b5019ae7`  
		Last Modified: Wed, 18 Mar 2026 05:13:20 GMT  
		Size: 4.1 MB (4112463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db48a6de01d222f5301b70aab59c2fe660c65612d7f873bb8bd51e5395b9ab5c`  
		Last Modified: Wed, 18 Mar 2026 05:13:19 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e4caf8df91fd5da6c526447b8292f07f2667d3240755fcde1c598ec7ef2d1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa3b97862428e2ba37d0a7a4d03fd7fa5855592e245b980d2a27659e97e8364`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d558e8a6d6e2a38dafd34626ed5431f5cf910f4125fa35344d7340dc43ec236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d142aaba3d70cf46211be8d3ae7603eb424b7c645f0b43cff577c7400c1e8`

```dockerfile
```

-	Layers:
	-	`sha256:a76bb1d4c2d859c61ab791ca0005952ab879481a3fefded3f7a4e94e9aa6f2a5`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 4.1 MB (4121361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314c967413203e50494f38822322c1858aa070e52c90a0cec2d319295cf85021`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
