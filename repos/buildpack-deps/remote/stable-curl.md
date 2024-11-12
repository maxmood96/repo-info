## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:b8745ef04ed056786a40fc4b6d52cd1753f527ea93a36eb751bb310e399e3d9b
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
$ docker pull buildpack-deps@sha256:41e41eb5a1eb21e97dc86dcc037ad0f73605f83b56c1c73464dd1db9196a4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73634041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0afb2b1893cde96efc8d8210faaf240bf974567fcffc52c897c2f3c7dc9d79e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:986d0095b9a0c1ba3301eb55fd09b2d313291d46eb689d40f40ba5e22fe89c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2308a6a913223982e9855dd8579b6c1952e064d55b55df3b488871308faebe`

```dockerfile
```

-	Layers:
	-	`sha256:ecebc53c12ddd3cdc651d3ac8588af340efb560dfff14086c45f26e4a6845d00`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 4.4 MB (4365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27611db305d9c1eaa6265accc831e7dd709d1ce5a580841bed26a4b03073d79`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e3fafd00e93960e28affb776bf24b68be5f16c8ae8264d6512d64e04638b301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70072054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae47018992349a5e2058c7afa3cbbfad33c53a796b526639fdcbc544a232dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e697f44f82c828c459781743ae81c1b1fa2efd11d0ef16c315af40a6bf46a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29044c644def0ce321a888bed6b2e6a887e065d64284048b8cefbfab2415ff06`

```dockerfile
```

-	Layers:
	-	`sha256:0021462fa99eaa3af9d3f7856d66255747ce9d86290f0a67360aad6258734a1d`  
		Last Modified: Tue, 12 Nov 2024 06:28:07 GMT  
		Size: 4.4 MB (4368821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccdb91b8a0e2609fdd39cee4ab8cac4e44254f455c3f6e89719b35df75eed9c`  
		Last Modified: Tue, 12 Nov 2024 06:28:06 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c662459553ad055a4708b89aa5566791ba9f6db440495230e423d3717ed80f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67105344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e198c6502a080d5a4c664099e8b9ff589ac930f16668d5f130cf883973bbaa81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cba624557f8771ff8e6f953c75df4617cfa8c60ca2b011736603d07c4444364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9976a29b32bbb9b5140ecd8b4bf572ea9cc6d74bd34b93452ba7cd5c03473689`

```dockerfile
```

-	Layers:
	-	`sha256:24a261958b30f61e4637a1276fecfd8dc488e904699a6f9c0198b7ff85717689`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 4.4 MB (4367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6bc5453abd7e83a2ee028712e1c439a5056c837ebe26cafe5657b46bb64d60`  
		Last Modified: Sat, 19 Oct 2024 00:56:09 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e46fcc0c7385b7dccc516a32fb6dfc4d75a18dc39b9963b799d0cc2425554da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad60e192318acaeb45178aa2a8ced73c3b5c2075f1d0909094e482012ae304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f238c1fe83bd003f1036848cda78a6c3cf076fcbed76560d0c41ed12edf3889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e335a8c4a64c4e0fae9e376895c95ac74dec942b688c1d5712b76326b89a71f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5ed8ce9f0036a2700ad927fefc558470f78b81f0b62876e96ad9516c09e17`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 4.4 MB (4365578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3af911d4ac8fc50b9625684b9dfc26cb7861e3d51df952fe066d4eb1c8f230a`  
		Last Modified: Tue, 12 Nov 2024 11:16:02 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ac574690768b372f5dffd3fdba2f1316b68ee58133eada25d6f76b945c3503ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75476458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec174eb03e66f601edeb0488058e18636473d68377651065577803c0ac3d03f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d746769d0ce07c638d82090c56538afac5862001d98ec7ae5b23ae300ec87e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1441e57a6c764c8c7ccd95b08a608a908f3a9b0e5c6b666386e59faebc024b53`

```dockerfile
```

-	Layers:
	-	`sha256:8f720d960686e4104e12b5daa17252fea926f0989e5e2d35e3b5ace686835b71`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 4.4 MB (4362362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce198488c58998d3efa8241e574d30337efbc03936c45f6efd2f314bd790083f`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40a0ca2a9d801d94c209dd4e81179674356393b1bb85a7c778a3f4374809cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b37c7d352dda03ef9d6be2c8d635f31984a92699dab52f36b5d3f12c515f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fc9c2dd787c1afef1c1632c49d1eb5b563a6facb531dd8b470488959b3ab9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 KB (6798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4747016d2b84e54ffe37fd4cf0d9b6bb34a7055915405f718b1dd16b0a090478`

```dockerfile
```

-	Layers:
	-	`sha256:eff80f8d463471c1876e84ba06456595ac60a9fd7d52d23925ba9857a315e820`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 6.8 KB (6798 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:466f233ffc3b8ce8fc8e24fe4e0a478f467ee9c1b9e07ccaabb6d7f4dd82b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79272813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8258da2a3b826e8087b187be36e101338667cc4c8f4296ef4b30bf4867d89e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2238f5c37875dcd6505f74cd1d75fcbb33c40ab59512d84b295b8205ca2a6912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a107c661e17348313475322db42ffce8541848e8dd47876d57a3062cd14c027`

```dockerfile
```

-	Layers:
	-	`sha256:f1df1624c9d126aec722784a58ffe81fe99f97613ee2061a4ec42a2636a26b04`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 4.4 MB (4369799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a16b8c21a8a4d843e70acb35845f9570090375bdc2418cb56cbc1f86835707`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:556f5aa74f180a341fe894576c8df3a358c7ad6432d78efbbc0da3bb71f523e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71996571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac9802c1503429c3afb4b5bcf9abbc62bf5678126c5a817806438584d76da7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5638e5d412c4935cdb5c941063892a1c760db5bd429ef01755d419da71ac16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196d3bd3ce51a1e06975a87f93ccac12d11dcde272e5ea99e71a63a7bf9d9b6`

```dockerfile
```

-	Layers:
	-	`sha256:86a46b41b61f05b5bf553bb19fecd56edefa4c046740d61578dbcfda5746f13f`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 4.4 MB (4365003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63952b86a5ed4c59bfbf8d5f3f31a85aed5da9a9298e45cbdcf514945aedb636`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
