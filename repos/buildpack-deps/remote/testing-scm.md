## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:5588d884c388b60bc4c7ad5d549335187bd3499ab9a35a3a5271c429d9557cae
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8e41f63471f373bfe55eafb9bd8706dabc6d65a65fe1b0314d63979a3cc1b82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143024009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160403e70976f11c21e8d1b76055af3b6efcc967dca95caf7df4b0cddbe388b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2da15d6ab4eca366627e054ac705fca48595c86940e1079388acd7fb2c8df21`  
		Last Modified: Tue, 12 Aug 2025 20:44:42 GMT  
		Size: 49.3 MB (49278278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b32c67f37fb1bae3e7791507a85c187bf40f5edf279234d1f8dd1817c91a868`  
		Last Modified: Tue, 12 Aug 2025 23:13:57 GMT  
		Size: 25.6 MB (25605315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb8ff535bf3612f283d47d0567ab7abafdb832c9725b38e843240b2717fbd`  
		Last Modified: Tue, 12 Aug 2025 23:35:40 GMT  
		Size: 68.1 MB (68140416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e5cae3464d6033d9803c7501eb7c55265d3c2e13d8a62e6b304a85402859d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d6fbfad19b621a3e2193213a6de5974e2e239d3eb06f03c966998794321486`

```dockerfile
```

-	Layers:
	-	`sha256:21375c8d206cfc635216b824e3450c10f9cabb431d52b27813d4d6f697184f23`  
		Last Modified: Wed, 13 Aug 2025 01:21:05 GMT  
		Size: 7.8 MB (7784315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9cbe8e9f1ba34ace4b8f74da0153af7aaf4cfe3b5c90a6049a9129abff30a7`  
		Last Modified: Wed, 13 Aug 2025 01:21:06 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:af6ebe611f5fbcee7951499c74e1a31e48034440774f6f6f94c11e4ddd6566fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137503656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1b0e1c1fa11bf3538c16450237718a2376ed35be87a9bdddd0c5d22550ad9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2fa5a98b9608d692994d9abcc2a7007473cf39d4da546665901804b35bd8b320`  
		Last Modified: Tue, 12 Aug 2025 20:45:48 GMT  
		Size: 47.4 MB (47442421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e8c08416a0595c07b904b87179f903faee6f0a25e5b00b485a3c0b0df46b2f`  
		Last Modified: Wed, 13 Aug 2025 06:07:53 GMT  
		Size: 24.3 MB (24331053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1486224fc8f64dbe0bf66d7516691f5822dfff3ac064ce9811427c63fb10b9c`  
		Last Modified: Wed, 13 Aug 2025 12:58:51 GMT  
		Size: 65.7 MB (65730182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7137ba4009554b3d5ebb2ed564caf211e6341decc438fdbb36df2315271aaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7792714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a3c4ef16134803e8888b0a147bd95bb390de3ee3d03614b70c0212e5e4c136`

```dockerfile
```

-	Layers:
	-	`sha256:4facd1841168d33585393bb5643c5f32c58eecbb5dc4da7a17ab680fbf738ac8`  
		Last Modified: Wed, 13 Aug 2025 13:20:29 GMT  
		Size: 7.8 MB (7785345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac02902fcedfd89daead6a33872601e129df2acaaeea2286fd4c6f3607c640d0`  
		Last Modified: Wed, 13 Aug 2025 13:20:30 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e57bc056ec79c39b7ee29a5b4ba5ed0008231be7b33a54a553b41fe6c752b23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132453904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5353b1a3445b3bfa76531eaa82323087e6b59566a165da21776840c5b552c7fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebefa9d9514d88e860c22acef070a7914aeebb2faf205f156980b98aae6239b`  
		Last Modified: Tue, 12 Aug 2025 20:47:38 GMT  
		Size: 45.7 MB (45712626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e92b397025ea1962fe06ac411410e1176db804c6ecdee14d21141a79f11c0`  
		Last Modified: Wed, 13 Aug 2025 17:21:05 GMT  
		Size: 23.6 MB (23605493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967cbb10d571d2d7a67996c18368f0902c78e7191a91127a26dd33377934be7`  
		Last Modified: Wed, 13 Aug 2025 18:16:13 GMT  
		Size: 63.1 MB (63135785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9c2ca24f27559453fe8c75839af60ac730999bf662076670fe171dfe9b45403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7792183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d883aa11c22e091c7e36241f36993b697de74a5b8faae7816c01cc94ed69370f`

```dockerfile
```

-	Layers:
	-	`sha256:28c1b4dee9c1dda88baa44f6abd5b4247c7e0c43b38c2375a675f526829c21b6`  
		Last Modified: Wed, 13 Aug 2025 13:20:37 GMT  
		Size: 7.8 MB (7784814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7f0c296e55ba8f253b7389148369a5c6659bda511c7575cd41cf00cc37e2c2`  
		Last Modified: Wed, 13 Aug 2025 13:20:38 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c773c963669c948c61b5ede8c995b5a5ca26e5b2f0c3d8954df92a34c4e72610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142612054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bad1dbfb9561c70f885566f06e9dcd1294ff7814f572271c179c1a55a866fcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:273757ec3c30b589868c996d06fc6679616be5750d77150b4ff9e1c76d62fc59`  
		Last Modified: Tue, 12 Aug 2025 22:09:33 GMT  
		Size: 49.6 MB (49641601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061b8abd2163f95be76efedd7a660366135f0445c2148195b2efc5c8b4e4520`  
		Last Modified: Thu, 14 Aug 2025 12:01:20 GMT  
		Size: 25.0 MB (25006552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2b605603692665647b54ba968c38451a923c1631c8391126b72c47d167dd3`  
		Last Modified: Thu, 14 Aug 2025 12:01:25 GMT  
		Size: 68.0 MB (67963901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9746160fcd36562d8655f4d0fd43ecf6097ef4eb77b58332ee910537ac9fc634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7799365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bcbef7375a215aed8ca5c9e75b6ac09b6d63a708a8c0a8ccf7cba18dcc0386`

```dockerfile
```

-	Layers:
	-	`sha256:f61e6a5ff5e8165627fbdaeec256dbee4e53debc9a7597ec3f0b2ca99f68a795`  
		Last Modified: Wed, 13 Aug 2025 16:20:21 GMT  
		Size: 7.8 MB (7791978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49684c8142147e68ede1abd3cbe5874ab9bd0e8c23d7d48c2b5b285be916bdf9`  
		Last Modified: Wed, 13 Aug 2025 16:20:22 GMT  
		Size: 7.4 KB (7387 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:23957de794c9ba4bc9be71bd80ac6d95dc91da0883230650c95821f5326e27a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147782615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b29b001ce2c28c76339e1d496afaf210df2033ea737b94281880b97217632b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a7661e4f52ad2bea3934eba54982654dfac7e7138172dda967b99622aa0bbc62`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 50.8 MB (50794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6bb2de85bab19d6809a38d4ff9a79ceb4e077f6d30db2f012711f90b937292`  
		Last Modified: Tue, 12 Aug 2025 23:14:35 GMT  
		Size: 26.8 MB (26764943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee9012b9d2c3341f95663e5bf25ecf833321cd039d9290e49577f2d383f385c`  
		Last Modified: Tue, 12 Aug 2025 23:35:11 GMT  
		Size: 70.2 MB (70223418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16563007359b1c4ca5255f428bd401f6b07776dcd1781e6339f9a3556bdcc533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7787742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099e840581966561348cb2402b61423cf8b85d7337744107ef2d3226e139c50`

```dockerfile
```

-	Layers:
	-	`sha256:7883ff43cf693daf39fb18f70f07c8e6e83ab6dcda36848011f7a6369d476b8c`  
		Last Modified: Wed, 13 Aug 2025 01:21:14 GMT  
		Size: 7.8 MB (7780455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f358e5de3712fa016eb5877ee874b2d5e8d758de509a7c5055ddafcb357f04`  
		Last Modified: Wed, 13 Aug 2025 01:21:15 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7c8d27d873af2d0ee698b002feb9172e1fe256d2509f043f28e8836de214f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153556741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b7d6198edb76a47b7b0e404c52dfd36abc407199d62a62cdcc3c9da44fec7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7a7f44f45faa95497b08557d13fcde72165c528469e03cbf308c4f4631f2dd`  
		Last Modified: Tue, 12 Aug 2025 23:06:59 GMT  
		Size: 53.1 MB (53103377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840e735c8e0187da0a3a1c46a694c6d194b251001f4a96704e0ac845ec18ebe3`  
		Last Modified: Wed, 13 Aug 2025 12:13:41 GMT  
		Size: 27.0 MB (26986919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f0a22fc2b7b0872f52cfeaf5aaae68c408642a3206537713bb64955507caec`  
		Last Modified: Thu, 14 Aug 2025 12:01:53 GMT  
		Size: 73.5 MB (73466445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:33a9e2f90dba513f254461ab53a4cbb4588f974c3bb72ca6abd7c602b8ac13d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7798773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430c82e7ab4de80b65855f8dc787cd7f923d2d584dea9b9f26dd9566eaed40d8`

```dockerfile
```

-	Layers:
	-	`sha256:b10bcf8541109bfbde2b940401d8a7d6f760d96d1528a032bb271c7e9f0140f0`  
		Last Modified: Wed, 13 Aug 2025 22:20:24 GMT  
		Size: 7.8 MB (7791432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1050a8b1d065cf92e6747c1a4ce83bc2ae312d538c2257461161102288a9cdb`  
		Last Modified: Wed, 13 Aug 2025 22:20:25 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2440ae4d8454531653027fa5bfbe2cc323734664aca64489ac64daa6b030a768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139806656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c33f384532e8fc2abe2452b598ab7f4c83eb724cb9b861da8b4b9ef7afaccc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18eac9f463d6a4f3c60a520935227506dbdb88fbd69eb2d7f1db2b18bab3b76f`  
		Last Modified: Wed, 13 Aug 2025 00:59:52 GMT  
		Size: 47.8 MB (47764299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40195d2e04aeb657d27babb7b990135b099dce2244de1f5f044377d8fb07f57a`  
		Last Modified: Thu, 14 Aug 2025 14:40:45 GMT  
		Size: 24.9 MB (24943412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7119e17d753e3bb840f4a76a177110ecbea100d2e7b7d1921aa4515d0cee3381`  
		Last Modified: Sun, 17 Aug 2025 07:36:43 GMT  
		Size: 67.1 MB (67098945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0eceecdcf19f6741b8a9e71e8d75e8e06035c6220be1409bf550d7c921f0a510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7780672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4bdfbc49b0fe5d3d696e2f80f8779799e93ea9f22befdb1e2a53054383aef`

```dockerfile
```

-	Layers:
	-	`sha256:75b11010ad8c66833609d090df56bef2929c694282567a322d0b13326fb33ff7`  
		Last Modified: Sun, 17 Aug 2025 10:20:09 GMT  
		Size: 7.8 MB (7773331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88137d4954b6f68ad24402ad7433e4b582294d0473c457811a2ebb4033909ef1`  
		Last Modified: Sun, 17 Aug 2025 10:20:09 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4ab576cc73b1750ec93fe4fea952fd61c83b2d07dda064c61b80f9b935f6c828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145166408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d4728a072b806564d1e0be0f9ff822c752aed355a4998509b8d6c48be853ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:737129d56eecb9e531486098db9ca11053ee0c83738b761209455c817b0cc095`  
		Last Modified: Tue, 12 Aug 2025 20:53:59 GMT  
		Size: 49.3 MB (49345157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788bc8e33ee7a99a1a339be1f8a021249410c7933d3ffbff46b2196b2aeb3d7a`  
		Last Modified: Wed, 13 Aug 2025 11:11:36 GMT  
		Size: 26.8 MB (26771668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efa37d0c7666ac39e6f0ed83896f1e13ab06ca2c907f41a30b77846a3633dbc`  
		Last Modified: Wed, 13 Aug 2025 17:37:02 GMT  
		Size: 69.0 MB (69049583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:31084dc8558413d4df0311fb123683ebe0be1f34bba4a98a6685b05aa79566b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7792537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c13e491446e8695363508d5b8012d1f432b86a1bb89789577115bfa88bce6b6`

```dockerfile
```

-	Layers:
	-	`sha256:353b15cffe21a085c54ecb187afc24b2bf6c9f4f65825d7127b53c122c08fa79`  
		Last Modified: Wed, 13 Aug 2025 16:20:39 GMT  
		Size: 7.8 MB (7785228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0681ed60638b973a24b1ee0f3fbc4f055611ec8d39414d929eb3483c7ceb1f4c`  
		Last Modified: Wed, 13 Aug 2025 16:20:40 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
