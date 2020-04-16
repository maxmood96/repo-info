## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:cc0a553ab64000eae03d7c2c9e88c14224d6390eef2915c732d5dc83240f26e3
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ff0784a678e9218e95a227d47f2887c672bca4f110427348490d4bd3d735a61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60513370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f022c5dc898ce376d182e1be1b241e5a59f195a814588a40ce4ce2609470712`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:41cc552a0d75b3dcf1b2c9c201e633fe0f0307a702ed6c2bd66a211bec21ed6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58092338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a9dca4395b394f94a831ca7aacfa7dd99871570745b87b8045bf99c8249339`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:29:01 GMT
ADD file:5a406f17e0981025084e19ed83a5deb90ebcba048fe641c8273f340add75cb3f in / 
# Tue, 31 Mar 2020 01:29:03 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:40:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:40:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:442790510f4830e8d231c31971c1ad175b7d7fbf094edfb7914e6154fcd31434`  
		Last Modified: Tue, 31 Mar 2020 01:36:31 GMT  
		Size: 44.1 MB (44066449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c87dcd2bd87a418f8e317fa8e6c3f1fddfa90ea5ed4a77e7f1e67e2a0c6e9f`  
		Last Modified: Tue, 31 Mar 2020 03:51:39 GMT  
		Size: 9.9 MB (9866705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85810ebe9c6c3a63905ec14959badf92e7ee22150b33cf41ac37544fddf2b98f`  
		Last Modified: Tue, 31 Mar 2020 03:51:33 GMT  
		Size: 4.2 MB (4159184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f969bf48361eb06d6b5ebf48bd7b6581a629825444cbfe394bf16ba2e036823
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55518404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d75a83bde16af7f7f79274488f96b287527f3663352bfaf6e6ee7048638cb9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:04:37 GMT
ADD file:b83ed4f9f7c8b10eba728f85030722a771b39336afd7ff9eef2eb6b94791533e in / 
# Thu, 16 Apr 2020 01:04:40 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:37d8a5aac9ec54f7757e1243cff051c8372be0cf907e086fba2607e08d2a4135`  
		Last Modified: Thu, 16 Apr 2020 01:12:16 GMT  
		Size: 42.1 MB (42101227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f4f4abba4245745ee86a35473696f5ecbe961a03af35bd6f07b2253c3bedba`  
		Last Modified: Thu, 16 Apr 2020 01:59:44 GMT  
		Size: 9.5 MB (9498336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accf104e4ac412a36f3c1fc31fb94722661bf356ac878a4b502dc20086c8d2f`  
		Last Modified: Thu, 16 Apr 2020 01:59:42 GMT  
		Size: 3.9 MB (3918841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:04af41beb107d2590a775182f36baf88ddb66a9b20ae2aac54ced0f8a068e472
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57000973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ea89989cc7065432bacd02313968f1fba0c1bfd484f252b8022fb1d533b4ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64c50404ec21fdf8b6fe72868ff0915c901dc8afa6924c1b8eba533907a384f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d511533d7b62a50de0efe2f3434b4b5ec5f56fcab394a4889ed737afdfa276e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:06 GMT
ADD file:298a4dfec0058f9502705ebab6ca3787b1bcb5845d21ecfcd1771505b061b061 in / 
# Thu, 16 Apr 2020 01:43:06 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:aedad1667b3098c616b8251fdfca8170596731152b6043a01601df826b79b4e0`  
		Last Modified: Thu, 16 Apr 2020 01:49:17 GMT  
		Size: 46.1 MB (46094897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a13ff1ee1a9968ed086324092c33ec123f94ecb99ccede500342483418d840`  
		Last Modified: Thu, 16 Apr 2020 02:40:58 GMT  
		Size: 10.8 MB (10818136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cdc434eb33063a8439a59c1a179e4fa3c9d968ee9a3ad4e2ff12714e1b77b1`  
		Last Modified: Thu, 16 Apr 2020 02:40:57 GMT  
		Size: 4.6 MB (4561464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e6eb2d6b442020e7040b4fdac4748dc6923ce757c5d0fe7ae79fdfaa46f510f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59946132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf2aeff6a3045803945d342d91edeb3307432edd178582c0ebad7eabc1371e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:08 GMT
ADD file:88dd9829c8f6a5ba7164ab347e4b14c986122f77fa3881b5b5f9bd34f8e0a794 in / 
# Tue, 31 Mar 2020 01:36:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:46:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a7f28865f7aedbe572d508cc57c37cad5f147864f7c67c67a38458e070687420`  
		Last Modified: Tue, 31 Mar 2020 01:52:56 GMT  
		Size: 45.6 MB (45647140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b575341a09a9b1fed08dca01f194be6db272e3f2d161ea2edf0db64d8e706213`  
		Last Modified: Tue, 31 Mar 2020 04:07:20 GMT  
		Size: 10.0 MB (10002319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28423de192fc0e4ecfc04a57e531587e8876d098a124122748a8f55a842f3213`  
		Last Modified: Tue, 31 Mar 2020 04:07:19 GMT  
		Size: 4.3 MB (4296673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd461c2eec8fd175a12dbe458f6feb108a82888f39ab1db5a0333f21515e9ea2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571100bb5fc3ad197d73b30d1f8f132abc10eaaeb37374ea4ff8e875c68c5ecd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:43:47 GMT
ADD file:bf54e49d85edbe8d61bd9e868d71faf0f26b4474f23eda7b692abfaf7aea50a4 in / 
# Thu, 16 Apr 2020 00:43:49 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b4e6598a8ad88c3d661d89d6fda41ee33a54f3c6f16c4988cceaa6fd0afd04bb`  
		Last Modified: Thu, 16 Apr 2020 00:48:18 GMT  
		Size: 45.2 MB (45232626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb98b0a4ec56e95b4ba3f3261ba975cd69e2a0240149eb53e4bbff9739e272`  
		Last Modified: Thu, 16 Apr 2020 02:08:04 GMT  
		Size: 10.3 MB (10325610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c82c0f221bc14891b71387b7587fd4f2a615d339ecf0afadce350f82b3e098`  
		Last Modified: Thu, 16 Apr 2020 02:08:03 GMT  
		Size: 4.4 MB (4372651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
