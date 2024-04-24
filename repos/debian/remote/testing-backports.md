## `debian:testing-backports`

```console
$ docker pull debian@sha256:8b12138e902ff7ad48b7a4159c431925bebf89e0086d8eddb51f092886edf7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:90747a59dc0fa2527a066bc18d73d13978dd2adc4ff6f0376b2f942f026bdbaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52338863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4563224c560a1ec5ea76eb4492bd726b849c0f24477fd16f8b269ce2d1423a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:21 GMT
ADD file:b8a11a0dc4e697e9f924afdacd33c6c1a4744e43ff2938c4539b5650bc3207a4 in / 
# Wed, 24 Apr 2024 03:30:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:30:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:efa2370e55f34d719cde5ccb31ebc8ceacbdfc1b76afe2aae60adf06d58474c5`  
		Last Modified: Wed, 24 Apr 2024 03:36:14 GMT  
		Size: 52.3 MB (52338640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb02be9c6475422468f1a6ec57dfc19cbc07fc9854b7ea3c6c5a7a35730bb54`  
		Last Modified: Wed, 24 Apr 2024 03:36:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:99e203c1b22586c558b2905b09c09784384239e605965aa154d32ef7e56640b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49434473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a8aa9eba99f8698dc9334a0fb9e249b5150e838ad3247b9bfce70e8e9e9879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:54:29 GMT
ADD file:c3db8fc0ff59085c8a63328ebcbc648547c629d90d57b3a48611023b5a50b02e in / 
# Wed, 24 Apr 2024 03:54:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:54:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:042fab6e37f5af2e0c7f5d334915ff89610f5f4aaf8299d53b355a0726af2814`  
		Last Modified: Wed, 24 Apr 2024 03:59:09 GMT  
		Size: 49.4 MB (49434249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eb3aca6a539f0e91cb4aba558abe08301e8cf4fbbd855b784708c992ccaa98`  
		Last Modified: Wed, 24 Apr 2024 03:59:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2644f59914d139c9bf985670e55a581aa802f928d2148b0dba8dcaaf8cd8168e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46930586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17b774cb61eb119f9f52a1ff077a757302c437911a57a2593fe3576d9f431e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:02 GMT
ADD file:2b4a467dc630bd5a96cfa038ee05d8ed4302bd61d17bb3a98fcc98c0ab904610 in / 
# Wed, 24 Apr 2024 04:09:02 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:09:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:78ad51e512969e922ddb678eb808c8ec3053c79958e7142f172d57bc5742d09f`  
		Last Modified: Wed, 24 Apr 2024 04:14:47 GMT  
		Size: 46.9 MB (46930361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8018ba14defccc8ca659651b4a240c758276dc672c4cab7d4f480f90c0c447d2`  
		Last Modified: Wed, 24 Apr 2024 04:14:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cee89b8967aac4600ee35b696729f5c6e4bbaca7ca39661443335f1b9a33f028
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52199660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a2b3d2597290871f1c42946111e27086d51610c34fd882a2d752b2579b8a37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:12:08 GMT
ADD file:bde6752542e4e995769792177622825fd367491a317b6d18fcf5ecee7e44bb26 in / 
# Wed, 24 Apr 2024 04:12:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad22d5f94f78d49cac32cb85d727d7c0ad9591d78322e8703c671bc6df55a2b5`  
		Last Modified: Wed, 24 Apr 2024 04:17:34 GMT  
		Size: 52.2 MB (52199437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718ebcd0b93ed9ccba41a4b3bfa47d58c51bda013b386757c21c08bbbccc0d34`  
		Last Modified: Wed, 24 Apr 2024 04:17:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:34916242197dd0462b519c22f16373c0b8efe44254bf0e4495f7848537f43f10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53187880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becf9d5adce55f572ddceab8e6c6ac18f8b7c7d9a1ae61a9607abeedfc35fe09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:41:14 GMT
ADD file:d13317359dc4242c5a65470d0b1543c04730a22315d52632ed08ef2845db1523 in / 
# Wed, 24 Apr 2024 03:41:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:41:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1467e916636bf828dcdecc6f2a8f3b0c6e5f5cfcf3e712bd2a089d157e42acb2`  
		Last Modified: Wed, 24 Apr 2024 03:47:52 GMT  
		Size: 53.2 MB (53187658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e16e26e11f2d2ad1079025cc1a908502e21d260ee5f6b5b5c3f8fcf308df691`  
		Last Modified: Wed, 24 Apr 2024 03:48:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eb994a169ecc345cf928f82aa93c46b6255281abf26dbcabb83e93c356e9585d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51411521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50c3d7e4063589a0bc8ae5163ef51c595e1bfc3ff3c2b8de88cc63a638fa57c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:19:45 GMT
ADD file:39997cd262fdb7c1ab86e5bd329bbdec0b99411434fa65268aa5f2f141d1d66a in / 
# Wed, 24 Apr 2024 03:19:50 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:20:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:789997181d7b1af2be77f38fd01378403217cac798b22c2b91152db6857ce361`  
		Last Modified: Wed, 24 Apr 2024 03:31:09 GMT  
		Size: 51.4 MB (51411296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6f63b784a0b3d9390b3db46784128848192a181cd18938a2148952a34f4928`  
		Last Modified: Wed, 24 Apr 2024 03:31:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:64dee8a1aaf454de73c4b67d99c850f2ed4fff38d0df7eb996498ee69f9eb1a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56253500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bdcd168326f7991d84693ce3eae9b73ba7c6cc0bb9f56429ccaa036e98d3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:25 GMT
ADD file:96a5c70b6b470689ae9f76bf58dbbdca302ccda081b6d6fb25d3249c5a22038c in / 
# Wed, 24 Apr 2024 03:23:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce4f206e19e1d340400f7cf79402f651c42ad37cfaf199791fb616c2c0c64fbb`  
		Last Modified: Wed, 24 Apr 2024 03:29:58 GMT  
		Size: 56.3 MB (56253275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc632e4899d3df8820b37b4214114635bf6e115d519b55d751eea25b9d77dad8`  
		Last Modified: Wed, 24 Apr 2024 03:30:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:4bc34be4ba1e8f93f35fa6ef1e8db5355055eaa407ddf191188a65534b3d72fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01ea6077e251d18bef840b9c0785e126c4911123a2a2a62f8638e93402956bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:09 GMT
ADD file:b0ed4b1191abf951ca60b74db08f035e1da25f6bcc32e8a7f9397ce5484c52d2 in / 
# Wed, 24 Apr 2024 03:46:11 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:46:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a1899f214a24ff2437842a08743ccd4bad2c8e5cff4d87f6220c3f36c1c34149`  
		Last Modified: Wed, 24 Apr 2024 03:51:16 GMT  
		Size: 51.8 MB (51766844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6d75b097e9b6a29e422545c2031d98527ab8696fcdbc3c3da7f34f18e93b52`  
		Last Modified: Wed, 24 Apr 2024 03:51:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
