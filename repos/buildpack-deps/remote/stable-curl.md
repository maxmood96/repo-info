## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:2cf44dc6ed437717b1b13958ef65ff82f319a07d9b9e6430f760b0ce56f71526
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:66af74907dbbf8b0b007f1364cfb5533d82b0914d637c5301d66debd326b5bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66778ca3ecca132ae2e3be9f9a8816c3d6c40cb971e200c41a3f5290dad963f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4381a2b2cc6a99c2a4ffa943e12de2a3b440472c92260a91358a6538faabe30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c0832bdbf3d4024494f0f35041fa87e24e76195abb8517155a69f34eb7029a`

```dockerfile
```

-	Layers:
	-	`sha256:a0219f42489d77927b354aa04cb7ac25d3f22081c950ff62e02f3f036ac57664`  
		Last Modified: Mon, 28 Apr 2025 21:55:01 GMT  
		Size: 4.4 MB (4360055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10113efd0c00dc03f7ef0ab683562a3ac0b0440a3f69563911df606e74ceda3`  
		Last Modified: Mon, 28 Apr 2025 21:55:01 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:525826559a142a1a47aca4b22a170f23edabb1ca153ed37aba078d7714de06ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68715956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2178c72340f8e8051315051950029b423f0ebfa7a3e6461c725a60a7fe30e520`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:954a4dee2c3bcdb3f959501018b2f7eee77429f86f4d4b0c0110a67bb052a4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce25383527aa4e5000837f9487356d0837ed9b455272a7722ab9c25b47f4d043`

```dockerfile
```

-	Layers:
	-	`sha256:0d05ef4deafcce75ff037b0c8a3911856d054e0a4fc8dc4b08cd9e1cafeb58dd`  
		Last Modified: Tue, 08 Apr 2025 05:11:55 GMT  
		Size: 4.4 MB (4363571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8155b1899737eb366ef64287a8137e433a85e6a474e0284bd9be37c4142a5271`  
		Last Modified: Tue, 08 Apr 2025 05:11:54 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:105f49f696b99216c44fbf41c45e662817e6fb3e2b2e5b16e1df11d31e219f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66115014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2e1ebde96ee71c635e5691f93f020118896432599348911a18d18182264fcd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:958a459768b0245f14d1d03553a58316273783164fe98d802c6a611347fe06f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d642fef2f70606d719e22576945892a0f51fa24b57c06aba99bd59838391b`

```dockerfile
```

-	Layers:
	-	`sha256:bad3deb3e137f2d195810db9439dafd9b3ddbdd1a7192fcdef6a161e1703f571`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 4.4 MB (4362352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f801c2bc7c44887fc924640035be133d3e5e73056bc8e28f2c8ace7b9b456f`  
		Last Modified: Tue, 08 Apr 2025 07:37:53 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:43e18787a40d79e85d413a50ea1e236f1cfa0fcf8889ca87262b71385e50ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71871808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c5daa0e948612bde3274e0d14bf7f9c336cc044fce24269ee07b51505ddac9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2a3da4dd2dd41cb5ad36feaf8f54a03f47d9a2a7813c88b028266f09130aae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf406473ae02a205c355a1c7932c8380f5f461b6ac7d0fc1d931cc040a93fc2`

```dockerfile
```

-	Layers:
	-	`sha256:6128e650c6d090228c54f969d5a77408df185e34e35c0ac1f4baffe660d709d4`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 4.4 MB (4360328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04fca87c127711e9cbdf4289abd17ac76c2779384a2b98fd355868c21cb9b2e0`  
		Last Modified: Tue, 08 Apr 2025 06:03:13 GMT  
		Size: 7.3 KB (7253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e2682489f49c6b2ef640e27da40f0b455c2e0cc22643aa8a1794ce26206d52dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74325719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28bb7e701b08f2c5d0a26b3746f00c6e92c9f6d49389b2be2fa21d2d58f3e3a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:edba52975ea1a893d184f0bc466c88dda42c467bb3b1576a1e12a02d1a02b326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2539bfcce893fb91748e8637c274feb036ebbf4a60ebab7ff17c3fbca0473b54`

```dockerfile
```

-	Layers:
	-	`sha256:f5f2461f65e1ee57f8a9428de80797091ac584b96e2648cb00cf660ed78ebe6c`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 4.4 MB (4357113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718e0351d6be1e86a0f14b942d13972f8513aa01c6e4f97f00ab329a64fad225`  
		Last Modified: Mon, 28 Apr 2025 21:53:41 GMT  
		Size: 7.1 KB (7136 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b0ad87f52a80e17f90101723c9bdb5d6c2bb4caff190929fbf8241801349a390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72370473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcce605aa6c3eccacae3f0ebb17d3907cedd806a791c722ca31738ebecd5105c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca10b4d080e8af4973a6e24a6843081bfad00b67f455872055b7af8fc0e92332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3758a9894c7a50de502579d72484d756c2c5f40f14a96630dcc77cfba0496d7f`

```dockerfile
```

-	Layers:
	-	`sha256:13a80988489aa37662edbcb70b3cebfde64e80eb1ac66943e23017fcab267f77`  
		Last Modified: Tue, 08 Apr 2025 16:30:53 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71a347195bbd53dc6278c4239a34384f03455cfe922b3ead51ffc7482f9df890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77981822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da98533123f3fccb50276196982f5c2308fa2d91f5343b37490d38d6abd0b5f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf427b662938f89bbae8e3d5517b2a058c266954c246416196a80ea68c83f157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d10542030a92ca67d5bc5fcefbd615c4fcd1d47d14cf1df33a7536caaf9098`

```dockerfile
```

-	Layers:
	-	`sha256:8ca51a4ae14249a3b3aa533df5be5359aa4e83b23664d09cd54622852ebc0e9a`  
		Last Modified: Tue, 08 Apr 2025 04:30:14 GMT  
		Size: 4.4 MB (4364547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3abc1a0d1ae10a0817f83c9cf5b826d27a210b9c9ea0f1f787892a19ff9e61`  
		Last Modified: Tue, 08 Apr 2025 04:30:14 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:48ac7c92f1b0b6dd171159d652f5c6f36b78c70c982eb0c08e1056c180a3022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71159643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f80b2ce834ef28f5e1e0ed7b906b9f54bb71b878f93c3c93954fee621c70a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45717e793366a78b4a3fa84c09c90cb3a210d3bc76381cc1f99b21596dee31c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ebbb2957bcf81b3ccc467e9b6d8eff3e482af8862b87a7c6b00fa260476ce6`

```dockerfile
```

-	Layers:
	-	`sha256:30fdc883177de49dbb75024e4f42cbc733d7a002328b317245ceb0040b4e73a8`  
		Last Modified: Tue, 29 Apr 2025 00:01:20 GMT  
		Size: 4.4 MB (4359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad7232f4813cd45c6d4470f8c447f041b60ad0a113e10cd2c92cab1b94d8ff8`  
		Last Modified: Tue, 29 Apr 2025 00:01:20 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
