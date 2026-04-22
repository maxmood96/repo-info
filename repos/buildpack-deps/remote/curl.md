## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:41352ce39d75a2419cf99b4cd31c736190d47c698103853abf144f74ce9b9a46
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5cf1317dfc446088fd8398addabc67da10dc42f8d25ece6aae6f83ac11b6868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74924545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dd4df12de63984ffd801a8f28bf0c4734a03eaa11a41ee729f08ead389a511`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30be87dd2f96c581cc094e9cf292a574dc11b38db02e2528fc7e38fd3fc1af8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d8e2b6acf03b37620dc90066d461f250fd68f4592199d7c9a9158e5b74c1a1`

```dockerfile
```

-	Layers:
	-	`sha256:3d2b18939cfc39533ea779a8141778424275852a11da46db0d90068159c3b16c`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6929ffc5b64823fc28c4e35cb3b0479abddca247838ca0291c963955754f4cfb`  
		Last Modified: Wed, 22 Apr 2026 01:39:49 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e2b2d31ff6786d69a3c7aa4a5c35e4b5f397b3ca56a478b7dd4dd003e8285824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71825078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260a8569bbc9134055d53c9ca7defccb760701d852e1cd175fb9c0aaf3b1e7b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c635b73b8a91f67dcb5ba2db26dcc3f74099816e3c14bb345601bfa9d19e569`  
		Last Modified: Tue, 07 Apr 2026 02:46:09 GMT  
		Size: 24.4 MB (24364186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95b31280036a21e8454315f123ed942568941ac6ee88f0f10f6c77ac1583be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca572e51f3e48dc8312c267eb985fffe95ac263471a3a6895f4d6f504df0672`

```dockerfile
```

-	Layers:
	-	`sha256:527fc1e77cd8bf153398966aa20ea9c2d8e084adf299c747cedc97e7be181dae`  
		Last Modified: Tue, 07 Apr 2026 02:46:08 GMT  
		Size: 4.1 MB (4122941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72fd710f7983795f446961a2cc40ae9cbbbd11b021ac3a2ca9d3792c87d1825d`  
		Last Modified: Tue, 07 Apr 2026 02:46:08 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:776bd60a73a94349ec7680d47b7c9109b17899a9e793c81646bb3da29dc9681e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69374809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eec7299c7f704ef1a788c391ce87983aef059bb672154150ca689b37120d322`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fac7c594bdd032deaa673e94487ba17b8b7fc8297285daafab1d169724391c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79109c0c83452fd6be3efd7d11f7d1542b44925d3db9fdcc387b7e2510b739d9`

```dockerfile
```

-	Layers:
	-	`sha256:f522efff2c7db1fa35a114c75e48928e16d27605384a676ab90e21f0ce6fc593`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 4.1 MB (4121452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b1fd1b206dc62682f9073f3f36cb134dbd4169d59854ad0e2c7d7975238fb4`  
		Last Modified: Wed, 22 Apr 2026 02:19:58 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e2f6d0ed953a5a058247ab2063d3cb3df58528e92989544131fd984e6a9ecf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74692654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5058161888f1f935040ef6055a7b1676e77c6706162a7ca640d02b02a3616f5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddcb3582c614ab90bc267d7dc67ad7b2fb33b4de12d692a58faa1a703d8c7983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5508eb468dec9d0c1d5512ed713e4ef00b0c90886a401badae3a4215556a66ba`

```dockerfile
```

-	Layers:
	-	`sha256:583582c8bccca65d12dfe50f843bef284a1ebe2e53ef24bed060db6ac738793c`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5481bce96e1621e51f3b6acff13a5f16a4b32e02e3623c920db3b57029027f`  
		Last Modified: Wed, 22 Apr 2026 01:43:33 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ef4a562251ba325b97ec882a86e0398835f2033f1903d0270c6c56b012f5b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77602467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9103f5b4d70bb09905518a8a329f4d2466abdd5dd20d0a13bb3e01310b376e01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7231b934c72b819a261130d93baa9a78a238cacd81de0266c3a2f365e10a3314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0829a33e83373cf930fe8d8d571f1703d2615df046632875e8ff9d3dd345e1e`

```dockerfile
```

-	Layers:
	-	`sha256:44763a27d7ad233aefb5de76878ae595d38fce9a278553c17ee4fa224b126410`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1130c9e3ea6fa11f53a5ac25bbdf8d51746e1b699e0523df929f6b1edce922da`  
		Last Modified: Tue, 07 Apr 2026 01:46:38 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fd3c42f20f54fcc8d8532587131681891950963970cb704592edfbb60f4971ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80132517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dea625ca66709ad7848ebad74eaa5809d9a9497811e9d88ed0519c014ffcf03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8679e4157d5d1f624a68cde0ec9ce5ffd6207d54b1363f25ace58bf01c7a1336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5498365be2f88512e34e024997633a702b813727af71917e2a12a503db8f566d`

```dockerfile
```

-	Layers:
	-	`sha256:501477fe3e81e0e594ca333f5cbc26964ec74c5b47be2fcbe0af0f3fd181b940`  
		Last Modified: Tue, 07 Apr 2026 04:23:26 GMT  
		Size: 4.1 MB (4123799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df46446f1d723440c11c48e7894f678142b74fcba10d1339110b2b61200f567`  
		Last Modified: Tue, 07 Apr 2026 04:23:26 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:dfd607fbec4e364d0b0395ab5fc8f32add2ea351f74abffe10044fda3b4b1106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75911391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e97ebc4a6d1c23e7e19e85d8ba3327deede39d4ddda19f83ab1b319d102c4a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e93fc18da2e58c4df1694ee2e451c85e25cafa0a11c9b83359608c46b672d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92eb19b803457fa59fbb3d3522a22f4dd230f0125de5cd0028c721cd319bca58`

```dockerfile
```

-	Layers:
	-	`sha256:a1624fb1017504967e23e0c130084870d81d168fb8f6fdb071437a16a4500ebd`  
		Last Modified: Wed, 08 Apr 2026 00:46:04 GMT  
		Size: 4.1 MB (4112463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b253441409b3e581cbd1f8a8b06b97878ba256d60d933248e3ddb66225a0d1`  
		Last Modified: Wed, 08 Apr 2026 00:46:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5d55ce766d35870f9e4300e7cfda7f2396e8a60bfc80b67b53a039f9bdb3f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76174531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18020ae2aeafe6a736eebdb8f016c1241c41846776806a8e2d8104dee2b8b93e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5ac32d9401ac5d551752ea5160b6b5c2c2c552e6c4f397c27bbe383d517d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128661342c1578bc5a97ba303300975c876f77a7ed3fdb27e05e93b79e2abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:7c7fb1b57c203b82952299cfb36d3ea77d8f8de1e712fbb0670c09aac0bd4f3b`  
		Last Modified: Wed, 22 Apr 2026 02:32:50 GMT  
		Size: 4.1 MB (4121361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460b73a43c64bc4cdf7ab5361c934dc56bdd8e1e50659e7f83034482165085ab`  
		Last Modified: Wed, 22 Apr 2026 02:32:50 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
