## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:5f550cbbbc38ff07094f245d9cccb2cdb2ada29f69a2cdce41571bad8bf3735f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:352c44ab804db39c460a0233e5f5077651777045f2e4e99c1ffaf0ef96f85f0d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70839292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8fffc62f77957bcc9d59dc182f1db8e392f65f8e28bb44f33fa7c89dd86f41`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:21:52 GMT
ADD file:719f8702f6aa56e8ad69f574e924fdf062e8fdc72584f70aaac387be5e1d4a51 in / 
# Fri, 12 Mar 2021 02:21:53 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:51:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:78c7a03f25ec710f7b6b9ccc0ee40eb1871016252eea6df272c68389f18d30a5`  
		Last Modified: Fri, 12 Mar 2021 02:28:37 GMT  
		Size: 54.8 MB (54840531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b278fd0013a1b4473879cb9b2035cb02c05fa6d0900c208a8ef34a515c8b3aa`  
		Last Modified: Fri, 12 Mar 2021 03:20:36 GMT  
		Size: 5.1 MB (5136354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30451e23b656b5f6aacafba452dc7ed84b576095192b81dad42df280fb244c5`  
		Last Modified: Fri, 12 Mar 2021 03:20:38 GMT  
		Size: 10.9 MB (10862407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7bb095742fa344544351a447e144e70a99c0ecbd39b99059d5613af8beffbbc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67983709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87894180c08f09f52c431f1b97eeb6d607c8a276c0b20e40c560ae052acf0ee8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:55:11 GMT
ADD file:a1779c1f149525491eb986605ce34dfd0564f696efff3fb2ffe72af7ec4c77ca in / 
# Fri, 12 Mar 2021 01:55:16 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 04:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:07:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:177cf6a27ef5c990e067555516777665a0919d69d03f92e8e1585fb62fc1e547`  
		Last Modified: Fri, 12 Mar 2021 02:04:30 GMT  
		Size: 52.4 MB (52373683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f538e256be329fedd7f020e741cc9e7bf33d3be2d4805f957ee220e75a5bf4`  
		Last Modified: Fri, 12 Mar 2021 04:19:25 GMT  
		Size: 5.0 MB (5046198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beefb21b2f6f80d57a5c923e17c4c63da87a1360a28ff998cd75a0904f998a21`  
		Last Modified: Fri, 12 Mar 2021 04:19:26 GMT  
		Size: 10.6 MB (10563828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:92ba4eed1d3c59eaf537f9320fd611f1da8295c4251533d1e521a18aa88cb7b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65162202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3fc51bace80c76b3400d2b1dbe49f455b0c7016c3e3a3cc2f227b53ba9f4df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:03:15 GMT
ADD file:14dd8de951fe825db7d388033d6936d3035ea22c36f61cd84e564b5c97ae4fb6 in / 
# Fri, 12 Mar 2021 02:03:18 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:36:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d53db477f7b952a423ea709246666b7c318b3cced3843682efc6d4a208dea579`  
		Last Modified: Fri, 12 Mar 2021 02:12:47 GMT  
		Size: 50.0 MB (50045565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4025818d1b6987e6fb293a834f790b3ed687e5e51f4f134fe506031c6ecd71df`  
		Last Modified: Fri, 12 Mar 2021 03:48:39 GMT  
		Size: 4.9 MB (4905677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71de73a4f3386ee5720525d4d312ada7f5eee4cbce9ccbfb448f73714f705238`  
		Last Modified: Fri, 12 Mar 2021 03:48:38 GMT  
		Size: 10.2 MB (10210960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6dc22ae4dbcd6da98dc98203beabc9abe30a87652415629a6fa0f8c62772e7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69515550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2c8271961e2ec1a219f33612548de734e46fd52c6041e115a1937542eab1f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:55:07 GMT
ADD file:e98b46fa08e28b488d04d4429e536292413d7b6dfbd8a34310c44a6b65b421e7 in / 
# Fri, 12 Mar 2021 01:55:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:32:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:33:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:443483bbe5c8ae014cc3cb8df57a0b708d2b55560844a100ea84ee50c9b1736d`  
		Last Modified: Fri, 12 Mar 2021 02:02:40 GMT  
		Size: 53.5 MB (53528745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9595d36f863c2eedb478cac05b443a7facc8fbe6215c6ea34f6e78566d92db8d`  
		Last Modified: Fri, 12 Mar 2021 02:44:57 GMT  
		Size: 5.1 MB (5125646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162a05b96d3ad03a4a6a47488547154bb54acaebbb89c3308feb6fcb9e7182cc`  
		Last Modified: Fri, 12 Mar 2021 02:44:58 GMT  
		Size: 10.9 MB (10861159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2688c0e477825d2ad4a461ab361bcc0a63b0dfb0a320bfcaa00b839688b74e5c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72369899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc40ca99f7f9dd4dd2ee742db942e4320c1b1db9c3b020ff2593d9669b976f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:58 GMT
ADD file:f2f05e5770523445c3d58c38661c24400d3d13e8d89e5e8b361fe9b063862930 in / 
# Fri, 12 Mar 2021 01:45:58 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:18:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1d51db899b128072895ed240852af0ccc606db1f5e0eb5b88ceccc9b8bbd2876`  
		Last Modified: Fri, 12 Mar 2021 01:55:02 GMT  
		Size: 55.9 MB (55863208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5781e963a9335b9df072e412a0ebc745f84d8ae613018e2920170ccbb48bbe6`  
		Last Modified: Fri, 12 Mar 2021 02:37:56 GMT  
		Size: 5.3 MB (5265307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312f71f4fac8cca17e63b3141b7ccf40bef38b47724251c13c3b2550dac6dd5`  
		Last Modified: Fri, 12 Mar 2021 02:37:57 GMT  
		Size: 11.2 MB (11241384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1df0c591fdcc60c3087d25b998cf4db7cb0bda299a4dba9d8618e35c94d28d23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69062167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d41f3916c6124f80a38f64302bc4c5bdd859a99b4803995cc16e1821a89c2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:10:32 GMT
ADD file:05c36efb2a1cdd3e19c1c92b44025435230be4ef1d6ad0368a35841611aa0b1c in / 
# Fri, 12 Mar 2021 02:10:33 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:13:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a02bcaa9a66e386c33b8a384f0128e8f3c09d4fae3ecd414b165ed57c46c73e0`  
		Last Modified: Fri, 12 Mar 2021 02:17:54 GMT  
		Size: 53.1 MB (53099214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c432c77aca766d470bb76933642682cf43076808ff53eb201d733630878d19f5`  
		Last Modified: Fri, 12 Mar 2021 03:23:52 GMT  
		Size: 5.1 MB (5098099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97822413d3936f802a61681a5420dab88509f39bc24caa7ec14f56070b2dcef3`  
		Last Modified: Fri, 12 Mar 2021 03:23:54 GMT  
		Size: 10.9 MB (10864854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5060f40e5633e0da43ddc4c612bcf9056f77830cacdc2818425c8c67dda62d6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75755580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9023a8a5fd8327d0dd9353de0936b8ed43f0428c5af59e0db07a03ef32bdbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:33:07 GMT
ADD file:976d560bd7f7860fcfb64f49aa1043a087bc71ae5099f0cb06a93ac6051ac5df in / 
# Fri, 12 Mar 2021 02:33:25 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:25:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:26:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45911da2c88811278c7ef0cc34bf94d713837727d8059f205da3332e2aba2766`  
		Last Modified: Fri, 12 Mar 2021 02:47:13 GMT  
		Size: 58.8 MB (58753842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea21134dbd57e532f752628fc40c5d7fb196f24a6a7c14d87635986a6cf0bee8`  
		Last Modified: Fri, 12 Mar 2021 12:06:51 GMT  
		Size: 5.4 MB (5386609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe41bf7ec41499507285e048756dc75193e211029867c6225e54a5a4f4becbf`  
		Last Modified: Fri, 12 Mar 2021 12:06:51 GMT  
		Size: 11.6 MB (11615129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:360894b5a2791f4ee8d9873c4fd75728fc0c0d767954b9cda2900598b124ba83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68990681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c165265362e0422d13e03e5147bec7cf890c4166df830614f4b7e772a47c962`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:46:21 GMT
ADD file:0ca8df72ab8a25212bc85ec53930c9285a0c63ea73409a2e42e8749af8d051be in / 
# Fri, 12 Mar 2021 01:46:27 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:34:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ae111c7645dfe78b7684eb4252c76f987ecccd3b0e2f8bf675e007362fec66fe`  
		Last Modified: Fri, 12 Mar 2021 01:50:46 GMT  
		Size: 53.1 MB (53116371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab6e9aed411053c58f4976ffb587937afb07a3caf34682be859f3e490c4e450`  
		Last Modified: Fri, 12 Mar 2021 02:40:31 GMT  
		Size: 5.1 MB (5121396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737e596c1c60857e5f5203de639f8591e441767ca10e8f3d18691ff699891e6`  
		Last Modified: Fri, 12 Mar 2021 02:40:32 GMT  
		Size: 10.8 MB (10752914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
