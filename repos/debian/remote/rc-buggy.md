## `debian:rc-buggy`

```console
$ docker pull debian@sha256:2ca06d122bad2b44d6244924672842a2c669e46f7e3ead959675f3bbaa1f5b8a
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:600ee2adbe160d3d32c469c11d17a89aaf3bb91b55240fb4fbc052c2cb5038af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de802bc341ccb08a77290672fb5472c3e1577422282f842ba921fc9930007096`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:31:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a2a7cd72e879f18a74976b842b19b3a1f619ddfe9ee66f13607eb2f16c3f5a`  
		Last Modified: Wed, 24 Apr 2024 03:37:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:05cb9214a9430093699f6f05540e1d1464e1b633e83297d404bf1819224989ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49745374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfc84014ec578c710d322a4ac4115122b05bf830d87c9d78d2bfdac9e3b2ee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:14 GMT
ADD file:48ad2cec46f0edaca758532e477d58141198d71874a7a659465c7778bc242f0e in / 
# Tue, 14 May 2024 00:49:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:96c71f057932ff03c2e4c9ce93dc6ca864ede3a6ed0a0a4316465b6b244a70e6`  
		Last Modified: Tue, 14 May 2024 00:53:10 GMT  
		Size: 49.7 MB (49745150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba55a0da71eb417227f50c1ece57850502bd0f1dc438e8104607bb2e9eefc9a`  
		Last Modified: Tue, 14 May 2024 00:55:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:9f1dad014b91aa3afe29d5124084834dc4180b9e8c8ce63464c625598c77e548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5189af53e2c9639784e70229b73f6c6fe939c886e24388d7db2c283978ddfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:08:27 GMT
ADD file:2777c4d68da3c72783e92f5c8fb23b016abe830ec194eef61314095668218e31 in / 
# Wed, 24 Apr 2024 04:08:27 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:09:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:074f397c7ca8667adffc9dadeb0bf349fdf0c55e27384ed869e827a03f001b2d`  
		Last Modified: Wed, 24 Apr 2024 04:13:47 GMT  
		Size: 47.2 MB (47214198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6109dfe8511d05c1ed39b064226f6776bb79aa79b36fbe4128c5070ead9303d`  
		Last Modified: Wed, 24 Apr 2024 04:16:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6bf95f4f845fd201b703078a01cb8eb49e7936e3c09a93caa304fbbb4ba397e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52930511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efab337d9cee76ec073bfe7987493d7fd675bf8a0456f164c40355679142c1c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a35d887ef4d1f89c72f4dec94a533acd405a16292ba56da6220f6171b62e4d`  
		Last Modified: Tue, 14 May 2024 00:47:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:e5cf61c7bf67937e1db22f60907a6b0ab29fad060739d749d3a7d1c29b2654e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53540142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183aa4fd365e077a9b9eae1633201292ed6a67a350c08bc7ba80c41df401447c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:47 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
# Tue, 14 May 2024 00:48:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce36813b366b567235109a8db4a2558d3173f56b91c55c4cd8a3579b0393aec`  
		Last Modified: Tue, 14 May 2024 00:58:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:1a626f7709b28630ca5e2d99ac468a8d75c65d21ee08502ff34474441ae2fd0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51498675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888bd951d84102b37d689f6e6d36e5cb570f1730bc7e5cad0b56236f5765d641`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:17:23 GMT
ADD file:6ee5f04f14b1e874e152ce4477f27a16f4f4f6e4e49473d9e0d4f54bc8c7736d in / 
# Wed, 24 Apr 2024 03:17:28 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:04e21b74f69d4354ef0e677ec5dab4b460bf993f23d559662b8fd1e622263e43`  
		Last Modified: Wed, 24 Apr 2024 03:28:44 GMT  
		Size: 51.5 MB (51498447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494a83318c51e53b2eacb087c46d2d72fad9700ca4fa04d6cd43f0475f5607a4`  
		Last Modified: Wed, 24 Apr 2024 03:34:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:8f4613a59e5ac8396b0b35062c80a5860f80e9553692019ac27308a9c784e8cb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56489458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24c53abab93e1bae0fdebf712b0b454086d0d19650f9bd40f402ebaeab439c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:30 GMT
ADD file:7b560eb5bd2a2213add3248349e22fae85a27ecd1155298a4bddb816d7a54856 in / 
# Wed, 24 Apr 2024 03:22:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:24:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:765cbb6e5130c0f3c7d92d3db7754f09101ef280d3dc88044ce2e4f3d010efb2`  
		Last Modified: Wed, 24 Apr 2024 03:28:43 GMT  
		Size: 56.5 MB (56489230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd5925f02d75fd77f75081f461b4a45a40f6b3ccb40e2dcf39597c2473b07e8`  
		Last Modified: Wed, 24 Apr 2024 03:31:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:70eb42d131033dc91993315bfdeb2d8661e11fb6ed4a10dda530aacc9f6aa043
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50665618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35edb47b4f3694bc21028cf3015240e5c3343098a9f22dee53dcebe78413bc25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:09:40 GMT
ADD file:d90cd6aeee4d6792791ea2b4b9b5059a36f027dc9b9bb977ca1e8446d6911cd3 in / 
# Wed, 24 Apr 2024 03:09:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:11:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:95fc214d1cab5d6d820b79b86707ae2364689381f1652820f201941397cd8e5e`  
		Last Modified: Wed, 24 Apr 2024 03:12:28 GMT  
		Size: 50.7 MB (50665389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6c2dc53fb042895f27c223670a1afe9525f17f7af30ac2b4ee2b6a34e86f0`  
		Last Modified: Wed, 24 Apr 2024 03:14:36 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:03687ed3a2b65378e027c3631e432f4e3d3d25a09c860dfea23cf6fb58773f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52293536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a811db6823e58fd879065d16b3ab390c0139dc50d6bb5e4740e6429e6efd64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:46:20 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884d204514e5c137f8ef640e3fbdf94cdedfb0370845c288785440bf2d4aa1a3`  
		Last Modified: Tue, 14 May 2024 00:50:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
