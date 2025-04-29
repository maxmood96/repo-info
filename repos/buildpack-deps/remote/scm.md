## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:3649b18f1b65ab6aefae7610812b4f61bb41af0d00f96dad318f7bc9ca00480e
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6ef98fcf732cc18db4d27e00a652fbf07e31111017bc47f87f75bf591e7e5742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136896807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca551b1f3f4cc2c001f011dbf6244d4b613473476102280a75e2562703aa879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a81e2a66db32f9bcf295011e179a313430be3bdef73d87599aa67fac6ebd525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73cb7eff86aec2bff6829248ebda9066d29aee6767970bb90e0fe9c6ad69dc`

```dockerfile
```

-	Layers:
	-	`sha256:794971caf641e757ee0ad015bfbe16c93188588d24279d24f93b286d04dcdec4`  
		Last Modified: Mon, 28 Apr 2025 22:15:09 GMT  
		Size: 7.8 MB (7750458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:747ebe48a43fefd58d584724478b82087e9287414e49a3da42d5d033ed8ac484`  
		Last Modified: Mon, 28 Apr 2025 22:15:09 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e84734c30f13c18d6992c1c8727bb8b40882c6fdeae16a5843f077f3fe6bfbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500e38651ecd4000c3c51402836e16017faa7b97eaa859b930eb79968220de2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Mon, 28 Apr 2025 21:07:39 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Tue, 29 Apr 2025 06:01:08 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461cae6835e6d9e4c238b202d114b5fb2f2b659479fcad91acee966b7bf3bcc9`  
		Last Modified: Tue, 29 Apr 2025 06:21:48 GMT  
		Size: 62.0 MB (62005790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a712f9d1124705170ee8fb19f1b92dff191bd6cfc1312ffbafb810addd1132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66c6bf9a8e6a94d86793cad07ada62f0fad8d7f548d3f10e7a93d0d2026c0ff`

```dockerfile
```

