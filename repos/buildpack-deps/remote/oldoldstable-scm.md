## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:5f65de717996d98e84c83a6f99d872518ff52ff91876c467fd9417a03ccc88cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:afb08259f1ac535fe88bee2b3ea208cf5e321631169945cfb0d00109ed848cb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119961448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c979f5a4a9e45af0df32e4796505a3108bb8a91bf411c99d5151ef267c8f2cf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bb813b9d3124da27383ff45f6492de797d07f073c38f205536ace4e3b5f28f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109593691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd9965cf8ab7101c1e6ca04853b5b09981b803c66d9eb7e33f70ab285d531d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39aab6618e942bfedf2bb38d19946ce54a60a0a9f12f57ccef3a1544738a2fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118968947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5383738d040fad2e19ce081951827835339766b7f8e2cfc59ae2ddd9af31369e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e77e8e4e30b24b55c8167c85c97b09013b5ff67ed076602f377d18d035b2ef98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122845788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4a9d785bc03f2e98c30ae7b86ec864c22b1f55134e641482adafe1b0883e72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
