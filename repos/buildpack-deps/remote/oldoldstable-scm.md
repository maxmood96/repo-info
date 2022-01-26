## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:7bdc390e93b915a4ad51ae06fd82629070385cfa0e259a65b8b3735a5269a24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5bdb164e59aa280f23620771dce6c3fd3637a843c9976d6cc1e715117b69acd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110788104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560f16a854cc144196c5a9b8658bb0d3f8f8bcfbbca3b7615d1a64832843c82c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:44 GMT
ADD file:8486e54cd9c7f48cd93b4dc399b71f2053aa61655dcc37e06a9274d4878408a1 in / 
# Wed, 26 Jan 2022 01:42:44 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:17:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a834d7c95167a3e129adb00a5ddbaf5d3c035ad748ff7ee1273373d150457820`  
		Last Modified: Wed, 26 Jan 2022 01:50:37 GMT  
		Size: 45.4 MB (45381397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3fa6f1b88b95ac6adeafdb618011e672d4c9f5637b92be373276ee7e066dd`  
		Last Modified: Wed, 26 Jan 2022 02:26:13 GMT  
		Size: 11.3 MB (11301881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778df3ecaa0fbba90d3a7d88947a4376ebdc7e2fcf8a4b5ce43b3c699faadff6`  
		Last Modified: Wed, 26 Jan 2022 02:26:12 GMT  
		Size: 4.3 MB (4342406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d353c340774e155d838e2e0f0952201366cee28591b065b7d328fde7bc72e034`  
		Last Modified: Wed, 26 Jan 2022 02:26:33 GMT  
		Size: 49.8 MB (49762420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5e40566e4b559c3c5c309db6fb2eb973afbc20a30a8f223b99a6241b8d722d5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106590022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ead94578c1aa46ac708a423dbcdf55f1c707aac0e51a9010a1c2d392c6888`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:47:04 GMT
ADD file:f9ce41b640f98db33431f520d66468b33575b20c5247749d76dc03214f1a92c3 in / 
# Wed, 26 Jan 2022 01:47:05 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:44:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:45:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81c5e7cc968aed78bd97c17445dd362c3dac0397104fd90548cabfafde2c64c0`  
		Last Modified: Wed, 26 Jan 2022 02:05:19 GMT  
		Size: 44.1 MB (44091791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b75993187fe65689a3ef56f900036b8f43234e10bb71bd0afffc124ea0518c`  
		Last Modified: Wed, 26 Jan 2022 03:04:21 GMT  
		Size: 10.4 MB (10352067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa9fe1cd41c295218d445675d34d1e730babea880e423ef7417804205d3301c`  
		Last Modified: Wed, 26 Jan 2022 03:04:17 GMT  
		Size: 4.2 MB (4161436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf0eac769bb01ba6d9f71a1196274c57ee40589cb35ff3bc84fae7292573583`  
		Last Modified: Wed, 26 Jan 2022 03:05:09 GMT  
		Size: 48.0 MB (47984728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dd7ea57495307e86bec3eca4f0ff4d35bb743463c21ebe8a6ef7f4d5e0996581
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102120680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c2eb296539174d21ae2b180358d9f348b659ff2908dabb724d6cdfd2af8d06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:07 GMT
ADD file:60b016ba67df7136a5c9120c3bda872fe6fc9264670eaec4af04649094d2c53d in / 
# Tue, 21 Dec 2021 02:05:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:57:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:58:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1680a7a0944ad84261b1979d7a37cbfaab55a5d7841917a0fb9a78ccc086ee83`  
		Last Modified: Tue, 21 Dec 2021 02:22:04 GMT  
		Size: 42.1 MB (42116934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feceeddac91e698bf009a378cca3bc65e3bee1199adb92912590e31192ac0437`  
		Last Modified: Tue, 21 Dec 2021 03:20:32 GMT  
		Size: 10.0 MB (9956591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee13a902270fb35c27560bff16e80e54c7122abb938b35cc5188ca753ba23cc`  
		Last Modified: Tue, 21 Dec 2021 03:20:29 GMT  
		Size: 3.9 MB (3921249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cb66d53e7811ef080c8e19ffc98281d9a7e1f083d7f574f6a709b728c2fc01`  
		Last Modified: Tue, 21 Dec 2021 03:21:16 GMT  
		Size: 46.1 MB (46125906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dea906b00f22ed3e5dfd17b8ad9270affd1b4da4141050a527dcffb9e9cd5508
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104998486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b1c5ebb55c0bb566b9bf271293ccf1fd364a606e6c324a84a25cc32d05a8be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:44:34 GMT
ADD file:fc57ceb549dcf9223a7806f1dbd83ede31ad1705eda04387f43795b8949b19c4 in / 
# Wed, 26 Jan 2022 01:44:34 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:17:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:17:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:18:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11cbe372cf332799e1339b2b8a04723e8224eb56d69212a1308d1df0da55eae2`  
		Last Modified: Wed, 26 Jan 2022 01:52:53 GMT  
		Size: 43.2 MB (43173725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf576a0611a8862b3ac5cc25b79aedd7b2f5a1a457ead352a467fa5b906d0f6`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 10.2 MB (10216892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc21f7f695aceaf60c5d2590b7acb0d3937aab7af8a9470dd74605632805610`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 3.9 MB (3873916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16466baa01cbf2b86dbc5f9f876247c80462e423aa7a6b68dfec79de47f85e9e`  
		Last Modified: Wed, 26 Jan 2022 02:27:43 GMT  
		Size: 47.7 MB (47733953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1bc3b47e557f94465346bdcab1523ac0be6ad278a8351d305016c1518243e5f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113287583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438e16f645389372aaf4adad8870515c9d8fb744bf6359aa6147561bca9322d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:51 GMT
ADD file:84c4f9ca5f39d4d5afa373f2ef32d0a65a614861bd5e53fe072387283ea5901d in / 
# Wed, 26 Jan 2022 01:42:52 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:22:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:58d50d1151db66fec3407a887e75ea0080e2b06c23447d1aa582592c9fbd7eec`  
		Last Modified: Wed, 26 Jan 2022 01:53:54 GMT  
		Size: 46.1 MB (46097933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc62fa793c6ec57e2be9c7b8ec84514c2c0118cdbc2b4336ee49f720fe729c`  
		Last Modified: Wed, 26 Jan 2022 02:33:31 GMT  
		Size: 11.4 MB (11359514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1167f9e9e1ee3be249d14a5d199dbb303b25457deb6ff54ac1887165400cc0b`  
		Last Modified: Wed, 26 Jan 2022 02:33:31 GMT  
		Size: 4.6 MB (4564913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb5396177d46c4d42762f2b25f0a04d0b1af759b32f35024060a9e5945b4400`  
		Last Modified: Wed, 26 Jan 2022 02:33:55 GMT  
		Size: 51.3 MB (51265223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