-	Layers:
	-	`sha256:dce29bc8aae5fca558fc50c3302d0741a1db75bbec1be28579854bcf470c6492`  
		Last Modified: Tue, 29 Apr 2025 06:21:46 GMT  
		Size: 7.8 MB (7752016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:672cd97b7d31061f4478d0e783a1b3a7f5717610a19d4032a7b7161de25221b6`  
		Last Modified: Tue, 29 Apr 2025 06:21:45 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f94741ada94f72478781627a4cebeeed636096147ba45b27ab76796d1412738b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125754439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f6255ebc8aa9e59f9ade214253e5efa348540633ebda9446c4aa5cd8db7c35`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f25b2e505b3b6e9ceb717701ba14c7be1456d6f130bb11035eb7f2306609e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a46ffe50989d2475e7c8f0570370fd4ac0322218d994758294d713ca41cbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:6a4ae54202b3aab83e34f1e417cf100d0b9432e90eb4aab7de52e6977d3949e0`  
		Last Modified: Tue, 08 Apr 2025 17:29:37 GMT  
		Size: 7.8 MB (7751743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192d7d05e2ecdfcda69e0b86b1033e96e0a2dadac0452430020dbeb94c8639a2`  
		Last Modified: Tue, 08 Apr 2025 17:29:37 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cb78b3d23a26ac60405b7054cd115f9624fd003c6bd6c01309f9f94289b03fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136227588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c0af69db8bd96385754bce3f02d4a9f559086fc5c09a0c2b9263e0ed160c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1e9336ba60a6e56e21f111e3a6884eb0ade0fca49e73851a6c8cc8ca6d2a855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbe72b5f39be1aeb79ac8aab336060dc4b5cd4b7ec8443fb6bc39dd6267f2`

```dockerfile
```

-	Layers:
	-	`sha256:4284f0d85189b43d41f4325b7ad8d8118252309d42d644ecd0e8e116c2851d1d`  
		Last Modified: Tue, 08 Apr 2025 12:18:04 GMT  
		Size: 7.8 MB (7756863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24629e2e6866215f004783d5ae042f981b92f8bd0ce6e90a1313b4df0b07165d`  
		Last Modified: Tue, 08 Apr 2025 12:18:04 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9eec5536c37144d5a0907ed047160f892bb19589ddbfaa5cf895b64e678c2b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140554641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de8c340fe84879e2cc82c2f85ca55eeb4beb6aa020521ef7aeca40bf88df00c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc4add4b76524b84f9b55465a37a987ff02d1739efb3dcbf0522c417aa1deeee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061d545dbc8d93e064e07c3062954029c3fc1bd2fd21f4f29e678855958794da`

```dockerfile
```

-	Layers:
	-	`sha256:9d55212a28dbb897c44fbab2f2e2ba5b332a863f8a1f30644fabf78e2859c1f5`  
		Last Modified: Mon, 28 Apr 2025 22:14:58 GMT  
		Size: 7.7 MB (7746538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad69f362eb137fc3187d2ab9738f789832c059384ee7323413dfa429a120a00b`  
		Last Modified: Mon, 28 Apr 2025 22:14:58 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a2dafa3a1fe40c585b5b53d1023089cd7d6f8641603e06c008e77e9ebe269a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135678784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a7c840a2edff2eedef4b24377f1607fbd3daf378e20c79684e23ccc991f885`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83e3505dc809d18860248927308a5c27c298583b9da5817d702111bdd65622`  
		Last Modified: Tue, 08 Apr 2025 16:31:05 GMT  
		Size: 23.6 MB (23595612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecdcc124054ab515f88e8a0bc5260e578fb23450a3ca215363db6cf689231`  
		Last Modified: Wed, 09 Apr 2025 00:38:14 GMT  
		Size: 63.3 MB (63308311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:706509606ffa603055a826be6728c963d83498b8e99648669b90fea9dce48d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccece35a240c040d4a5ab41de7510c41bc0ef22c484ad9100645b2f365297c64`

```dockerfile
```

-	Layers:
	-	`sha256:230334131441ca6ddc474ea0bc01030912df5584c2901485304a7e83fc97a892`  
		Last Modified: Wed, 09 Apr 2025 00:38:07 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71033e8720141ce0c01d8096634c1ed9a8d6b6af6f960c7621164b5647f5aa5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147825745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d6aff5ceb9532be93b535fe3fedb655347a781a677eb2861f9e0d34207d54d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e5374dbeca4ff5b6a97ea2f251787ccb4f4ecd0321f031be5bd0a6b6a639f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaaca6dd23fec3c3b7c4d3b5c52cff9ad8d5a38fd2288e09577ae5569ec080a6`

```dockerfile
```

-	Layers:
	-	`sha256:5e72a19a5043628d3aa105823f22c7e1b4354f43f88cc2af598b6045c71eee6f`  
		Last Modified: Tue, 08 Apr 2025 08:37:51 GMT  
		Size: 7.8 MB (7758159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328d6767f7f9b796e1f698dea7f1daa9c18d226abd390a99f68eaf1fdc94498f`  
		Last Modified: Tue, 08 Apr 2025 08:37:50 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:42d3b590b427310d4e636340178da6ea58dcfc4748013ddf0bedc351ca0bf002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134656520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155c77ef2e6073c2b42b52f71dfc988a7a9f4383ad3698274b2f3f7d9884a702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:21aeb81bfcf6482640cfe8aa8fe38ae13af3d33f5dceec298f344e38f00a356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7757318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1660d2d43878757739726bb9c477581f30bfd4716c50219742bf65dc236026ee`

```dockerfile
```

-	Layers:
	-	`sha256:2a2c3e161bb32eddd981af71a0bdfdbe1452c148c764ed524a7272f206cab294`  
		Last Modified: Tue, 29 Apr 2025 02:58:47 GMT  
		Size: 7.7 MB (7749663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2267cd230f22468225b25b29277b125db7b9db8bec4e14db54ac75f3ca452461`  
		Last Modified: Tue, 29 Apr 2025 02:58:46 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
