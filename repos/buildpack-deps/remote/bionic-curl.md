## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:f23bc5a2c3cc20b1cec24a4735c09a756c7a7da7705f85bc32c8c18ce427676a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8221eb88fdd8650ef9b020c20bc44db33633c51259d942bf8f36a7026a59b7b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bb4e90337bafee1eb7172c0bb81e43bda23dc37d7a644f401cfbbcbb0816e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:02:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:02:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2c4c0515b34e36078574315ad974d4563e24d45b76bed28c008d4b84af5d5`  
		Last Modified: Fri, 07 Jan 2022 03:21:56 GMT  
		Size: 6.6 MB (6642245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc31a01cc6d078f111f123161ccaca397151a5fe113d9a8c6a47e3600d02b03`  
		Last Modified: Fri, 07 Jan 2022 03:21:56 GMT  
		Size: 3.0 MB (3022839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c82094304cec5557f94754da88889f4b695c05d9d3c3406e21547375b45cae88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30600596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746a3a4add4f4a5e006398a8be05a30b8164784efdd91dfbe92e46f6dbe131f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:03 GMT
ADD file:04c050ae3b998115f9e3f0da295a93a62bdff5d2efc3c37e792665d263cbf804 in / 
# Fri, 07 Jan 2022 02:26:04 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:51:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:db4feefed17933b9e08cd0d0fd6c63db5c115552848576f2bc2062c8c5f69628`  
		Last Modified: Fri, 07 Jan 2022 02:30:10 GMT  
		Size: 22.3 MB (22303634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7effbe8b0ef2fabb2f78579f400c46d711622f00f77feb1ba43590d049ef323d`  
		Last Modified: Fri, 07 Jan 2022 03:12:31 GMT  
		Size: 5.7 MB (5712218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369e7c93d7c89dbe2c27677cd5cc7c33d18491e2f71b55a48bd815d221643f50`  
		Last Modified: Fri, 07 Jan 2022 03:12:28 GMT  
		Size: 2.6 MB (2584744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ff1164a51cc0ed649388396a82ab8b06993a86296f64d17c4e2de46e9537f113
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32379659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632f5b7554c54c75e0e34ef6b7f7f4a252ba6bfc16dbecbfbbf93f5024f38e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:18:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:18:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7212d104ddd6ac7b61a9dab6652696a5e0a7c8e59d4ccc1aab1c318f4e912e8`  
		Last Modified: Fri, 07 Jan 2022 02:28:12 GMT  
		Size: 6.1 MB (6082562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be7d81b14f1bfa58b6939ab7ec75458169ac7eae4f05ef867a6d088985c9e32`  
		Last Modified: Fri, 07 Jan 2022 02:28:11 GMT  
		Size: 2.6 MB (2570182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:229b77b2b0f8c80ca466f1f8d84becb549971bf5fddfa8debe198ff0eabf21e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37338755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0355fffb801a5ccf862b4938fc1b6332da697a1394020e84a819e1d781b8ac4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:39:03 GMT
ADD file:4992040d291a9a6b53435279ff532c15e004fd7c7b35aa4783850a06ccff0694 in / 
# Fri, 07 Jan 2022 01:39:04 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:01:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:01:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cd8c855b84a6297384d4a364fec672137f3aef84749b319ee5158b568545eb0f`  
		Last Modified: Fri, 07 Jan 2022 01:39:50 GMT  
		Size: 27.2 MB (27156435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e486905508589dc62500a1d530f1012b6b203e72ca2e07d9c8b267282daa2e`  
		Last Modified: Fri, 07 Jan 2022 02:08:02 GMT  
		Size: 6.9 MB (6930197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908bb3b2708daae4e8c3f613f3461f07d608b18560a647b4cce654f4ef141c18`  
		Last Modified: Fri, 07 Jan 2022 02:08:01 GMT  
		Size: 3.3 MB (3252123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c4cc55ef805e82ecb6ea0e7ad084e5f5bede047a2840a952eea1dfa397b7aa21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41207959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7487c7e66a7fc60ae2b7ea847a03480de5596b74e78937e2a0d71875010cdb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:41:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02cf98deb89a0429afce514e8acff660769c377b62a27bed4ac9461d5fb3d05`  
		Last Modified: Fri, 07 Jan 2022 03:09:21 GMT  
		Size: 7.1 MB (7056362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb8c7ad2e71ddbe68b162a1dd387cc107143935937ebd41ba87891667c78553`  
		Last Modified: Fri, 07 Jan 2022 03:09:20 GMT  
		Size: 3.7 MB (3719250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab9f586374c96439624ce9f3d97ffd436a47fba3185d3d4091047b413a0d23eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34669694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee966c5b8d29ea677220688e6ca754cf3e067f11c4aaf32d3c1dcc80991fcdfe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:09 GMT
ADD file:caefb9be68fabe0b9b7dba683dabb869e5165a5a13534742d73a489a3712d9a9 in / 
# Fri, 07 Jan 2022 01:42:12 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:01:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:01:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7587f9252eef493a02840102ba78c74de317d3d47f6d568af5602ff6c1c54a20`  
		Last Modified: Fri, 07 Jan 2022 01:43:57 GMT  
		Size: 25.4 MB (25362136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51aa6028c0bcbca283acef11857a9719bfcf7c326e520202a60fbac277eb02`  
		Last Modified: Fri, 07 Jan 2022 02:11:43 GMT  
		Size: 6.3 MB (6332575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372e9a53b61e00c123206d32eb8d2114f344704896c85db85ac39b155313e3f2`  
		Last Modified: Fri, 07 Jan 2022 02:11:43 GMT  
		Size: 3.0 MB (2974983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
