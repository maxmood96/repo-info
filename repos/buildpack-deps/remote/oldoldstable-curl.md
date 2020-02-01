## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:38b103852acf9127058aff021ac323051a9c3e6d754e9f191886fedf916a1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:48c1eb6cb8769434c89c194c34266140d5225d78e8d45833eb001bcc635f431e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71935125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dd2448f7dae10d9cb32766ae016f3b2714d8070b98ad4afdd241c951d4929e`
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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b3a093758699a05f34d6354ead4f98e34f313bc886b22273fff31a180ace37b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69616119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2fd4ee65d1add1616a0d363ac308d6d6b423671d419d6741c047a5793fdff0`
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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da5aa38c89ba729ee70fa4c15f0c405336efdf49c21bcf6ad504f89f9a54fcb1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67025692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6c602b98092724202fb347bd2f856155e05607d7c71f47bdbd9b6fd46ad51`
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

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:afd6c0b408abaa87ad868cc96e979395925b8a335c80c2762b16198332206aa3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74463018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd7d990691d8b4eda0baf3da9655cc7f9a929d30387ccaa67e9dbf3813c04c0`
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
