## `buildpack-deps:mantic-scm`

```console
$ docker pull buildpack-deps@sha256:6a0768411a6c535217dfabf03ff5464b983883f7e1c5c27e3308829510240642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:81eea3a083e927c796cf1a1cfd206ee47230e74a1a4dda087250bc6818c3adb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82717366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3040c9c01a0950ab5034711356b474bf3e84c8de87f367263fe4ddd07ec472c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8496cd0ea1eee2817b0144b138e4851ca29d675473addef86c4d5838b98b10e0`  
		Last Modified: Tue, 30 Apr 2024 03:34:40 GMT  
		Size: 28.0 MB (28037242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90001033f98f32d73d26d33545975169f4a8186beac4819ea4fde58f38f27815`  
		Last Modified: Thu, 02 May 2024 02:13:27 GMT  
		Size: 9.9 MB (9911781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d673a81eea47677f1c20cd613c42d148d058da96220692d2550e23112c34d7`  
		Last Modified: Thu, 02 May 2024 02:13:44 GMT  
		Size: 44.8 MB (44768343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55bdd449697c67e888d8aaa1e151f301722259cb59ba96865713a1352ca3fe00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83790239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01db34a3fb8448e54c3d53a70a5436766d8d612ec202345af6192201106c43ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:05:53 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:05:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:05:59 GMT
ADD file:36a9fb96170feb2e8bb6dfda0793b5f7069593502c61024a6ed3d84eb01afdaf in / 
# Mon, 29 Apr 2024 16:05:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:57:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:58:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c14f7cb79524b2adc26e658f09be736a2820a009c0cf783b8204bd8f44ff6dd1`  
		Last Modified: Thu, 02 May 2024 02:11:20 GMT  
		Size: 25.7 MB (25687736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891e062e56c3529de217cc9c1b86c28a85a8a887411ef56e0566d3b280203ff0`  
		Last Modified: Thu, 02 May 2024 02:11:17 GMT  
		Size: 9.2 MB (9152040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922394cec4336bec66ccf4cdc7027a9c41f90dcc87336a1ea3fae1ca7dd15295`  
		Last Modified: Thu, 02 May 2024 02:11:36 GMT  
		Size: 49.0 MB (48950463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:331bf00820eeec0cbbcc12c966faaa6bb6667778ca5156c8a0cff2c20f6860e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81725841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0114c27efafda64b1f7afcd4f413ffd143b933f5d3bcf91b8ff9e3e9c4e082d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:59:01 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:59:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:59:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:59:01 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:59:07 GMT
ADD file:0766b52edac59a701a3c97d7372ee928210e45e682fc997b4e7f869a2136ff7a in / 
# Mon, 29 Apr 2024 15:59:07 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de30cfcb0b3c8185bc9bf88dc253529aa2f988dce372173b61c766339c7d4045`  
		Last Modified: Tue, 30 Apr 2024 03:38:06 GMT  
		Size: 27.4 MB (27380844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c434226caddcf2d26fded83051afc5a676600e1a811e0c60301447972450`  
		Last Modified: Thu, 02 May 2024 03:32:49 GMT  
		Size: 9.7 MB (9666068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be4c27558f1ae84b9ea479f94cc05da2332db46eb7f5f592143a723012da835`  
		Last Modified: Thu, 02 May 2024 03:33:04 GMT  
		Size: 44.7 MB (44678929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dcce2f50f4b4a8090fb614e2f2f3d5668cf40af43e3846a2d8a8924f02046df8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93498421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba177d55af5edbcd9f7f06745624a42b6fa82cb341f334f841668a39bf9231d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:04:17 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:04:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:04:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:04:17 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:04:20 GMT
ADD file:3eff778e5407e167e169212e204258e93e6574103bc6286f120fa1e790582498 in / 
# Mon, 29 Apr 2024 16:04:20 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:13:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1532b783baec83835efe31b4c05c574cf39a1e1e98d7628702e186198cf0ee6d`  
		Last Modified: Thu, 02 May 2024 02:32:33 GMT  
		Size: 32.4 MB (32350607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d677821ac7ae97f0fa4ec3f5603bc76de57322ccedcc962b6e6f80d05d963c8c`  
		Last Modified: Thu, 02 May 2024 02:32:26 GMT  
		Size: 11.6 MB (11585962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acf8b3c751d3b8dca105ecc98b21874e712adc45ccc949a1ecccedcc7def18`  
		Last Modified: Thu, 02 May 2024 02:32:50 GMT  
		Size: 49.6 MB (49561852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e78701138d0abc9034056107c0fd4cd1139e77386c6660f1dabfc03c8d660b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82904355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b250b68daf8d9f08f9003c47be350750eeca4465ed6bc7602d3569ed8317d532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:24:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae85e9169f00cfaac0525494fb8251c5f790089a9748fdbd34e5fec105e50fbe`  
		Last Modified: Thu, 02 May 2024 01:34:50 GMT  
		Size: 27.9 MB (27890933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e372ff38d547ce6c08db910602c662578b312dc24c86593738f583360e0613`  
		Last Modified: Thu, 02 May 2024 01:34:48 GMT  
		Size: 9.8 MB (9759011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f4cdf7791a613f05e9e4b51edd04a313f26fbe67c95bfbe74d9d933253a492`  
		Last Modified: Thu, 02 May 2024 01:35:03 GMT  
		Size: 45.3 MB (45254411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
