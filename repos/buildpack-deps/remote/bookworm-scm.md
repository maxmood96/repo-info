## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:6f6dabb08e75eb30ff77c6172669708824ff9dc78c8cfba75a25face3de5da2f
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

### `buildpack-deps:bookworm-scm` - linux; amd64

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1bb71cd12588d2370641faa8544c2577b1c0c03d7c377bfe2ddfe01c2d973ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130724177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdc5356602150a9a136fb955c0e6a171d0c208329667e3ebe17924d7b54465f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:444a58715eaf0dfd1bf39e8ed2c8a7ca67bc95fb2e8d072811ba720753b5bdd3`  
		Last Modified: Tue, 08 Apr 2025 00:22:50 GMT  
		Size: 46.0 MB (46026188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475fd0c8f5bfbbc214449bab28de187a71afadbad78b3fcf3ab5a380454a0d52`  
		Last Modified: Tue, 08 Apr 2025 05:11:56 GMT  
		Size: 22.7 MB (22689768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a439b8dc553dd972e806fbe1e6609bc57221e66dbdd1f511c50afda48bb3355`  
		Last Modified: Tue, 08 Apr 2025 08:37:37 GMT  
		Size: 62.0 MB (62008221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16d66596b9be4fa432273706d18f3da9438f1b915f5ba7345f54e60ccf058f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545bac41f31061b215f3fd0f9f206509c0bafb6373c5f0131d62d196154df8c9`

```dockerfile
```

-	Layers:
	-	`sha256:dbd9bde4f15f43c3ded13f5d4635eac7541f2b5489eaf7f00fb36b9c14cb8627`  
		Last Modified: Tue, 08 Apr 2025 08:37:35 GMT  
		Size: 7.8 MB (7752016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3129eed24be8ebd58ab0648c4d08105a59979a93ecad1fd7e06adedc3c3d19f6`  
		Last Modified: Tue, 08 Apr 2025 08:37:34 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; 386

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; mips64le

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; ppc64le

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ad80d3136c1ab532a85014ebdb8ba48be4d2202c17118bc97e0b82718b0a0e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134657707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3423ac02511650ddb3f6b13690d854c106ac1262b4cde87aa5bec3e7644c6ed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61726ebeb8ff504c7044b9d48e6f0733ed923720eebaa0aba02b9a4c8658ada8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7757318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595044d1f7213913752e48ec1ec35170e194dfc86ac7d806515d0ae1e53a026`

```dockerfile
```

-	Layers:
	-	`sha256:eef1cbe556578f9182c602f7e8a1089411a5c0493c775f124f93ce608ae15539`  
		Last Modified: Tue, 08 Apr 2025 06:52:24 GMT  
		Size: 7.7 MB (7749663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7398389ed1bec9bed7165346062aee15123baef72b0df4e4bf2644d9b37b12f6`  
		Last Modified: Tue, 08 Apr 2025 06:52:23 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
