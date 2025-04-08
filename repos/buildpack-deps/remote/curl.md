## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:d196c139b8770e0f992ebcf9f870fb97c07470590496a95ee96e4b9066b2260d
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6c3c650ca5440f9675e75f2483b7087edd4e0a08411c3f7553521cbaa01fc056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72501631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9934a592ba6842f87e05a281e86cc8f8a6f9d7cdaa175367ffbd29c5be9747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fadebbc385f6de799d5e86633ebba2d937b115aee0ec8e4675e7462f7c9e143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a29d9a26381bb7f64c7bb2dcc8921287804cff06c2cb886d4f21831fb607e6`

```dockerfile
```

-	Layers:
	-	`sha256:2e15aee1925f8db6639cf6446398ac489b1b861ff9f35d1b152c824eec67786e`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 4.4 MB (4360055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237662db7ee035c68ee34a167711e09b9e8ec4936b5e5296a25084039680921f`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm variant v7

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm64 variant v8

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28d439f012a0310c6db22f2297f146813de2421892f01b441505e3f4c957bb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74325334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fad1e8f27804d4c44d65c55510fec547c603732ea2c0ced6931ee9c6a2a1724`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ae395b20770e2a5d604e2059714080bf14f887d81d54b11f7c6d7abdd9740e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24ce351e2a0140ea50dffd88a454e30c9544e003f5a539a23a8492e599f8251`

```dockerfile
```

-	Layers:
	-	`sha256:0d4918b88e8c7436e5d0107229df039c88526f82d6546c404f4e272dac4deb46`  
		Last Modified: Tue, 08 Apr 2025 01:23:53 GMT  
		Size: 4.4 MB (4357113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf93331f841297cbfd242eccb050299e33a052285cf01dbccf961d78d8c81fc`  
		Last Modified: Tue, 08 Apr 2025 01:23:53 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84c204767cb7e0b90bafb12767fd1bff559c2c78870f258036b9624e96809e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72351760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcf474fa8fa3e36b696440aa460a51857bf8ed0384c2824817ecc7f81c12fb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ad0c9a32b05d0670c51f799e311b9dbbd42de3b7cab9b58ef8244b318a90e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a8ee4820b7d1ece08f5c10e31c75d5d20ae3025dce0812ad05ee0861133c1b`

```dockerfile
```

-	Layers:
	-	`sha256:12c42f8f5255e5d3a616b4a71655ec5f8b16f30f189d9c0099ad85d5710b77ae`  
		Last Modified: Tue, 18 Mar 2025 16:33:18 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2d595940ffb81f85fe34df6b14d059b0a940afd73168654884160f81ca034562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71159332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a53195a74708ded3f6528bda6a99af24bde5de1f3d12ae0fd3fd6d457e7f56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c33d0a443a02b325222c0894175e2e91c8639893f503d269cdb8f704f4c0d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debcfa45af89c6ffa64a9be50e0014925c7855fc95f4ebff313f1c91976f866`

```dockerfile
```

-	Layers:
	-	`sha256:a141ff8893f692a0ca9ca5d2ce3a31dda61b020f1c20cf658c7af6730cdd8037`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 4.4 MB (4359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2765bec492adfa03553cfa10226e232927a89c6a5b3037c157e4cadbb0ecc476`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
