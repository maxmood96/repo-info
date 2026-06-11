## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:d356be0c6218f9956d0886b58d94b8ae6c7652e278463e5ee83df725df219aeb
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
$ docker pull buildpack-deps@sha256:6ba715df17d2b4a8a4dd594a0a4d88c3b96f612b3ca81af3ce77a85aadca41e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68756179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdfc3b39a854cfdfefb0507b2428109a8bf27b5549e30276e2fca5817d08413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:277709050f924e972fdb724215b7b468e4723c03c7a7166db4799124d5f75099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffda32c4a2b801b870bcf7414fb0fc94f52bafc2445dca3871d00d1b1893865`

```dockerfile
```

-	Layers:
	-	`sha256:5f88b6eae6bc883621b9ff3d69888fc6055f45f5d4921ba9a400026ebb63a3e4`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 4.5 MB (4518186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711ad1b36d68ea709cca3a9c07429242525597865dc117a486baf129202dda94`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:657e24bbab7921237254d390aa783ed3fb68e9e72f1d6dcd5d03bfc4f27765be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66157938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6274275a3a98fe9b07ddca9a8525fe4a7c665a1252732a5bdfc8c9cd5f08ce68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e351bf888e49af953ed9ca8b7019938bbf39fe04156e4714a846245e98b63db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6c92d39046c0cc60c2bf966f317bfdbe1c1c836054dc66e937b5c6e9ccc2ca`

```dockerfile
```

-	Layers:
	-	`sha256:e7592d8f081e175d0487c58d8d5c97dc964baed2a3e551c19fae8d4534e9e74c`  
		Last Modified: Thu, 11 Jun 2026 01:23:37 GMT  
		Size: 4.5 MB (4516659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcab072c50bb21f632a636d5892ec79b5d88596906fc9d3050b28dd2139f7306`  
		Last Modified: Thu, 11 Jun 2026 01:23:37 GMT  
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
$ docker pull buildpack-deps@sha256:97c802d35b4f35c2212815d8114dfd3921def930e0812332621d2ddb17ef0302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74370920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89726f570e36c60e5af972d8e882ddd356e7c7a7ef0a2cb1e528152a71cf7b5a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:09e3ae716592192d443f7aede2634d0f3c1df855a2224e58571132c333b6ac07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f958ee073b66777fc055a86afc96b21611270feb2a79acb3f7ebf8a7278f9b`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3c46fcd22c5a7c9954937cf710803a0bf8c5c5c067fb818646f5f4064b256`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 4.5 MB (4511489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f156a8744ff5f28c570d35ce118045856d8f5db0fc2c3097e054e093d221bb76`  
		Last Modified: Thu, 11 Jun 2026 00:44:58 GMT  
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
$ docker pull buildpack-deps@sha256:9f266b35fff203887be290380b1092fa9841dba5d71dc9e6b38b2ea14ccc7362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71200450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadc1a4472d2cd0a9727394872c4f2eb747fb1b76e671ceb713f38c3fca83a47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22e9e699689eb395fb1c2eef1e50247f99958d71eae312aea7397049ccaa20b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdf632ef441a842387ac62335c9eda0bc74e12c50c4a541c3dbdb843f371e7`

```dockerfile
```

-	Layers:
	-	`sha256:d87edb8cc667051eee8327ccbeb9066cf67024d88c83ea29e255f9002b90f2af`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 4.5 MB (4511174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef890e49192bd7ee91b7708a91bc4dca5ac6236d2b14311fa02afdcb96635d6`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
