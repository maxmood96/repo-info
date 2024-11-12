## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:ac3b77b97d93526de4f0d77b776ac4713b1d653173fcbb26050af57ff1e56449
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
$ docker pull buildpack-deps@sha256:b676273f23311ccc5244ff6e63155dad8b5bb55b6d82b8f4e8d33972ef6e4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa631a28a982643843676b9f863f4d093a30c8b4fb480687f9dd53bab255da5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a44f1891b371bcae4f11edff9fd8aba7516fce6c2ff75aa458027d07967d8f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cbd7f1f078bdc9aecceee2b5a77d73e45b0bf9b977b377ddcf47db36b3e1b4`

```dockerfile
```

-	Layers:
	-	`sha256:579eb45b34cd6da0fb68f0f67d8357369dadbde36df878a8b285533dd9fb9385`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 4.4 MB (4365542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7295b715924a4334f4fbb9c240fcd002eea2c8913954669a52796ad9fa45891`  
		Last Modified: Sat, 19 Oct 2024 01:10:42 GMT  
		Size: 7.1 KB (7051 bytes)  
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
$ docker pull buildpack-deps@sha256:704d078e6f0512924e23fabc519c270c4337592544ac088b753a03beb2edca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79261574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae709f8a5a2c18f20fdfcc13765d33af7c929548193c66e87d682e2d4338628e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:802ada8d1fd6a69d696bd789b9e6ed88a9e51de5e365b475c2d0bb3e15964827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d70d877c0e5eb209272eaa51467fd68839cc0c02f90c896d0ef9848c923e5d`

```dockerfile
```

-	Layers:
	-	`sha256:b6e7a8cf77bf1496c9a858f7c7a6f5e188fe91072b7afb22d90ae72605902920`  
		Last Modified: Sat, 19 Oct 2024 00:56:53 GMT  
		Size: 4.4 MB (4369763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1ded31c90b6bb0502d04c6c8a2dd6581bfd17ac18f5381e46d9ad71ed29b0d`  
		Last Modified: Sat, 19 Oct 2024 00:56:52 GMT  
		Size: 7.0 KB (6997 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21adcc891214e1112da5648d6249bc00f6bf79e3e4f4877a81e94b9650c2abff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71988844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf3690d729d99a4c77c28f19d3e7ceb3e8a868a32d1fd17330077491fa06c6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b672735e07b6bfd358f69deeb922ae67580e9d16527ecebd87aebebf732dc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb7d494d53ee86cc3697683f361f7502649fb74eedbbf4aa682d707dc2b17a3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1dfd30ced67644e7b9d672f6c07044e4b073d0d5506e4c0fcce2d600a96042`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 4.4 MB (4364967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a34545ab0e16c7b338028391562e8fb28abcfdebbb1613eff8f60838579b1`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json
