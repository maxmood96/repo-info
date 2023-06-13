## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:dca27b3662376ca8161b72b79bd1fefd9484c1fa5d4f3f3322c0c644eb434a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:96930574e8e23fc3aba9308a51b92f334209d77878ec5ce3c157dc408663f631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68027730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0aef6fab6bc9843476c668743258f76db1c92e3d473f1305386f8fa2d713272`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:19 GMT
ADD file:54838b3dbf7839dadd0b29835bbe53ecbfdfde657ef8671ec5ac3cf5867ea069 in / 
# Mon, 12 Jun 2023 23:21:19 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac8bb7e1a32398e26c129ce64e2ddc3e7ec6c34d93424b247f16049f5a91cff4`  
		Last Modified: Mon, 12 Jun 2023 23:26:48 GMT  
		Size: 50.4 MB (50448512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c264c0ad4598c25048a6dbd3030086cc5c74000e11d04ac27944cb116aabb`  
		Last Modified: Tue, 13 Jun 2023 03:38:30 GMT  
		Size: 17.6 MB (17579218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6684c3a5a8aaf2724956d65259db155e96babbb51d80e77a34fede3df2e8eca6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31370911de88492fbee3dcef81f1474d3d9afc367e0f1ba505015a9eb5c22005`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:02 GMT
ADD file:c3ae258462983c32de8d633c17dcc414087b5ccd8fd76f708981c7f20c7e86a4 in / 
# Mon, 12 Jun 2023 23:59:03 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:51e8b9db05761e5bb6c498f0c3f479641e693e39aac9800c97e87d5c936ba9ac`  
		Last Modified: Tue, 13 Jun 2023 00:04:43 GMT  
		Size: 45.9 MB (45916072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9e979674a28bf584e41acd517729c9aa3b1d14d2f629078892eba0a0734b0b`  
		Last Modified: Tue, 13 Jun 2023 05:04:38 GMT  
		Size: 16.2 MB (16211260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4a49b101c69650ebb15ae82e6416ca7e17e930378aad79f13055051257fcd28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66688446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bba7ca73a04727e5f8bd4ec371071201cbd09fcdb0fc792396552aa690bd1b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:41 GMT
ADD file:bb3cb9e6abc423742d7c1b6bc006a7cef70038c5621c71a90a2ae7c1ea29ec63 in / 
# Mon, 12 Jun 2023 23:40:42 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8371d57f7426517aead21bff5af0cf321625cac166c86214c439fb67db84243`  
		Last Modified: Mon, 12 Jun 2023 23:45:01 GMT  
		Size: 49.2 MB (49238409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7349847b3241e237d7a69174fea45593592e320324afdbae5c685b0a96e8181`  
		Last Modified: Tue, 13 Jun 2023 03:09:21 GMT  
		Size: 17.5 MB (17450037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aabfd541800f37a4e99f609a08a1d077da1a5a6b9bb19b6c677d4e410170da6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69301550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621e73f576d1f388cdf59f1c4f83aab2cc64c3423d532152c222c81ab8a0a95a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:16 GMT
ADD file:c4d7ce8374a492278fd0b54ca10fd35f995676380e4ef134e484fd85ed50c58b in / 
# Mon, 12 Jun 2023 23:40:17 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:121d519ab26049cf059ad8c480f995a2bb103d39a5b57857d7ac27ab2b0d35f0`  
		Last Modified: Mon, 12 Jun 2023 23:47:27 GMT  
		Size: 51.2 MB (51205988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0d6f2e6e8ec2df89e5e0129152319fa3c75a480f6083c74b8b54ccde31ef32`  
		Last Modified: Tue, 13 Jun 2023 01:13:59 GMT  
		Size: 18.1 MB (18095562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
