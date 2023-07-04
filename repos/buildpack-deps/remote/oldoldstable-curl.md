## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:e4db303dbbcb1245358386f4d818e34c5921d5b416e5de934dc12c744d13cf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b9a6fa925c3754fad97e1e096b2107d8809a8c2786947ea28ebca51ee9791bc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68027808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba93f010c9f896ebc93161f6655c1b59d288182d9e9e6d2e1bbecc0f8c94e4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e4f798b8796023ecee944e089e79871ca261eedc4a2ee6a38b08418d9160f4`  
		Last Modified: Tue, 04 Jul 2023 03:53:27 GMT  
		Size: 17.6 MB (17579065 bytes)  
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
$ docker pull buildpack-deps@sha256:31a0d9c686cbc2328cd57c3363515049f391593d8dc552dea36b5acd6aadd135
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69301759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553a8774245bf544e4a5813eb3fc8b73b523c6ce15b6d5278ded782d365eab85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:11 GMT
ADD file:6ecab94f7cb2bc0740a669cfef73f0837a2ecf6475dfb0fc072cbd1a7f60ec41 in / 
# Tue, 04 Jul 2023 01:39:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:33:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b3c3fd2dd1697ce9fed8a2be0142b2d1294d424c56d0ce6d44bb8055d77e35d`  
		Last Modified: Tue, 04 Jul 2023 01:44:33 GMT  
		Size: 51.2 MB (51206276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0e83aa5cadecbd9663b4464fa33665e930f60918a3178f75983604fc64d38`  
		Last Modified: Tue, 04 Jul 2023 05:40:47 GMT  
		Size: 18.1 MB (18095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
