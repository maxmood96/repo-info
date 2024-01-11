## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:1cc50972533423a4b037a7c3e4084150894861d89eac733c5218c7c5451f6814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:514e58f54bdadf582d51ed14d8139df6e08f22d7f48fd374f222c8e8c316ad5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119962645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaa81469ea33323b1337e3bb8f591bb50c847a65a2dc316ec65793516f5d810`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:27 GMT
ADD file:ac13007eb56f6e064fe27101dfa666f02b04f4ce9a2bcf3ade6cf6055562b7e8 in / 
# Thu, 11 Jan 2024 02:38:27 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:38:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7418de5ce68f67dad705c01c70a7bb811f9b886f8d7aac2b66110d376046fdcb`  
		Last Modified: Thu, 11 Jan 2024 02:43:26 GMT  
		Size: 50.5 MB (50500254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5caad11564dacebdfbe4a52e47aa5f32a8064c74da57cbd81c082761a657bd2`  
		Last Modified: Thu, 11 Jan 2024 04:46:40 GMT  
		Size: 17.6 MB (17584913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7615c88945cec92f7f96663069cbfcf2b0dc1fe60bec4e939e55d85382c88e`  
		Last Modified: Thu, 11 Jan 2024 04:46:56 GMT  
		Size: 51.9 MB (51877478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4b8b4c0b6daa54f8e0cba9808f973e5dc925748dd8bb0fb0eee057ae813ca566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109594192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773b971ab46e2d8a20c794c0ad0a62266a3f551e3b6d5eab7a29af9bb463fbab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:52 GMT
ADD file:7f9fc3dd3778509079c1f4010b0ef89a6910aa3a83b317c5134489675daccb47 in / 
# Thu, 11 Jan 2024 02:42:53 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:18:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:19:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c11d78fb5679ceced7c7aa83357081cad2ce04776bc24c72152ce12e6b5b8411`  
		Last Modified: Thu, 11 Jan 2024 02:49:46 GMT  
		Size: 46.0 MB (45967605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf675975f6adfaf2c5b813bb5cfaf951a864bd6c9f1cb87e7622e2381bdf947e`  
		Last Modified: Thu, 11 Jan 2024 03:31:37 GMT  
		Size: 16.2 MB (16216537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7908e6bb56f5fd563f9fd988126258215be6efb8f65248027684accc2ec7da05`  
		Last Modified: Thu, 11 Jan 2024 03:32:00 GMT  
		Size: 47.4 MB (47410050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6d5f9cdd42f852bed56509b95bb33f0138d007002f27f5b411f8df71d05d3d76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118953665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7350c2c27b8bb9ceb4dec1b1505ce6f5ad07f9f7e7ceabf265dc1b327c3e225b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:31 GMT
ADD file:df5e5dd39efc6ae3cc9132f6ca6bb569731f7a37cf4b41f87bcb7aa1ba9771e8 in / 
# Tue, 19 Dec 2023 01:41:32 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:36:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93507f9712ced9fbfd0d0f689cf7b55fb245cef88530c07ac5dc5cad20fa889d`  
		Last Modified: Tue, 19 Dec 2023 01:45:40 GMT  
		Size: 49.3 MB (49289026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d548003bf6042e58cd00488bd9dec02acb1fd956797b04f2aacc5f11f2e1a6eb`  
		Last Modified: Tue, 19 Dec 2023 11:44:06 GMT  
		Size: 17.5 MB (17455285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eb6e6e06a1244843fc7372bcd9203e91c1434ac505900a1ce0f6c242e66f8c`  
		Last Modified: Tue, 19 Dec 2023 11:44:20 GMT  
		Size: 52.2 MB (52209354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f67cd37099b16dbc793be42462097fe4ae0b8386402cb4cf389bf82c4bc7b583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122846570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db3b144c11911c659796271ad884836d45ec7082efcb6a4703f749b651c84fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:12 GMT
ADD file:1e68cfe2a77ca5be656fe9cf5a3e89e23630239ebc044ace148ba49124dbaf7a in / 
# Thu, 11 Jan 2024 02:39:12 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:34:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:94764bf084b89ee796b567eb9a1b71857d957204137c0ec8781723a4b7ae71ae`  
		Last Modified: Thu, 11 Jan 2024 02:44:28 GMT  
		Size: 51.3 MB (51255203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002489140685fac56869096dde7388de7e568f955020400561fda107e627e1aa`  
		Last Modified: Thu, 11 Jan 2024 04:44:28 GMT  
		Size: 18.1 MB (18099537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0f566d9ad2952e86549c70077da7291b2e25aad2f8980fc09b153723515edf`  
		Last Modified: Thu, 11 Jan 2024 04:44:51 GMT  
		Size: 53.5 MB (53491830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
