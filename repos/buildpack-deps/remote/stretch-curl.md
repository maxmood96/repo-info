## `buildpack-deps:stretch-curl`

```console
$ docker pull buildpack-deps@sha256:98082ccb103e0b911ceef3c693d09c89cc8d44b92f465d55d42c85e7b77fe284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stretch-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:95304de9c06dc70d62a8ef8679135de133b9b7d6bb7bb936e642c8bf246e98e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60513408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c7bee01e949e704dd8e19f734bfbeaa0b1df25e6057d0cf968a1d0925655a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed671951175759663951474a95df46cb4411d6a1511548aac8ec72e8ac487946
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58092600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831e48da4a32278cf7a47f9fbcdfd73f1df41079c3dfb38f357323237d3fd3ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:53:01 GMT
ADD file:5ed8e2bc0bf117a359d81b052913e99f6139d0b36e5798d75392429effd5afd3 in / 
# Wed, 26 Feb 2020 00:53:06 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:54:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:54:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3294d23573097fea5f2d79377bc86444ebf83e4bed50a8a6c62b7aa8637dd7fe`  
		Last Modified: Wed, 26 Feb 2020 01:03:12 GMT  
		Size: 44.1 MB (44066613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952c5ec5882944f0e3977bb3d28960e53c97b7c4985863a7fd5b7c33b3a309b`  
		Last Modified: Wed, 26 Feb 2020 04:05:26 GMT  
		Size: 9.9 MB (9866766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6614c3a732af22df2caaa8ead40737dc17a198f0ee9d057e6e53fee7f9f12`  
		Last Modified: Wed, 26 Feb 2020 04:05:23 GMT  
		Size: 4.2 MB (4159221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f362610572b0bc24ffc7f9658277cd5c1cf3181aac33d974ad14075f795b58aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef3f8c2f6efa9048352ddf2e172b1e49ad1b98fd28cc13c4b5a2aa7d27ec87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:69498d1e66155e0fae276a68b153eeacd1d0e12a74acfc3ee0227aac204d43a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57001092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5e38424c0e457698584cca9b5af597106bda99b03e17bbc900ee39ef67f79c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:21a0af7e53d868ee670fc04279ac4a7ce4f1f4a7e92d4954ebb5c805fb93a529
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3f3557b441d130600c216b4de596884be184ae6bea75750f4e9f9454df63f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:34 GMT
ADD file:a2d15d4f5721611194d2e75c068cf76220a1fd273b28e60afc9d97c41920f37b in / 
# Tue, 31 Mar 2020 00:42:34 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:25:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e23f42c0de4ea650702adc216b9d71349a24439e774c0bbbb00d2ad19aa304df`  
		Last Modified: Tue, 31 Mar 2020 00:48:31 GMT  
		Size: 46.1 MB (46095182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8aed54eafba002eda33cfdc543523b6ddb486d1a0cbca690ff815f53d50e9`  
		Last Modified: Tue, 31 Mar 2020 01:32:58 GMT  
		Size: 10.8 MB (10818153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a1db665f4b770126afb4ccdc427fae19617bf624b95982ce876d0fdb478291`  
		Last Modified: Tue, 31 Mar 2020 01:32:56 GMT  
		Size: 4.6 MB (4561461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:700e252c3af51f0e445130c7c191c7a1deb2c0a49e1a69cbb3999063313e0404
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59946378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae55b305f093c50fd3d48b511ade282cb29bfbbcfbc728b11088441aabbef329`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:36:21 GMT
ADD file:734d2a25bec5d510e72f822b21a5ef5786a928c6cb933209a04c6358fd600b67 in / 
# Wed, 26 Feb 2020 01:36:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:31:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3a8babb46b416d2208716bc29bc3e805dd074b943418fc44ac89d66e363bc68a`  
		Last Modified: Wed, 26 Feb 2020 02:03:30 GMT  
		Size: 45.6 MB (45647081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58107739cb9bc4ee26b798057c5699d3917b41fdd5074d870c116173ef2b88d`  
		Last Modified: Wed, 26 Feb 2020 08:54:46 GMT  
		Size: 10.0 MB (10002548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a9dde531080020a5aecc53631e693820a9b6870602303e1eec2d17f6591e1`  
		Last Modified: Wed, 26 Feb 2020 08:54:43 GMT  
		Size: 4.3 MB (4296749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d1df6d48c5a2df2d9c8b0c7a6f8e40a15ba2090483fb0849140a6aaee76d678
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59931446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea2f003a2dc1ef03fb619555d79d79c6fd16566acf595b65f5b819e651bad6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:44:30 GMT
ADD file:bb76ab55808bcd0567a32c3d7328d5c1719147f0f723a4aa574872eb8f12b4d4 in / 
# Wed, 26 Feb 2020 00:44:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:42:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:42:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a2baf8ed1bce68a4f36469f3537f12b9e5bebc860ab4aac0954714901595c575`  
		Last Modified: Wed, 26 Feb 2020 00:49:08 GMT  
		Size: 45.2 MB (45232848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58b9c529db9ec73f2bb8ba3f678b389c4df7bdb3ff1083ebf516aee839533b2`  
		Last Modified: Wed, 26 Feb 2020 04:49:17 GMT  
		Size: 10.3 MB (10325927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d9d2deeb51ba62efa7f9206911520eae29fdd6a401851f5f400f881ef0fbc8`  
		Last Modified: Wed, 26 Feb 2020 04:49:16 GMT  
		Size: 4.4 MB (4372671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
