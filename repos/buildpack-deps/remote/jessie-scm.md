## `buildpack-deps:jessie-scm`

```console
$ docker pull buildpack-deps@sha256:55c5b5dade717808b7361663900eded8df5f3b10b9ba2be38951619336b1c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:07037fb4f73ae8dc88cc07066b0db4fafbb384ae2a19e244147474456716798c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115254413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8e3389b13ee35ce58259381d03a049bb8f3258185405c92f2ec484bcc956f6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:35 GMT
ADD file:6bea7fdf1d11cd3f2dfa923395205f70d42d388f597b21e289e7f516a2c687f1 in / 
# Sat, 28 Dec 2019 04:21:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:51:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:51:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4888a2f4fb02c1971555f590f5c9ef6369e7fa4599e586fb70cdfe80330370b`  
		Last Modified: Sat, 28 Dec 2019 04:26:07 GMT  
		Size: 54.4 MB (54389662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe6cef1db298eb80da7e99c0df1d8cf44011585831905df6373b5dbb32e0a8`  
		Last Modified: Sat, 28 Dec 2019 05:02:45 GMT  
		Size: 17.5 MB (17545463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d711a2398cd1349ffa38f874196cbe32d2cc4e6742bec566f58fd70eadd0138`  
		Last Modified: Sat, 28 Dec 2019 05:02:59 GMT  
		Size: 43.3 MB (43319288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bfc6f556ea97e05d6c0959e6f40e237482f6a23efb6dd1788f5af8f4a139f38
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110776295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f651f9ad0c4c09fdf826c86f0560ec0606537ab727985384b55f5eab5cf6e9b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:50:07 GMT
ADD file:d4edce93ba93edcd37d608a9b631879fc39506074ab425c75b3c55c68ce0f349 in / 
# Sat, 28 Dec 2019 04:50:10 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:30:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:31:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdba72d0442ed279b2949203d28c37c7388a87145a31eff8a5dbd1ec4d3f8dd`  
		Last Modified: Sat, 28 Dec 2019 04:56:54 GMT  
		Size: 52.6 MB (52579512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185dfc772e20f53d92109142b40655cb4ad05fd0c5a9d98fbc8588dbd41be3cc`  
		Last Modified: Sat, 28 Dec 2019 05:52:05 GMT  
		Size: 17.0 MB (17036607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e547a5aca6d1873224ad1dd685e40fb404e262be8dab3b9babd9a06110880f`  
		Last Modified: Sat, 28 Dec 2019 05:52:26 GMT  
		Size: 41.2 MB (41160176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:265ed7fd250b490f2298259e00f86cbeb67f9c16983a4fb8e3875b7aefc05c38
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106798183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9b30dbd4c0cb916e88a123a3972e910b44a50e32594ad1ad4104137ba8f506`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:26 GMT
ADD file:1e4262fa38cc66ad7a041517492cdebc1a6003d5abdf60247a62ac9b6e4f89a2 in / 
# Sat, 28 Dec 2019 04:59:29 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:49:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:51:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aea5fd044669abb13c109c414677bbdfcff8ede5c7702238c4f2ac6516aed8d2`  
		Last Modified: Sat, 28 Dec 2019 05:07:53 GMT  
		Size: 50.3 MB (50303019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d184ad45cae18544214bc702ca0f30ac229146272a0beb9a2cadb33e292754`  
		Last Modified: Sat, 28 Dec 2019 07:08:31 GMT  
		Size: 16.7 MB (16722673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419f61375e6a1502499e02be09f7c9c9ebd6d98cf596528d66dd2846bb8674c2`  
		Last Modified: Sat, 28 Dec 2019 07:09:03 GMT  
		Size: 39.8 MB (39772491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fa35eda655d911cef95b6d5199129b7ccc52f2d3c92997bf3896a797c38030cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118439447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4a1eabcb1258eea7553cd08d4229f8563b5a8de9f64ad5caf56c381c59c7f9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:48 GMT
ADD file:23c9537c86963e84613c942db01132e5d06384a5fd0b9f92595ecd7aeff0935d in / 
# Sat, 01 Feb 2020 16:39:48 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:32:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:605158be38a8eaa27411bc385ed7dcdc4884e9ad8da221b2c160b4dc702fd008`  
		Last Modified: Sat, 01 Feb 2020 16:44:50 GMT  
		Size: 54.6 MB (54607256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddb6eab72836c2f7baabe2d7cc8baedb1fd4b769a0b80c9bafac7bd2504cb0`  
		Last Modified: Sat, 01 Feb 2020 17:43:34 GMT  
		Size: 19.9 MB (19855762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297985b73d122356ed17677fc8b290e4f7868384fae0b731bb529cb8791165f4`  
		Last Modified: Sat, 01 Feb 2020 17:43:49 GMT  
		Size: 44.0 MB (43976429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
