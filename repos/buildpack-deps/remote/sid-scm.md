## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:435c4fbe67ec45ab1b56d0681eb7f5f06d0e5c4b2158cd0d66036f0f4236b068
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0c38a7687f0674a661522164ba751c80c07b0d3a05e33519b9b3572cbd8304fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142855163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03397ff9a668d6d063b375f94b83f2a80bce9f3f02eb1a86e8126ce2c9bace81`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:21c8f2db1ca60de292da0e982c4bd4b81bfe468b8d652fac5b9003ceedf12013`  
		Last Modified: Tue, 03 Jun 2025 13:37:28 GMT  
		Size: 49.3 MB (49250549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d79457730a0db09039cff8714fa8c41f073c5bed3529b5417fcd2b8736c7b`  
		Last Modified: Tue, 03 Jun 2025 15:00:28 GMT  
		Size: 25.6 MB (25585150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcbbec8ebb5599a6f3f7c58410495e59f3b554270ce0b5227dc68965286c92`  
		Last Modified: Tue, 03 Jun 2025 17:25:55 GMT  
		Size: 68.0 MB (68019464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b01441eb4db94042507d117d31e48a5d1158db9844ac3266b7bdc58c9ec975e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12bc84bf88617e1158463ab8e1cc26c79c7b55d01dcf7a2a8476a068d19df1d`

```dockerfile
```

-	Layers:
	-	`sha256:dcb0dad4a2cd445171946de684fde5f130458145d7007dff8673c92e8e758a7b`  
		Last Modified: Wed, 21 May 2025 23:38:02 GMT  
		Size: 7.6 MB (7608960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20225d8abb4f0408d536a4f5194da5239c5ed7158d37e4745f2279d11b814b8`  
		Last Modified: Wed, 21 May 2025 23:38:01 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9f22d8178bf89590e4c828c5560dd75fdc57dd090dd0730ed8e0a5fea9c81ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137398498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace7de8079538aeac8c22a50ab988e388645435f236cc1314a4dbfc884f573f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f211461130ff11866a85e649352ceeb2f6ebc110118114f92b30349c5de358f`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 47.4 MB (47442893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390184f3e2aece3a9d3a8380bf315948d0d62ca40bd766f23543d583f330b82a`  
		Last Modified: Thu, 22 May 2025 01:14:31 GMT  
		Size: 24.3 MB (24323529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa73818847f3cc7d5638e8f2c0e6dbb5c84e00109279fe366152e8bc162b55cf`  
		Last Modified: Thu, 22 May 2025 04:45:28 GMT  
		Size: 65.6 MB (65632076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25fe6ba3387589d7ffdd3f2ab9910ade886e43f1b3b0783c868a79de043054c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dabfc20f5675119dde937d239a0f45f4d1abe3cd5ea0f455b990f1d2322de8a`

```dockerfile
```

-	Layers:
	-	`sha256:cc1c5b6c2f14a914a9e457cd302cd9b15eaa104163ed5c88d617e58be4fb9bf6`  
		Last Modified: Thu, 22 May 2025 04:45:26 GMT  
		Size: 7.6 MB (7616362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a8c80204407f0b487456733fb2907277c8325f7002fd80e8a7b1f133adecdeb`  
		Last Modified: Thu, 22 May 2025 04:45:25 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 12:13:20 GMT  
		Size: 7.6 MB (7609459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b30748f5568ff42310898e9e89b34927258a81d8898712f210bb7d5e3b0ff4`  
		Last Modified: Thu, 22 May 2025 12:13:20 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 09:19:19 GMT  
		Size: 7.6 MB (7616623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f9e8a01667d942810139ecc66ee9008ba09373546541edff6d2860f0ea7b98`  
		Last Modified: Thu, 22 May 2025 09:19:18 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:68202e463315b04dc6af3018bfa4c83f3ed5c8667c71883403e6836c4abff195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147626048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f690026ea5797ad50001f9e7ad1e6489f3586e437427ef1bf4e6d96edfae10e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c296d6dda96e0fb26dc4760b3366cec8a0723558334f5c902e1c373d0e43ab6`  
		Last Modified: Tue, 03 Jun 2025 18:04:13 GMT  
		Size: 50.8 MB (50760379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a77ccac61e5d039233fd2cf7db2ad5fed48827a001629e91bc009eff166aeb4`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 26.7 MB (26745468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61c02e4c2f4cf8b97da95199eb210e94faa26e3fbbf359e109faa57c15cbd38`  
		Last Modified: Wed, 21 May 2025 23:37:36 GMT  
		Size: 70.1 MB (70120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:020836850525fa9e7ef70dbd15860da647751141bcbd48927169c91ce36338ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec21a86c33d1434ca49b49bb8fdbd0b3a82d3106fb4db66d6a288f6d0e0777aa`

```dockerfile
```

-	Layers:
	-	`sha256:744cfbebb55a91f994617f111be4d2a9bedc02dbcac85edc98f3ab3751c51109`  
		Last Modified: Wed, 21 May 2025 23:37:34 GMT  
		Size: 7.6 MB (7605106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4328f8532189d7fee4f0cf4fab21f5be2b2f79bfc720c6ad196af1cbfe49a86`  
		Last Modified: Wed, 21 May 2025 23:37:34 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 14:32:17 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 12:41:08 GMT  
		Size: 7.6 MB (7622437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f2bca606668f5a1bea56afcc42eab166a62eea54312e28867a32c5b1194df7`  
		Last Modified: Thu, 22 May 2025 12:41:08 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:923a6a19a930c0388f11a901e2d2912e35e1a57a2f3dc4a4ce0c9492c3e155a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139544175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dffb9e90f2c118bcda2d237ce6dc2ea0dcd9bc061c6076e28570d944dabcceb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Tue, 03 Jun 2025 14:40:24 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db4d1c372b0a8bcc5558ebc33a0807a079cce1bf7f64840912ce33adbe79d6f`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 24.9 MB (24915395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d77ca161501cc8afd738216058d54ab2ad4f404972c41e87bffedc3f8f0766`  
		Last Modified: Thu, 22 May 2025 01:09:16 GMT  
		Size: 66.9 MB (66891223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adc67406a97bbc491de8d7145c764f72eea6c046f42d2729770ee069e55ee78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da93994a928529ad9b613b651ec3b8fd69300e12512df963a03eb6c9867a0219`

```dockerfile
```

-	Layers:
	-	`sha256:c171722b89d071b9c6559d8a8b567668218f26dde200f9f52dc22d957074888e`  
		Last Modified: Thu, 22 May 2025 01:09:07 GMT  
		Size: 7.6 MB (7598778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b54c33a87b886563879200fee2b12a25fe14fa8286bfc8034cc1a49f826af4`  
		Last Modified: Thu, 22 May 2025 01:09:06 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f11391916d142332766026af9a2d427aead88a036bb9dcad71fa3112ed33ab88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144747935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c2740840e27196a530b44704331d8d6fcba609cec37d9799b8d01971b239a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:719077674b144dec5ce39e78bd5eb75fa6363d159411371db443b10356484cce`  
		Last Modified: Tue, 03 Jun 2025 18:04:07 GMT  
		Size: 49.3 MB (49325662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279b96ed4b6a4d60a4f4cae771f06c0b94acf2fcdaafdb528c367ec96583697`  
		Last Modified: Thu, 22 May 2025 01:02:36 GMT  
		Size: 26.8 MB (26753393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c2e2b167b6b97a9912e58f820f9ac156c2b2b363c5456b8345d2dabd44b39`  
		Last Modified: Thu, 22 May 2025 04:38:13 GMT  
		Size: 68.7 MB (68668880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a0f23bd6d9a7f473e9844b45119dde3d4bd73b96c73668d0432d116cb7f4c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5eba5ad707a72ae40b8adb0893ab85052f46514a9f12edb4d439ece3b72a33`

```dockerfile
```

-	Layers:
	-	`sha256:1ccf26d054b249cf40760dd7b6f28cf4ddf692ee736f612b7b9a93f5a5728354`  
		Last Modified: Thu, 22 May 2025 04:38:11 GMT  
		Size: 7.6 MB (7596561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc7e7c49119fd408ba203869807308683f203ba146bfab0fec046d7c937cad2`  
		Last Modified: Thu, 22 May 2025 04:38:11 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
