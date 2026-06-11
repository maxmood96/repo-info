## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:668e0821be6e39bbfdd930d3f6e9d15698ef8c0ffd803e7a4561bd73bf8bb3d5
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d9827af9a0ae461b2173a98aaadf9c2c7f36fdee9d0da2a507adcebf7c0d4cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72546042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0705f0da4d7eb05ef081c8686d877ef4188ccacfe3a65d17c5c9b826c0752265`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a517623f41d8640c0e69aca118cb1e085d76e95cd58113089546a176d021860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d92a0cca61eb4899379e3bc251bb05534f79ccddd2833183e1b4bd2d8247c`

```dockerfile
```

-	Layers:
	-	`sha256:0ab66dbbaef843577ebc99b858459dab40ce5b3de5ea835b562642f6abec2a02`  
		Last Modified: Thu, 11 Jun 2026 00:42:22 GMT  
		Size: 4.5 MB (4514370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c31118263759aa0843d7863c721fa6697e229a77e8ea2196ecbab7c312924a`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dc88449e8114fffdcbb9c17ce056ca3204f9f8ea0073e8395cff883c02354525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68747130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc41aecba5ab0070254e596b1f1d33bad4ca629aaf6a0096cff03c8c22800450`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ec445b149b50947066418df58d379ecb3cbca1deae1f8b8054123d04c60e4d`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 22.7 MB (22717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:207793d3090a83d056d5cfb7ca65e2f7dbd158f1984544a36f76d4d4f5e2f21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266de8173203c2df6615e937c359ac620d29207571d18d02b317011f0050c0b8`

```dockerfile
```

-	Layers:
	-	`sha256:13216556668f988de1a2b964a8edfd868155a156cd629b0229309ad8167d5fdf`  
		Last Modified: Tue, 19 May 2026 23:56:05 GMT  
		Size: 4.5 MB (4518168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e43c606f1ec3d60201eb18ab74cedaca4e77ba326ba15c3ff14155e2a848bac`  
		Last Modified: Tue, 19 May 2026 23:56:04 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aaa21bc173df72d972f33a8e086ac5a6e978e82ea65182b4f232b39bae3bb05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66159287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d9ef2d23b99f070d19dcbe2bea3767b0f6be847947e9e241a839032c1ac2f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38766093b63d53414c84717200adb10428f14697011f5e5d3a6c692b2037dc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b62f5b81fb70cc5dbdb4f65c7b8d728d229df5d7fa876d89b9026701566c70`

```dockerfile
```

-	Layers:
	-	`sha256:bd38ec6d52bc66c3057bebf8dc71d1073006a81a89b8c8ff61844122476699f3`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 4.5 MB (4516641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac551389b789fdd672ffbb781ba1fcfcd10cabfa030d13d0c2e97a079d53fb72`  
		Last Modified: Wed, 20 May 2026 00:02:10 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bd167d35f644b0e41f6d0794471eec2a9a3c3c5f52f553eee4f725f7efdeed23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72002312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa46eaa27b7b97a1ab9ef5ffa4bcd9383627458ed6f66e3094bb28049e00aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a87f16766abbe34ab9bc5a9602c35022c5459e8f8d33d902aeafd4e2aef74397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75df71bddfc65f7f8527b6822449e416fe3a177d398cd74dc96fb6beae4f69f5`

```dockerfile
```

-	Layers:
	-	`sha256:779ccd8a5930523c65115180b5f2d6178dd63ceb58ea98a7bf5e3d2243c2797d`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 4.5 MB (4514631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37460920efc699937f457c95363e3fd95fc5ebf024224b6b8304fd624155093c`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c24d3c5445396b62c71e20432bcdf2487248369848ef1ee456aa5dac4d286fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74362602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84497b809dce4baeaca5766b6cc6cabad5dd9e2449ea0e8531f5dcc4a0e799b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:460611f12778dad7692789ce01b1bc4c66c9b49d1903b6cd90a0491fa2a1629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cdada86d170b7a562af493d0db4816850f723b0e3ad74b8217573c181b513a`

```dockerfile
```

-	Layers:
	-	`sha256:aa8241ecb7a3195d94c2123dd67d94a60f959c2be0c33782b793ffd85a62855f`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 4.5 MB (4511471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aea4e11bf76f67c9de46f870c8d5970b67ff0b124384b6688bc3d91291bba04`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5485464a506b4806c93bd63e8463181b97948964b110a85f29fae94f79620cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72407440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4da1a186c4a8d41207c37420baa8ed8b8486a680e8d89bf4223fe1eaa245f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da14ba9a088108b08041f83af540e21c2fd11ef5729cebd0db809fe0543974f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b9cb25691a57d14fa38c322eac504ce7ec98e7944d78851398fc6bc2726828`

```dockerfile
```

-	Layers:
	-	`sha256:fdd1ef28837e2aeadbbd49371944cf723c5129d27d1575b57363e9ca02b25411`  
		Last Modified: Wed, 20 May 2026 10:05:29 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:605f7cad340a1c65b7d8aca4fbf019f8b45600dc3157030c17ecc3e4b6c738c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78026665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3eaf228a602681fe5ae3eadf5c42889ddaa702d01bd8d3abd76fc20d2ea9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca9a10b011b986aa72f286cd55b8958c928275c27fe6e0dbc30a0b9de0b9e06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61b79c879fcef29065480968bf2bd03a8cbd401f74a1b7512c1f26dc8ee02b4`

```dockerfile
```

-	Layers:
	-	`sha256:62469d397464b3dd2b1afc5645c86966876fcc9f74c9f1dcade175d7b5b2e635`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 4.5 MB (4518978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3562e529e883f7c3ffa6c9dbfffa8153ec67e1a4372978ae8c6d3e0a71605563`  
		Last Modified: Wed, 20 May 2026 01:13:38 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c89b551701972f7ff2bed472ffc8a3a0a9ec2a4b1b9d1631746b826fa0edcef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71194790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904805285c438a54cd8842095ba2dce6b0c5a9b85d085f201547dcc9bf80a5d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05696af47833f28b0f4526caec26c8624a7becdbf6124195a718ecfd87481b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aafa63b9ea84c437329f710184dbc938429377d19e904a6068f4b5f79965799`

```dockerfile
```

-	Layers:
	-	`sha256:7df8ebf48427baef28858b778de343632442a5949bb461e655db5125d29f6cf9`  
		Last Modified: Wed, 20 May 2026 00:18:11 GMT  
		Size: 4.5 MB (4511156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67f1e8df9757a960c6be006c16ec590253c3cb9093f8dc43e02622788deb678b`  
		Last Modified: Wed, 20 May 2026 00:18:11 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
