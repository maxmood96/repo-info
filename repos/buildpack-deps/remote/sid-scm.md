## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:0d5f5f421fd2022136098953ca6117d73b9c2140d714cb1e266c36454eddbdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5ea59f6da4d8726fcbbbcb5a11dc677beb9e5b72502efb7a6540f92cef668c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142424109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c235159aaa260ad96e296b0c1d3f62be59fd7f75c625492ab506a1646922099a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b3978af1e166e57bdb05260799a7b1770bd65f02601552db72ffbe944a422d`  
		Last Modified: Tue, 21 Nov 2023 10:04:34 GMT  
		Size: 24.8 MB (24793981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae081620ae95b09fd1b9617c1f676d0d998479bc08e6bebee281d0bea30f3f7`  
		Last Modified: Tue, 21 Nov 2023 10:04:51 GMT  
		Size: 65.5 MB (65507860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a14fff4df4cffc72ece82f02fb56f4d17fa776812b43c4c2cf6a19a9b4c87db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136117428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bafb9025c11df5f43acb3bedb814be855b4fd0db9041333997866bd26b03b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:01:33 GMT
ADD file:b1618939ac80f9d3256d12ed22ac3e37f61dc396e5370e7a4013561a073af181 in / 
# Tue, 21 Nov 2023 05:01:33 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:19:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:228b88d8d39e27fa3bddca63f14715a5dec3e5c3de7b5b5a892c00385ea38d2b`  
		Last Modified: Tue, 21 Nov 2023 05:05:36 GMT  
		Size: 47.2 MB (47196697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df76a43e2f790a0c0d3fd4795cae7a8d79b43803710d103b38936a70bbe216`  
		Last Modified: Tue, 21 Nov 2023 06:26:42 GMT  
		Size: 25.9 MB (25892928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8da3dad66ffd081a2a6a2a79c62c577b4c8f5b7751d2718f24e60791eae1e`  
		Last Modified: Tue, 21 Nov 2023 06:27:02 GMT  
		Size: 63.0 MB (63027803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43bd039a111ff18dd0a63cd13a31d9dd641b36941ebd1cb91eeac6d9cb35d1a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130513940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ee8381f8cf9588f0e2a248e8ff70be2963e34f40b9d56f53796168d3f1103d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e8fae7790bc6b852297041272f6286f4b7c607ca5435b1a4ec5492425ec55a`  
		Last Modified: Tue, 21 Nov 2023 14:17:07 GMT  
		Size: 25.1 MB (25054248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a7a5eecc1f0a2e75f1dc4cc1953feec4555e8fb395f67d882284d7c17af33c`  
		Last Modified: Tue, 21 Nov 2023 14:17:25 GMT  
		Size: 60.6 MB (60615689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:af589c91ef37d6c32116a1b241e4aad363808ff422474ba16f569efd841b146f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142225783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222f9f3797f956ce854e32cffc6df6746b36e71ec083ec3b8e35759cf731ff9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a3b26cecdfe35cedc579177de975c502073e0ec3b623c7408d7145436fd16`  
		Last Modified: Tue, 21 Nov 2023 08:08:57 GMT  
		Size: 65.6 MB (65611513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bf9e365b381337f4d6b2f5562e4a5c66f62d51e107a697e2abc16c6cf3807722
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142969483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890f7be8650dfbec3174b0c555ee6f84c9085c83f218e591ccd4bcd9822ca9fd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:0aa90abbd80c68d937903de7ac8fdcce0f516fdd70f080b677af1e2322c000b9 in / 
# Wed, 01 Nov 2023 00:40:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 13:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:96660bac4658b1bffb27e96ac8ecc86753a1844f042ede32c4f1faef702dc202`  
		Last Modified: Wed, 01 Nov 2023 00:46:42 GMT  
		Size: 50.5 MB (50516486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7af088639fa61079db294f16f91145938a488365f2aec8cef7a85da80c4b13b`  
		Last Modified: Wed, 01 Nov 2023 13:59:54 GMT  
		Size: 25.2 MB (25185750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34a1138df818473932216f10a656452bbeead89efc81870811003208908e138`  
		Last Modified: Wed, 01 Nov 2023 14:00:17 GMT  
		Size: 67.3 MB (67267247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:21f9abec3d9a8296975dfbf0f1e6de9f0806aaad961672253abf0007a8da6da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139732835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ffd837da0f2bbc0869984b97e66c0a66cf007849896b160812d7109cee071`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:12:53 GMT
ADD file:9030cb9b65f8be61ec19318a90c95afaaac8943c61f5ee6b30b90d758a8b0964 in / 
# Tue, 21 Nov 2023 04:12:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:41:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f090d405a1df972a813ac2207398b0e5b36cca91650c17a34fb17616a3e7fe19`  
		Last Modified: Tue, 21 Nov 2023 04:23:59 GMT  
		Size: 49.3 MB (49341847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e9e1c518f951e1dc2742e209f1d1b2ba924d2068f93c7d8e386603f98f04d2`  
		Last Modified: Tue, 21 Nov 2023 13:04:52 GMT  
		Size: 26.1 MB (26077539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ae92ee0eea266534adac9439fab060820cf91e6c7180edcf62427764b9201d`  
		Last Modified: Tue, 21 Nov 2023 13:05:44 GMT  
		Size: 64.3 MB (64313449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:24a7862e93585787852dbaecc311fe50c85ca997c602ae777a5a40f37264db6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f839951b7a1ec1855581f34657a10b0e452a76662c147f9893fb5b4b1355743a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fb001517f3aa634674774ca44ff1ee072157218fcd0522c1630479101d895`  
		Last Modified: Tue, 21 Nov 2023 07:09:33 GMT  
		Size: 70.9 MB (70920797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:33c5e15d08ce712b59fb3c301d86849d093fabbed9d042e2dfd606d54cb3405a
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139693887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b886411896315e38d59726c286243652452815642a349f1633769e908c0c92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:02 GMT
ADD file:6edb177cc4c3fc7c02043410bba7fabbbaa23493a2e0444ac13e281f6fd7d209 in / 
# Tue, 21 Nov 2023 04:09:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:33:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:35:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9197643899c29fb1e411101ee2f4e677b44704d5c2c8ce98f7567cb7f7a6cf58`  
		Last Modified: Tue, 21 Nov 2023 04:12:00 GMT  
		Size: 48.2 MB (48206696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0617cf6ad3eec888f08f7b773880b515adb1cae0586b8aa6f4b5f40076079dd`  
		Last Modified: Tue, 21 Nov 2023 04:43:06 GMT  
		Size: 26.8 MB (26784568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e112439f28d2102590bea4e42209332ea3595b8c9789016a1e8b479e123bee`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 64.7 MB (64702623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1769e0bcb2fe395e6ae63c7c91bdeee37003e88269a8db80d927a4fc64840f8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143751167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47000f61dc60af3bdb834e3d3470c752ac2e6269191cb531d5f7264a413791e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:06:09 GMT
ADD file:38bf5e0509c54c17377ce5928ac13833ab7953cb7ff56a92265b9835fad4a7ef in / 
# Tue, 21 Nov 2023 05:06:14 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89d47f76a96d7ec8b86acac59109c329b28ddeee28c3c0b2ae9c6f275a50a136`  
		Last Modified: Tue, 21 Nov 2023 05:11:22 GMT  
		Size: 49.2 MB (49228111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd42e8e3bd2b6546f326a1d59a7ec0be9e7ece5e7885fd1749571be27caa1ba2`  
		Last Modified: Tue, 21 Nov 2023 06:18:03 GMT  
		Size: 28.0 MB (28032511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21db908a00e81480eebf3fad2c4e13874394ba9f9978d3ea7677d3be28b4fb`  
		Last Modified: Tue, 21 Nov 2023 06:18:18 GMT  
		Size: 66.5 MB (66490545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
