## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c3b1e2cc69a0c3bf9405bad6517555de0ae1ab532e627ca712459c934f1cc49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c573a4358c9ca312a8dc933ddeec1a8a926bfa4a3fdf2701884194a699684fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124267191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b947e8a66d95c9df647185039f8cebb9dc87cffcb5256163a546704161fa3cd2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41b7c94298d0ef0ea6701e44b67b9033aae60426ad4b5bd6972386401abd8079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7717501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf0f453e5bcf19f9f171cbeb9750f28eb82216a6629c46fe964af78c9f49cc9`

```dockerfile
```

-	Layers:
	-	`sha256:68212d0ece93d0535489e5f2587ba3c84560c410446399f2b8d78ba930c2191a`  
		Last Modified: Tue, 08 Apr 2025 02:13:51 GMT  
		Size: 7.7 MB (7710148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7f12a3245297b520cda5e49e4c872869a89a1ea33e509273e71ec45b23e08e`  
		Last Modified: Tue, 08 Apr 2025 02:13:51 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:10e160a2eb0a598ff915afbf442a63a6f15cd0eb86ecbed306258c7d18d6c8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114340798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ad997df4877b7df4accab549c62377b24a1248240a97106692b881b09584c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4b30558451369a042a41509e315b4af7bd6c5943c1b09d29728aa44a76085055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e54ca69d57410aa74b8c1aca0d2f60c77294d27773f85f62bed3c796932cef`

```dockerfile
```

-	Layers:
	-	`sha256:b78426ab7d42bf3b5e9816c311a81fc89a56c9c51738973b044c229460e106c9`  
		Last Modified: Tue, 18 Mar 2025 15:29:12 GMT  
		Size: 7.7 MB (7709588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f9eb1ad504ac11b040e08db2d363b5b5033ef7a264fd77d27bb2f6b6ec07e5`  
		Last Modified: Tue, 18 Mar 2025 15:29:11 GMT  
		Size: 7.4 KB (7411 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:90a79f6f2a751ae8b2315e716f3828ba1ad180148c580f17927fe5909c549aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122853317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b56b4bcde03d08a17d65621355470cb9d4dfc5d893199e281f2dac9e94e4b5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da1e6ea956c4d1ae53505da4ccb571eadb5c4678c979b7d0ca96e4ff01d5c36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7723315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42df8661e7343868a88f667be7c264772fe0cf0006e747edded938733763525b`

```dockerfile
```

-	Layers:
	-	`sha256:1db9eac15b89a36b454fcbb31302cb2cc00a67417c8d578a27f05a4894d47386`  
		Last Modified: Tue, 08 Apr 2025 12:18:41 GMT  
		Size: 7.7 MB (7715882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8338bcce7f2b41c54270ef37c6ba3e877bd811964940388c541b3346296a3c6b`  
		Last Modified: Tue, 08 Apr 2025 12:18:40 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ed999fd62bbd35c47cf89bbe8b7354bbb26d827a798eeec1049b69299caf2d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126998719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c382b7c19416d52b78d5cd12e35948fc143282fad4c1e4e5df876d4bb174f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f5629cd0ed8c5aa790d72e7673ec1ca6fb24467af246a9d4b9b89fba38ed5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7712969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd04f53ba860a7e15b438e986b585f4cad9dec226f9a5c0ef0420a40cae4e014`

```dockerfile
```

-	Layers:
	-	`sha256:ea7959e4818a3a6607d11ee58bc3dd69c6ce4ef9147189bd9ec79294314e2a40`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 7.7 MB (7705638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc5c04d774482495d29ad9c47690e4264b36de3368fe805116edd04a6dc8082`  
		Last Modified: Tue, 08 Apr 2025 02:13:57 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
