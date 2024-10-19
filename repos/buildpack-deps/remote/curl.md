## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:89f0653a0a912939914d7df4bfbf6b6759e1713ac7307b734d205628eb195879
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
$ docker pull buildpack-deps@sha256:f5bb9ad274f7483bca35b7ade28409ddc366a3030c721f8ec01945f49c1f1400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73606409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6595c5df915beb56b486d44173ffcd9c8778b221483592385d56eace9a801f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f0ef8013ba25f54dfd23730377c2d93f590a45df065a2fbd1f91b943b36a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c17604ff561b13d6f71ee7c0a751e0b1d183ffa185632d141c0ba72398ed3a8`

```dockerfile
```

-	Layers:
	-	`sha256:afafc89040020b7a28a31732e2dc724fbcf41e580d58b02b74e8b0b4a2872c90`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 4.4 MB (4365270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4400ed85ba89c4bbb3ecdd1deb3eec80325469a08196255657479cc4d709369d`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 7.0 KB (6965 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:29e22265f8e27deff56e30507c4bf3c45395cf51cd0cb178b01a10d0e74fee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70060096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7708f0af4315775dde7d656b19d6d877ece75b21b2f7335d8bcba64cefecd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74674b1e8da5cd0bdb2b88260b7dc90e413cff1e3bb65d3d272730dbf8690e00`  
		Last Modified: Sat, 19 Oct 2024 00:54:46 GMT  
		Size: 22.7 MB (22729575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4af3bdf4e5d1217cfc39da2266dc0351e9da0d1cd982341b997f89ea78399711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9290411caaa63ac5ed8e0a3029f8c3819fbbc16a6f4487e2f8424d6bc5d62dd2`

```dockerfile
```

-	Layers:
	-	`sha256:09bac3dbe394bb359e9648ccd0cd52e4092634e941964afb8413c9256644626c`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 4.4 MB (4368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66fbb3bdefadf96a90da6d4bba1633b49859fa6532385c149fde11810506952`  
		Last Modified: Sat, 19 Oct 2024 00:54:45 GMT  
		Size: 7.0 KB (7027 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm64 variant v8

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4efd8cc6fecc767a4806aab581f19e51c45faa286f89478f3967e5eeff607d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75471772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2131351b74d10ef77e845cfcfcbd26ab0a63bb6cf71eb9d1b38b7a253694a7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968576d52726552d23c39a66f1a0ba3f2ca10d188a4fc6750691a97ed494efd`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 24.9 MB (24894938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8464dd421e7a13ca2df0a0ed389801a2de33aaa8ff036e0e0a6e3b59de523dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94482666a0f9222c4e2432930198f007ba125621aecbb5b0a20a303cf82f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:bd25bf9485ae7822635d94ac3ac93b79ed69aae815fe5d3237c28b028036df11`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 4.4 MB (4362326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daf96ddb27c922caa431414e6f3178b8a5546068f19f674e9e40d530b3a9207`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; ppc64le

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; s390x

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

### `buildpack-deps:curl` - unknown; unknown

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
