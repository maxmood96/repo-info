## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:167c37777693323e7a93c8702606b2d84492a87531d0732a6cf38c4eca9011b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8bb0ede91bb866bc02551af560ad8644dcdd65231febb9c300bb839ed06ee6a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81865253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581321af1d6702c782ad6a57542b51b06b27d26f3ef038704d9a381caa7952e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:43:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:44:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291e1ef8ab60792ae6cb1d242dd07c4ab478f68b32f81111e0c3d1c1929e2baf`  
		Last Modified: Sat, 30 Apr 2022 00:00:25 GMT  
		Size: 6.6 MB (6642632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da53fe0378831b03b11a50742623c9d4886df8f8abcd691d75b0f43820f4450`  
		Last Modified: Sat, 30 Apr 2022 00:00:25 GMT  
		Size: 3.0 MB (3022399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e99fbc9bae2e2851a9f7cd6830cfd1f3a847242b26bf595279a4eb683c0e470`  
		Last Modified: Sat, 30 Apr 2022 00:00:41 GMT  
		Size: 45.5 MB (45491114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6ea45fe8b9155b916f1a9f98e0191bff337683e724192b3cde269f098779507f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71290191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44369f2f504ae91e0fe1cea0e41d0ad97e845b3ee95bdf72a6ec9612dadb3400`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:23:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:24:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:24:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a73dc6c378126504521857c1f5b32849b1a6f778ad3be2ae05e85a203b1679b`  
		Last Modified: Fri, 29 Apr 2022 23:44:06 GMT  
		Size: 5.7 MB (5713646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882d05cf8d5563b9acf2592cd89c94aa437d95d40a15b9f67c62ac3754b6c395`  
		Last Modified: Fri, 29 Apr 2022 23:44:03 GMT  
		Size: 2.6 MB (2584817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3bf1f68a620a53fd64d163d712d07fb918d0e130f47c4b6d7c88fd12ab8d9`  
		Last Modified: Fri, 29 Apr 2022 23:44:49 GMT  
		Size: 40.7 MB (40691277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a98e25d55904a28a4d21cdb10eb7be2b73f38afaba5918a87891d78d0072b905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75679924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf8bb03cd2fe608dbf3393722f9e47a06ab462000a486ceacba9dfe4fa28460`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:14:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:15:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60798d5be0c4fe2a3b108def28399e64d3473055149c3b22fa62e931213239e4`  
		Last Modified: Fri, 29 Apr 2022 23:23:40 GMT  
		Size: 6.1 MB (6082989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbd896531eeca6d8cc62526013f972fbe235bd8cf006d5bc34901a7cfbb7ff8`  
		Last Modified: Fri, 29 Apr 2022 23:23:40 GMT  
		Size: 2.6 MB (2570403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1586d1e5563ecd2e705ff77d7fab291b0fff2765b68e0f69e0e1f9ead6e3a99`  
		Last Modified: Fri, 29 Apr 2022 23:23:58 GMT  
		Size: 43.3 MB (43291443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3164bcd93fea18484ffe93e3056bb76f85ae87d59e82d0ba584110f5948dc924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84220412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae352c28aa56532464f089bff77ef2bbb6c5de9821c75c4e538d54e20bf66b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:46:47 GMT
ADD file:bcce1e9e400660e474d54b70b67bc484a7976aff4e980b58d10ddcb4daa58a7f in / 
# Fri, 29 Apr 2022 22:46:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:04:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:05:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c49d5e021ef38e29480c34c86df22d89b9b63fe1a57ec4dd970f56497edf9a`  
		Last Modified: Fri, 29 Apr 2022 22:47:32 GMT  
		Size: 27.2 MB (27164138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00044d31281cf13c152f5e70253339f641f049c967eea3a67f7c7cdeda06e95d`  
		Last Modified: Fri, 29 Apr 2022 23:08:58 GMT  
		Size: 6.9 MB (6929613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb356e4b0392c6131483434a9739dfe5b56277b73834ac3ab909088b468daf`  
		Last Modified: Fri, 29 Apr 2022 23:08:57 GMT  
		Size: 3.0 MB (3038588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fc18cc175f54f06a86be36bdb54f6500bb57c2b579ac52b02e22742e3d58bc`  
		Last Modified: Fri, 29 Apr 2022 23:09:17 GMT  
		Size: 47.1 MB (47088073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:85f97a4fa99c43fc39f23187372745f308b34ed95c839ec43f2f5f52b96e1980
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94948027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcf3cb312add486e04df9adca8f2fabae20d0df0518932ec0b037275621383c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Apr 2022 08:07:45 GMT
ADD file:d5447cb8fcc4a12030e43cda74f87e1bec09c6d1093307e25164127500f5e0d9 in / 
# Fri, 22 Apr 2022 08:07:52 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 09:06:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:07:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Apr 2022 09:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00422cde8b22ee0ff419263739625132280d08ffe78075ad3fb44dd003fab8e2`  
		Last Modified: Tue, 19 Apr 2022 13:12:05 GMT  
		Size: 30.4 MB (30442273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d587db8c583825f01547d10158ffcd670b22090b1d7e22c4cc5e38a8d66de0`  
		Last Modified: Fri, 22 Apr 2022 09:40:32 GMT  
		Size: 7.1 MB (7056674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9dc57e211ce75e162542827ed82b7296b4e38b40d85577df3c9df74cc13ae0`  
		Last Modified: Fri, 22 Apr 2022 09:40:31 GMT  
		Size: 3.7 MB (3719458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f3d85745514e470e8c7feb12770beffb279852e12e73b52443c36b69c39fc4`  
		Last Modified: Fri, 22 Apr 2022 09:40:56 GMT  
		Size: 53.7 MB (53729622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9354c20468051c74cedb8b7bec1260fc31b926db368407685c214e2c05efceb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79711977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d13883041199e66098589606325a450c451cd74dccd4bc955f57d79a0e131f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:50 GMT
ADD file:9b5ddd45fc485b5c5ea3d28339d1768fa5d8f60059022a971897d51d94ad5847 in / 
# Fri, 29 Apr 2022 22:49:54 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:09:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:09:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1347a7b069ceb0e131b6f229b7b96bae189f8e4c594c1933170e278d0ed928b2`  
		Last Modified: Fri, 29 Apr 2022 22:51:49 GMT  
		Size: 25.4 MB (25365828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad71b6aca98ce06e987b76f0d613b62e64dffb408abae9b95415af2f7416c46`  
		Last Modified: Fri, 29 Apr 2022 23:18:34 GMT  
		Size: 6.3 MB (6333148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98f9a7ec2a119d06fe06667d3a801ec5234c7611b1d83200aa930c8c69fc614`  
		Last Modified: Fri, 29 Apr 2022 23:18:34 GMT  
		Size: 3.0 MB (2975210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa5c603c5ee07210bbaee5eff68c14fb9b0a6d3e78d239fff4de9d445cd34a4`  
		Last Modified: Fri, 29 Apr 2022 23:18:48 GMT  
		Size: 45.0 MB (45037791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
