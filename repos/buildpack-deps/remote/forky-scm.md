## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:27a7f4e1e7cd8e688c430d04f7ae0e51c0e355d2f68da74ab8e15793863fc46a
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7a6d0ca59ef6b24360ebf1657d7a74d4531d009d69825345ac3a5f57714992c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143500898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4e3a25d041e77a74b40ac10c8eeaa035a2d50cf05fefae607617f5fb1bb8c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3cdde7daa1c8617934a7f6fc5999acbd8f13f45edd54e774f4a3af8f31fa8`  
		Last Modified: Mon, 08 Sep 2025 21:54:27 GMT  
		Size: 25.7 MB (25659714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c7415b1ab77e9af8efc826d62011c5a0c0c5ea052f4de5c46ff0ed4fc8b2b4`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 68.3 MB (68266149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb86ac1fff97f2efe18df046b93126f8d831a187304b7175812bc9dc0ada245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0597a6b2c78c6d81e27fb9ff0bb2ac8acf203c8cc19db17ff0bbffa4dd9990c`

```dockerfile
```

-	Layers:
	-	`sha256:75572272b55270563016f10171fc7f31f230dd8e278b0db5a39e2aade585b78a`  
		Last Modified: Tue, 09 Sep 2025 01:20:28 GMT  
		Size: 7.8 MB (7771008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effbe429d88d0a8b19093eae6be25bb4286fc6e4b4d09362dbda0672837f5b6c`  
		Last Modified: Tue, 09 Sep 2025 01:20:29 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v5

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

### `buildpack-deps:forky-scm` - unknown; unknown

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

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6965118dfeaba01a4b52100f206c8c72ad1513fe112a8e7b744a75be2f19572f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132820795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3e19f1a165fc0ac1bc607ebdd96e615c04abc4afc5a23cbb396ef7eb4cdbf0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86adee590a893d066c841440cd9d1bbc41753c40fc6a723dd85c4ca79b9b96`  
		Last Modified: Tue, 09 Sep 2025 03:20:59 GMT  
		Size: 23.7 MB (23664786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed6e10bf1b9316986fb492bbe0bac3e1cf59a04a08869527f7e66262ef8c0f1`  
		Last Modified: Tue, 09 Sep 2025 04:45:46 GMT  
		Size: 63.2 MB (63212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:416907b2cfff7c68d21d3f11eda3470eaac4f79e9901a5296fb1b3b8af1a223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb78783840cef248b119d9309081bc9f8380662ec394ca8f11cc13ac0b22818`

```dockerfile
```

-	Layers:
	-	`sha256:e33ffe92671e3b1f45903e45bdb25193f014356947df25072d6780d13b54c0ec`  
		Last Modified: Tue, 09 Sep 2025 04:20:42 GMT  
		Size: 7.8 MB (7771507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530085440479fdcdec639575d25f151c342492c06e9092f0964d60cefbae733e`  
		Last Modified: Tue, 09 Sep 2025 04:20:43 GMT  
		Size: 7.4 KB (7372 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:97e52ea478ad9828f8b1410a1270c0f4cf57f91b3cea4040499729d92f372f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142969742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea793885a27128a15d12d85c6d7ba293e375e06b785a7c93bb4d0bf9f5023ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ec7eb396047bfcd475c3064af0e813d0c880bc68b69e6192c860aa1172659`  
		Last Modified: Tue, 09 Sep 2025 01:25:47 GMT  
		Size: 25.1 MB (25079091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af77d2a7de68721cd0ac42531f98bd04847eafbed443a4058e3fef3d9fe456`  
		Last Modified: Tue, 09 Sep 2025 02:13:14 GMT  
		Size: 68.0 MB (68027155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4cbbc7c3cec00170a754235bdb480fb05c519743e1b59de16d713422047ad6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7786060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f81d131cb2c808cd20f39066f34c75196f53f68b6a139766587ba8bfbdb093`

```dockerfile
```

-	Layers:
	-	`sha256:100546f03752652ad0ff19c35dc7977749d7b1df2b01ec88fb6958f473b65a55`  
		Last Modified: Tue, 09 Sep 2025 04:20:50 GMT  
		Size: 7.8 MB (7778671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91277432f59739e8a9be99c96c39d880ae0155a9fbbe49a91f769600272ec5a6`  
		Last Modified: Tue, 09 Sep 2025 04:20:51 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:393afe471196ba546590e03eb0ed0903e51bf57a5b170cd70ceeffde6e122352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148202705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2638513be935e238b2c88841de9cf103e4092c35ae45a99b3f954f8b7e21130b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160456f8adc4b90f7d6b65b9febd09b29220d231ef5935250170717564dfc2ef`  
		Last Modified: Mon, 08 Sep 2025 21:54:42 GMT  
		Size: 26.8 MB (26824472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73639472e8dad9dfb716e8a6bbce77939664b0fab7a79dae0ea141902d199b`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 70.3 MB (70328423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08ca09b57ac54862efbc10b568822dc6be2db76d57430be3610fb23d0d04a32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ef298368bc9ec051080e4039fc033514c06f995e5f9123d479ac98bd165bb8`

```dockerfile
```

-	Layers:
	-	`sha256:6ed7e9b0a32440a40fe26825eb0e3a2d195fa6d5653bb1455d528b238be6fd86`  
		Last Modified: Mon, 08 Sep 2025 22:21:00 GMT  
		Size: 7.8 MB (7767155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecffee443e0c8b7f3047ef65e5770a03dff83ce28f03670f064897b3e1bf3d5e`  
		Last Modified: Mon, 08 Sep 2025 22:21:01 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

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

### `buildpack-deps:forky-scm` - unknown; unknown

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

### `buildpack-deps:forky-scm` - linux; riscv64

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

### `buildpack-deps:forky-scm` - unknown; unknown

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

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:45d155178d15af214067fea0cc7406a9212f55d837efeaccbeb7b76b2e78ebdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145569336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d90f73552e909c1f081980d3fd1fdb43d352039f6f648af927def9e2e14267`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d70c4639b1bb56ca2bfa88a8dedfb6d14d5f6a857613b672fef601229bcd766f`  
		Last Modified: Tue, 09 Sep 2025 10:20:05 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23441d4a53386d92d68dfd117aef1e221cdf7c5c29e7c8841eb200ce14f89465`  
		Last Modified: Tue, 09 Sep 2025 10:20:02 GMT  
		Size: 26.8 MB (26840296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aced33c6860e9f1fad4c8609ff123d675ddb56caf85a90370df68696f49dccdd`  
		Last Modified: Tue, 09 Sep 2025 11:45:43 GMT  
		Size: 69.1 MB (69145858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1927b6886baaa12d583c07bd3957b00d933c2a9d246f4c1d1e3a90836d6485d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9986f730a2ad22e08708fef6cbce2cbb7d3396893a9eaf9228340d08b65ff47`

```dockerfile
```

-	Layers:
	-	`sha256:0364b402dbe367d69623cf41e55bd900e4a84806ab76e0a42bfd38292c63612c`  
		Last Modified: Tue, 09 Sep 2025 13:20:15 GMT  
		Size: 7.8 MB (7771921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806df7b1cdbaeb23ac062593b7e336e924c4d42083c92db8eeabb9f97611074c`  
		Last Modified: Tue, 09 Sep 2025 13:20:16 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
