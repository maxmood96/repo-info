## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:0ab54c387ca31bb220421df21936afcec9521b23accfc95338594d5eb380f343
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af6a50941cfc5c1606c3d105484f8a10b89c11e5395ec997dcd1c1fc03dd0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142909972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588cb5fdac5c0ce11ce4ee586bd7ec6af5c2d97b37a09e153d6123003b08339c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b1598688dd5948f64dc955f58b0dcf5627fc6bbc5754f5ea08612c6d3bace8b`  
		Last Modified: Tue, 10 Jun 2025 23:26:12 GMT  
		Size: 49.3 MB (49263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cec2bdcd950987565d27e6bef170159a9fdde6f46531b0889933354046db48`  
		Last Modified: Wed, 11 Jun 2025 00:01:47 GMT  
		Size: 25.6 MB (25603931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbea8bacad06666c3210aff4437aaea1773f797c5f0e58c28f9f9d0f3ca5ec62`  
		Last Modified: Wed, 11 Jun 2025 00:02:53 GMT  
		Size: 68.0 MB (68042724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1aa4910882821580cca174be29b22c1c4f7a26dc99a64cbedc54e4eca50ba047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67ffa512f71cc660de1674877fe436b3fb2970312602c45a3442cba16501873`

```dockerfile
```

-	Layers:
	-	`sha256:627fba575cdebcc4ce0639ca315b43d5577658b643821b739c625f54e9e403b5`  
		Last Modified: Wed, 11 Jun 2025 04:20:59 GMT  
		Size: 7.8 MB (7776243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace33d7b9dfbc1b9df233a4f0b5f0ace0b0679e0eb2926aa8fad14bdaeeb671f`  
		Last Modified: Wed, 11 Jun 2025 04:21:00 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7e76a2ab3e9adb7c843aac72b39c46589fbef7b2a760689e003fd3e072100446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137404579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3332a4cd116ba5cf9cb8f699248025d6b805df274fb912d5bf77b66d2f9401f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085f136199cc5a804201375aeae18b933264b5486014fd2d2c46cfb68e131fc`  
		Last Modified: Wed, 11 Jun 2025 12:21:44 GMT  
		Size: 65.6 MB (65640755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:625a2db157df82c398b21c4202a1e0f9d6c8b6d6be358b3c4ac1c84f4ae6e460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7793883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0488e13d788ff8807b78f4ed2b0f945d1d2e9915636ad250937c9eec4cfdb84f`

```dockerfile
```

-	Layers:
	-	`sha256:174cf164fd718ed3d05dd43f5796b35ba27ece82e631b087165cfef849a97459`  
		Last Modified: Wed, 11 Jun 2025 07:20:30 GMT  
		Size: 7.8 MB (7786526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a731a60015a8e89e7008471aef30701ee6676227e23b2ef5f6b5b0fd36ff2f`  
		Last Modified: Wed, 11 Jun 2025 07:20:31 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f510d189a8f33ac19e025c00034d487fc255ae7dee12a54b672142942e6a30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132301853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb76d4658916a37a16ab4ea490ae51a2618be93721a2d113d24f85419e699f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Tue, 03 Jun 2025 18:04:06 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e723f972fd882067b040659dac6bf0007c9489588821ca8240ce91487131`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 23.6 MB (23589756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe087ac4a0ee4d60e25cc222cddf59cdeeee34ea48ec3d3c1cbcb898be35e05f`  
		Last Modified: Thu, 22 May 2025 12:13:22 GMT  
		Size: 63.0 MB (63013467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0166d0cd2c811767eb0ad1134f4b574d50682b1f04745d7b429553e39d1b8d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f26a854c9f4dc292bd97008aa0569f61327039c8263dc0eeef7cd09ea106e7`

```dockerfile
```

-	Layers:
	-	`sha256:065e605584416159f2fc4c4358494fcce434e62b258f17768c7b29e241c1a848`  
		Last Modified: Wed, 11 Jun 2025 01:21:07 GMT  
		Size: 7.6 MB (7609459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b30748f5568ff42310898e9e89b34927258a81d8898712f210bb7d5e3b0ff4`  
		Last Modified: Wed, 11 Jun 2025 01:21:07 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e8c4c57e97dc298cb153c1f204d4691fd87feec64dc58235a404cbd72003a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142462796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b345fc5ca5dbbd59438cdf2e932f849f518cedf2dc5f424812e67a2dbfdd9149`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b158d051d6fdc917c4a2f2c9c640867150d5c68a1439dd536c0ff065f9eab`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 25.0 MB (24976033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec4c1b10ede551eb1553f94290e8793e9558296a1221a501ace332d77dd68f`  
		Last Modified: Thu, 22 May 2025 09:19:21 GMT  
		Size: 67.9 MB (67868897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eca18f587229db145ab108015d645db11995e15424e548c75c7cfffce03821d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7624000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd1db5e004d13d59c4fb62de6622e8d7e0fa511cb65583c053259fdc565d394`

```dockerfile
```

-	Layers:
	-	`sha256:e9e391400913c52ccc8003d12c486b768f850d01d872b3e59e59e191b345e319`  
		Last Modified: Wed, 11 Jun 2025 01:21:15 GMT  
		Size: 7.6 MB (7616623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f9e8a01667d942810139ecc66ee9008ba09373546541edff6d2860f0ea7b98`  
		Last Modified: Wed, 11 Jun 2025 01:21:16 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4da97911ba7d4e39aaa9ac5e5efc03e6de300e12a5482654ec8b071378628292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147680199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7822ec7444554aed38f213ccb2e82388be6ace88a3102de9c407759ef93a125a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a1a02b91b1c2266da4734f34b831bb020d740f7bfd0647d1828242b377de717`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 50.8 MB (50786017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c1899ec001f75529ee8cd455eb4a23c4b9c5414c63db7730474213c55437b`  
		Last Modified: Tue, 10 Jun 2025 23:36:16 GMT  
		Size: 26.8 MB (26759161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521cd224c201b94f36b1b9e6ba5db4b89c6a8f696946eeacb5bc6b1ac6ed6f5a`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 70.1 MB (70135021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73be5d884aaa2959427a7e1072b12a78becbbdbe0d0cbe4944c73094a7fe1ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a5eed419dbd2d3ef98df812d9b24c913d5954f120cd5739b6edb3fec772dc`

```dockerfile
```

-	Layers:
	-	`sha256:770fa87e6b934d3398496d1de1c914944905391583fc6e4b68c049b055f8780c`  
		Last Modified: Wed, 11 Jun 2025 01:21:22 GMT  
		Size: 7.8 MB (7772390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cab14eb66433755b8897dfbc7a585872e4e3082eae6459a8930aeeffa701bb`  
		Last Modified: Wed, 11 Jun 2025 01:21:23 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2f0ade1a3c737c4a418fe4c4c4d42d95c3395d5edd36bde3cff430e279cf512a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142202492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca02cc398ad57eb241273c0d6f9ca3fd35da2cf378950ad1090a54c19a6f332a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:27b34307efc56192fd4ca945f6323e2158a324121ac08b2b6be4739d1a7a2345`  
		Last Modified: Tue, 10 Jun 2025 08:48:47 GMT  
		Size: 49.5 MB (49538322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff848add2d23cbb649ad48161ea5c02c3695dbc152c477b6b7b6ddde8893826a`  
		Last Modified: Thu, 22 May 2025 06:18:44 GMT  
		Size: 25.6 MB (25629837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0328e102aaf6d1ba040810e1f44f2d4a53bb52688eaba926e1237110a438c0e2`  
		Last Modified: Thu, 22 May 2025 14:32:23 GMT  
		Size: 67.0 MB (67034333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c31373d458ff6f23241b2591706760b33ee670856b9b4fadaa599567402d5294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdabf9e3db80c49a07c9926acee9f49eb869f8ddb6c50537e177c64770b751`

```dockerfile
```

-	Layers:
	-	`sha256:5e3f0a41f6bd88e410ffb0825599aff5f628f91164033fe17451a028fdd4152f`  
		Last Modified: Wed, 11 Jun 2025 01:21:29 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8cf09f59cd9521e2a6bbe7c0d398527d507314b8476fcf1cf60b263e8ee8986f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153435791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50f3d82d43ca6a3b114490ec9b1d03088d667df488c72022b7d944e477fa4c1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16f5e7cd9c9945be6c34f81a399d644f442eadb5c4f47f89a090f84971e9d67c`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 53.1 MB (53087015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d194009a872a9d9be939ab0b551a2fd792af6fbbec9e72310f90b49fa15b755`  
		Last Modified: Thu, 22 May 2025 07:32:11 GMT  
		Size: 27.0 MB (26967476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af6197342ea5f5e1fdaed350b46564c26eed8ea834f6255283150c0e746ab8`  
		Last Modified: Thu, 22 May 2025 12:41:13 GMT  
		Size: 73.4 MB (73381300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d3edb5e419950f244a218607e033074dbaf3b1f7a914057217ab9b0d22bc717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbf866b387f8f8054b7660094466ec0476fb12b206247b71f9de791de3e14f2`

```dockerfile
```

-	Layers:
	-	`sha256:44ec5ca1bd53c934dd31a5ceb1d83a0c43a000e3d59401cf8afca2960c9e2044`  
		Last Modified: Wed, 11 Jun 2025 01:21:35 GMT  
		Size: 7.6 MB (7622437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f2bca606668f5a1bea56afcc42eab166a62eea54312e28867a32c5b1194df7`  
		Last Modified: Wed, 11 Jun 2025 01:21:37 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b3df35c212eb327805801f1cb5fbb0583a28b36fbc27cb48022a17955cf0f931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139675924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38df2eb066c6eabfd808fcae02b5a5dd60214b63d70e236191512be0f93aff23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0009e91f3f8c4153a02b39dc6e9b3c5a36cc3c8e1a157d73e8f9e91097515059`  
		Last Modified: Wed, 11 Jun 2025 02:03:30 GMT  
		Size: 47.7 MB (47749671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df49454d4e709bab7fd6d2461b736d24ce3db865904adb84e1af7a3e0716ace`  
		Last Modified: Tue, 10 Jun 2025 23:34:49 GMT  
		Size: 24.9 MB (24939799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d5419b50e53679e06a4b73e768cb2cd1c6fce73cac408ba77b0431e99651ce`  
		Last Modified: Wed, 11 Jun 2025 11:59:20 GMT  
		Size: 67.0 MB (66986454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13152d5e9f5b06e7cbf399aca691342ac96aab2f2762cce84dc2c6f6771df1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891c1b4d6ab7c75892f8c0a954fa53dbb2e79ccfa630418565b6efbc15f62e01`

```dockerfile
```

-	Layers:
	-	`sha256:869bf10b7b7bb91caa75f268c11308a51d4ae46dda938da8f513a8ac7ecf2675`  
		Last Modified: Wed, 11 Jun 2025 13:21:11 GMT  
		Size: 7.8 MB (7766059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2fb699ad45851b0fc32af2e6778cb5768d8f0a1e094d0dfbc8e31905108566`  
		Last Modified: Wed, 11 Jun 2025 13:21:12 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c293ffb9b5b24aef4938abd4885ba2ba9e2f6da430c5814905c41195205aa15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144801421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8e8179fdc2fd23d77f50bc13033a5be291ee18a60712acf385c1258dec97d4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc44cd2b9aa97b3fbb56995ed62a657167162e1278b818c7bc6bd60f13d1e12`  
		Last Modified: Wed, 11 Jun 2025 07:20:39 GMT  
		Size: 68.7 MB (68689048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52b93c5ebe2451a2cc87dff75a7cef376de6933d492208b7a6700656686611bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb2182c6381249391b53a79cc33c435907a5c53171561f8c71a595990551337`

```dockerfile
```

-	Layers:
	-	`sha256:420baad8ae06e11a3b53d019d6555225c352251ccf0cb6ba267eb8a9ae0fb4fd`  
		Last Modified: Wed, 11 Jun 2025 10:20:47 GMT  
		Size: 7.8 MB (7767538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86234c91b0e0ca8f244dbaa838cb2bf82282a4a04bc299e3d47ebd138f37a9d1`  
		Last Modified: Wed, 11 Jun 2025 10:20:48 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
