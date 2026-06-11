## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:946313ef537967311c9fbc5696b67315a73051a249572a8c724c98ebed935238
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:04603c23f8433ff0e8e7a0f20dfb58d66e9ee720e4ac548c676b4f4e6cd6b2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136950158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ae5b6cfd4e8db8c8a17ce6748587f1ac9a8b96e01cf1a0e5b085a34a804266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2ca8a7ab64cbdaf6906320addea6887b8ceb9b2c619c209d1c2f7228ffd8281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e329d7c90f72adb846dd65379f5dfb4e80dde9138fac55c16ed95287f86209a`

```dockerfile
```

-	Layers:
	-	`sha256:479b3984b9a0089a08880c2fe30a32ea9a50e62f81c9c08d17f4466e3d005d97`  
		Last Modified: Thu, 11 Jun 2026 02:24:41 GMT  
		Size: 8.0 MB (7966088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da10b083e2c7038a672620103ffea6fb667e47478a8c80a75b7fb0a598a658d`  
		Last Modified: Thu, 11 Jun 2026 02:24:40 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:507990a378809a1eff943177ca2a7cdadac5bf6e9335c3a9cfe1224edceb32c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130778662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909d760d82de9815b8e4780652e0490066759f16be454d2826fbc5da71f7e490`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3683b8a7792857dc507c3398919097537c8d564a235824e722ff16657599fe21`  
		Last Modified: Wed, 10 Jun 2026 23:38:13 GMT  
		Size: 46.0 MB (46038189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c451565562cd00a6664508aa8323b184e76b5b0de69ee46d3c1372a759dd2d`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 22.7 MB (22717990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a91f6061b18b13afa05f640b62518105d726e8abf295d2ddec34351f6d93ff`  
		Last Modified: Thu, 11 Jun 2026 02:46:57 GMT  
		Size: 62.0 MB (62022483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc1088304ac1ecc51ffa0da756ad048eceebb33afaf5e262134ea54ae51a7e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72f4bfedc120b852b3086ed551ed0e1f95926eecabc3288bde8e48872ab0ef9`

```dockerfile
```

-	Layers:
	-	`sha256:4a59b40bcbfb8596a4d0148a9ff1d55df9ffdc4de99f3ea02e203fd7f8b8bb9d`  
		Last Modified: Thu, 11 Jun 2026 02:46:55 GMT  
		Size: 8.0 MB (7967946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cfd556697c9e77794a2713da680df7dde93523d4b6f87e0c81a3814d81dfd82`  
		Last Modified: Thu, 11 Jun 2026 02:46:54 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ea513ec4e85443f4c3b223318bf1c2bc7547ec2f2a74469fa49eaf6c55ecd26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125819525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef5d63707f3087e327a8a086a3173d88a2d52ded76165c7645b07113d959a49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f7c68aa5629a37a99de2287c5dada27c5ba0cd553e5b4f28471c0e6c213`  
		Last Modified: Thu, 11 Jun 2026 02:43:46 GMT  
		Size: 59.7 MB (59661587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e83046c8a4667f2f6deb8841289604ef8df24bc484601851a2b7198156a57277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ea2bd08a7a0ee99bc7ce9f51bd50c55f737e269577e3b42e716f32761b0efc`

```dockerfile
```

-	Layers:
	-	`sha256:2fc3680b654f37c238293e47e5a8aacaa6c2ee86f34e22871ac2ff69130f1df9`  
		Last Modified: Thu, 11 Jun 2026 02:43:45 GMT  
		Size: 8.0 MB (7967365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04284fab2082519232a4f26fc66fcbbb53eae2d66aea23ef91e06cb39adb685f`  
		Last Modified: Thu, 11 Jun 2026 02:43:44 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4869073fc098fbc9d5ec8c6aff83913b10cb0af18ba681861c08c3e734067e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136490190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb8b5a21ddec883f31a83669b0db2297d1eb91e6e1f6be5ddd895fb70b49f37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d57eb944a604d2a355b6975f86d3b66e395890936783938e8951db8ad55d0859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab6f4f657679bd81baa057be2b97a776b79931919f44298f551b40eacb4a501`

```dockerfile
```

-	Layers:
	-	`sha256:a3078417848979cba1e52f7d595cf48c1698e2d22c1d7b8a696799f70d55db40`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 8.0 MB (7972481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54367adf5afe8209502615d51c5bdfc711ca59bd0fcab73e31836adb61518668`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ca72ab64dd4ec0fb2fffb18c5b86979673b3aed138c331752e3b5b1cc6932d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140614920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4895bdc56d0492544ee6155b38f6a4e3bd947459d9c3a447cbe6c09ffda506a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1abb617cf69e81d401bea3de65ddcc50a1ac250e94890ec9ab61cb42a18679`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 24.9 MB (24879714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc4b12d03ab32e6c96be6bc5f6e0fc347b431b1f7686aa5f92f4cd1a5cccbc`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 66.2 MB (66244000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3cd6a1e2ab9188a8cab5c1908aa48191e6b4ff826ef3300094673befb31736a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd089aa990ed61fb2680b36002ee9ca5e8f3db25f951fa83955cc2f9fb1024`

```dockerfile
```

-	Layers:
	-	`sha256:e279b5248eae26a05437cf743e674fdcbbaa9d806b3ec81223017d281e19db87`  
		Last Modified: Thu, 11 Jun 2026 02:24:51 GMT  
		Size: 8.0 MB (7962246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d21165e6412028b5f330f0e3b02b3b3c806072e6bc0bd923642a29617b835b6`  
		Last Modified: Thu, 11 Jun 2026 02:24:51 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:77f4e6764e3d0af1bbc42ed7169d01322856d6e330289ff1b54811913cfc5c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135723777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c311b013a9cd9724dd120ab1ff6cbd3f69a4bda7f6a7e7f81d8e28e4b90c3c0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22534cda1a112d38cbe65b89d2c2f5b1bcfc9f909aa5ace3ff8ba599e5e98452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0b6ea9c5c1f2d2175cb2820de5db6638a5cf5cb7109ce46c66854be91e3d76`

```dockerfile
```

-	Layers:
	-	`sha256:90fe789bc93d5abdd6cba5ca6954f282ab16b785d4a39b0b6efd498f7ea81f71`  
		Last Modified: Wed, 20 May 2026 15:12:36 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d1bdb0fdead6125f744b8c347b7e42815b3c8df9795effa5d48a4ee8a804b82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147887096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f0beca69bc13d6f8977e0b79d177f9539ef9183707412c4a95ffd8784d30e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 10:26:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3af7c755dce470b1c44918153cc71bc2ea3bed1cbf9108bce1ad1d4579fb5`  
		Last Modified: Thu, 11 Jun 2026 10:27:04 GMT  
		Size: 69.9 MB (69853632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a10bf21b288b7211fe561286548f8d0ba56139c1f572b31b7da9564f73bf6229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9926249d4392afbd9ceaf1a572a50c208b8c7e05afe450577042a68979e262a`

```dockerfile
```

-	Layers:
	-	`sha256:72d5b42d6cdcf5ff16f77eef10eb5285815e7b517b57dff84aa4485ae555c186`  
		Last Modified: Thu, 11 Jun 2026 10:27:02 GMT  
		Size: 8.0 MB (7973961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db71c3c01c7cdaf1bc8a7d6fc728fe1a72dfc9023f35f6767495d24855e45abf`  
		Last Modified: Thu, 11 Jun 2026 10:27:01 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:04bc163ac3dee4b808eac099716e840035bca88ba3bd2032a3a4da83245fc920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134698651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d41dd35215c0ddc351ab46cd816eddf361db3d7ca8928224c55a40271d63dc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0f0bf9684619796dace2f15b323a1fcec3fdfd4a5712e33f82ae28ed815bf`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 24.0 MB (24038950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33cb3e3ab28182d2640ab8d60069099e6c4d1dd9ee3f806d20e366f1901797`  
		Last Modified: Thu, 11 Jun 2026 03:26:38 GMT  
		Size: 63.5 MB (63498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0089867797040fb4aea7b68e2977d695b1ba3a6c538dba51757f6e2c56744305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672a80f910bda3458a8d2a4705ec6f522edade4c2fd52652004d0c7dac87c7e6`

```dockerfile
```

-	Layers:
	-	`sha256:737baaa2b61a00ecd5efa8c93e16da23067d069622c4568939c1436cd5bcd954`  
		Last Modified: Thu, 11 Jun 2026 03:26:37 GMT  
		Size: 8.0 MB (7962401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0bfbed3228f06bab3ad6774d43d166a81742be278fad12eb87c2676a877496`  
		Last Modified: Thu, 11 Jun 2026 03:26:36 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
