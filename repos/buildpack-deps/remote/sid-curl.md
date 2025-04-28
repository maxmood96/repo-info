## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:cae4cd3a695b5f9ff92bcfbb413e7248743083a6b0eb44d7e381b0daeaf9793d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1edc3c13d07945e7f48e3751699c3787ba7311cf2e73194b401c1852592f390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74241363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4749af358deb69d2559ebfa9dc7d95ed096464a8caa7d607943289795d2dbe96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2aa53e779a14a678b6be0553334055853528ebc9774eaa3e69e5fd71326114f8`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 49.0 MB (48967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505e1c0337e142d28ab6c58fa7e5bf319287c629af695b520d6eb278c386eca`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 25.3 MB (25273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d5b0670b6f2ea040e8bf3d615384c2ee3e09e7d4ecc2823c17322ed859d3539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c36c5886035f02fe6b1a812b79bdf09beabb6b6fd5d52fdc26514fc4a9f38a4`

```dockerfile
```

-	Layers:
	-	`sha256:ccaf6a3ed903ed7e66d3c0e65224304271aad99b34b7d740d00c80d5daaa44a0`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 4.0 MB (3978433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e30698ce4837d1320f9694ffbb7e1fce558dde1c98c371f517a2ba0ff33478`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4e91d128c022b7ee0f5c1fc16dd71ae435ed867a69269cff4088e1d33a7df3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ef32fb65c8593c198c538f9ca5cc4fe457a2504bad47b949fddc48bf55258`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a67f90f752f0b4c3cbc55e5cc36457c9464d60f34b4c1a8cb2a06c06cfda363`  
		Last Modified: Tue, 08 Apr 2025 00:23:29 GMT  
		Size: 47.2 MB (47203396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a07c09d53242d965ab755e1358498dc94eabdef8c99be65a21d5b9eea16d2`  
		Last Modified: Tue, 08 Apr 2025 05:12:45 GMT  
		Size: 24.0 MB (24031511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c20d47cc6b4ef2c0086f8d4ea61a2a74cab13484d79308d5fcfc2233f35904c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f990610742d47eba0ca8a8066ce61d0cf5bb22f2c794b7b83de4e80abb52fe2`

```dockerfile
```

-	Layers:
	-	`sha256:d2f235485447ac57abb1c497da654043b43a249f669d9f588cecf076617108c4`  
		Last Modified: Tue, 08 Apr 2025 05:12:44 GMT  
		Size: 4.0 MB (3987340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a9bc928908757bf1f8f9d0ebc4103a1cfb6163807a3ca3fcd102a06268d347`  
		Last Modified: Tue, 08 Apr 2025 05:12:43 GMT  
		Size: 6.9 KB (6862 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76ae97d301ca7e88e885efdd6a8cc5da54624f9c40b6fce0b71aea25d4801a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68763268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029cc42fc82402d99e71902929bad71ba8a06934b494dfa1b8de6ee3bdacd31c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9e1d1d502e5470a18b1778621dae87bc08126015f4514c8d42f4923e5bbe3526`  
		Last Modified: Tue, 08 Apr 2025 00:24:51 GMT  
		Size: 45.5 MB (45459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef4244a5aaa0829da0ede8fd328ccc49be5178ede43a05010a5169a12ac0dc`  
		Last Modified: Tue, 08 Apr 2025 07:39:15 GMT  
		Size: 23.3 MB (23303278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e62042cc8d0f9bfd3016b7b3a449964eb184e607a691f233491687f4751f673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7716f31361fe6b52d6ed19922f441733052c09504dc58b8c3802a334061bd5`

```dockerfile
```

-	Layers:
	-	`sha256:b65c631bccc0a488de210144b325a88087be520676704cf6626253fa3c35bdc2`  
		Last Modified: Tue, 08 Apr 2025 07:39:14 GMT  
		Size: 4.0 MB (3979932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25d06e3ede80c575929419b509caa51e94c5292d34c8c4752239dc96756f9f8`  
		Last Modified: Tue, 08 Apr 2025 07:39:14 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b688bb6cae20aa6f6978e1846dbf08f21914a537e3a9648eea2c93a91c817198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74024895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa4cb4158a2332f87390a9a8349b6a1897d94b808a1a31198811d288205478f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:09d775ffe2e3a261e25d75c66999fe50b8109b656ae312ea92d80a3277b69b88`  
		Last Modified: Tue, 08 Apr 2025 00:24:23 GMT  
		Size: 49.4 MB (49356840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26d5bca0f15f13ec1e165536514cafcf57ff3d2c87ab2850f356915ddeb3aa`  
		Last Modified: Tue, 08 Apr 2025 06:04:11 GMT  
		Size: 24.7 MB (24668055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8643e100c201cdd7e42e25e53f7b7fb29823a7cdb1f0e4fd73b49b746b9e08a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896bdd1f5d5e25e358ffa124c88dc95902edaa53d18bb5c3b3eb26d2d5e5e551`

```dockerfile
```

-	Layers:
	-	`sha256:0c955ab3c7264101be31070cea90b1ed289569944ecdac7dd61cd00b48cf058f`  
		Last Modified: Tue, 08 Apr 2025 06:04:11 GMT  
		Size: 4.0 MB (3979965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1f776e201c2571cbc92af2a89969e654d9afedc36ea36c389596949bf00c3b`  
		Last Modified: Tue, 08 Apr 2025 06:04:10 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f1de232033fe84f3e55e6accd8a15b5ad6e281162673dc3286bcdb085af03cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143bcfc3e9f9ca21ebcf55c4388bb0bcaaec0ca42dca8fc6cd6efbb5d4b68b89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f72acca1637ca2dd8a6d7b3e16eba9907e862c2052b181ab848453b963bf8836`  
		Last Modified: Mon, 28 Apr 2025 21:08:12 GMT  
		Size: 50.7 MB (50745529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c1f129fec1b0fb6b1af41a0589e5dacc9adddd0abb3826af4edb56b312c90b`  
		Last Modified: Mon, 28 Apr 2025 21:54:04 GMT  
		Size: 26.6 MB (26570218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8893d266103debc8e91708397ee165b1fcb9598d054c081f193374cc8a5c6eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1963f0a0b73dca4a57d96b72b01af7e426a5d4830de0023e640c71be26b8b59e`

```dockerfile
```

-	Layers:
	-	`sha256:cb386e9cf134120b9e253e860d320afcd1067948b2ef485801997b2c63e093fc`  
		Last Modified: Mon, 28 Apr 2025 21:54:03 GMT  
		Size: 4.0 MB (3965909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e688426533b87a66176bb6049b1992e7e406f35ac0248d14345c156c5519728`  
		Last Modified: Mon, 28 Apr 2025 21:54:03 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:226810cc5ee58f1f11b70b59313115c299bd1912c5f53c7d7c54ffbedc2c2ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74610237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d14ce9f991633960ef80a53160bc54dc0def287525b1b723be1c23afa5ca16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e47ff6f8c72dd6db533d94619301df4fe359af27c4bdf16e11f5c32ee9c26e9`  
		Last Modified: Tue, 08 Apr 2025 00:23:50 GMT  
		Size: 49.3 MB (49276857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e51d673a637240b96d7c17ea9519652624afebf48f4c69f85cde5bf9564505c`  
		Last Modified: Tue, 08 Apr 2025 16:33:23 GMT  
		Size: 25.3 MB (25333380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13e9ea55ef6dee97ab83f267d5ab033d6b3a46ce59666c092306f886f8d7e3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfe560259d3662ff63d11eb43a176ab85ee589d59adead40b61bbf4afbdf243`

```dockerfile
```

-	Layers:
	-	`sha256:e59233e640fe77851bae635f7becffff67979e70b35ee4010e475eeadd8d4fe2`  
		Last Modified: Tue, 08 Apr 2025 16:33:21 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9473808c73cf0aee03c8f2e4f91b9bec8a04ee8db67d1aea13fb42ea7236f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79421983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8022627cc153b4ea6e230bc8d809eb0077d9f64c3bd0ffadb7c22a7f0eb6ca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:24038d07494a40a6e0f9bb4cfa800b5c396d2199d38fdbd9a4d93a09f5534ac0`  
		Last Modified: Tue, 08 Apr 2025 00:24:22 GMT  
		Size: 52.8 MB (52784300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db81c823da47f6b320f39ca946071003941c644715aa03b5cfb4494f3617d2b`  
		Last Modified: Tue, 08 Apr 2025 04:31:07 GMT  
		Size: 26.6 MB (26637683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1af2c1d7caa5e74bd78707acf7c736d191b5aafa9cffa204b1e7f4a7aa6eb732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e3e7603052f7b994623674d9eaed32e25c3b87fd5b755755f4d1fcdf8a3b35`

```dockerfile
```

-	Layers:
	-	`sha256:cfd40ac0d09127acca3048acb2aeded8472cd2f9db5aa6e56d2f71761a5bdfcf`  
		Last Modified: Tue, 08 Apr 2025 04:31:06 GMT  
		Size: 4.0 MB (3988346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e3af8d26f54eedfe57d6f626f2dab80e0b7a304c2d88dc6f71d5a9f7ea0ea4`  
		Last Modified: Tue, 08 Apr 2025 04:31:06 GMT  
		Size: 6.8 KB (6834 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c1bcdc1e8a3f78cae50d6998c73334677ca33293c03e0dcf68946d213ac5774a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72627229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605972011265b42e8eee8e790bf098638a1d6ef758ba6ae09742448c33f2e26`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:974932b0d4f6a2a6986aebb6971e9388758bb668ea9d86ad8d2fa557cb4fc4d8`  
		Last Modified: Mon, 28 Apr 2025 21:09:48 GMT  
		Size: 47.7 MB (47731445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66e85f6895b6c676e8788d49a505ba553dd35816b89660f34e2ff2455d80e6`  
		Last Modified: Mon, 28 Apr 2025 21:53:00 GMT  
		Size: 24.9 MB (24895784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:464dfca8d6ff360a0917bf5abf554df6f43b11903ec16c6334100e345a03a9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df1cd0fcc6090bf5ea7849115098d1410cddf34c63e1e08d2c3059e1204137`

```dockerfile
```

-	Layers:
	-	`sha256:5f6ad04569bad263598b87a8ac080fefc5b85d89e384c0deabd5de7b69044ffc`  
		Last Modified: Mon, 28 Apr 2025 21:52:57 GMT  
		Size: 4.0 MB (3961483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e2b4e00b3418b1a630b74d5e90ab97950375449e1909c238c33e987bd26e09`  
		Last Modified: Mon, 28 Apr 2025 21:52:56 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33b23bab04106e23161204a3311ed81600e2bc7d55a2c4d1de07f0af6153d603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75507631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d69f1cff51a744ed05918ee35d6a5c969de0dae4e7968233a7f02cdd3aab6a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4724dabe4aa05329c356a033beb752bf4d3d8e15762c4c9025e18f8b74f6a65`  
		Last Modified: Tue, 08 Apr 2025 00:24:40 GMT  
		Size: 49.0 MB (49047465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d32a5e527bdaaef0ef8d058290901aa64df97cc259e7f2fd2e845c51227b`  
		Last Modified: Tue, 08 Apr 2025 03:45:05 GMT  
		Size: 26.5 MB (26460166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2856b0f32493e95349154b2d89a3a01c96d1fbfcc4a2bf0525b4e631b9fe0743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9679e829b8c0e580620cd2db8b2b5daf6624746ed25063a3fe251d25b133f9`

```dockerfile
```

-	Layers:
	-	`sha256:3cc60fcac6da30b40c43c868cb77f40e4bf3edbed51a39a07f727cdfb21a97b3`  
		Last Modified: Tue, 08 Apr 2025 03:45:04 GMT  
		Size: 4.0 MB (3986048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bd30a8baee6be9cc435f687208a0e2ba6f1f7157f39731326dc009deb3e309`  
		Last Modified: Tue, 08 Apr 2025 03:45:04 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
