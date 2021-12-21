## `debian:experimental`

```console
$ docker pull debian@sha256:7a67ed28007d042cb1760d80d5b604cdd60f3295cace557d5617ca1c6d47f98f
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:ae5a92c4a5e74db308253f8a3d61b011e80a52f0935b7c6c38d962ec234aacaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55798195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef37997e03fbd52ec8a362c8fb10926d1f76b1f83b120a1f26a11f81e5ec787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:25:12 GMT
ADD file:48125de314404b5ced792c318b5f07c798b024ff765bfb646af1bbf4772924fc in / 
# Tue, 21 Dec 2021 01:25:13 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:25:25 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bd3794a0f2768355393f3911f660530b0280b17bed920ed2afb90c7aa975de1d`  
		Last Modified: Tue, 21 Dec 2021 01:32:33 GMT  
		Size: 55.8 MB (55797970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb6443f37b6eb317c0e1f61f8e5bb5fdc4811925b07e4b5273a650d2d64c79b`  
		Last Modified: Tue, 21 Dec 2021 01:32:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:0abe7a043b6f60514f21e76e738d6ceee18d8ee1688564c87b3d62d308762fb5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53269550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc81f90e21cde91ec724e0d078c1bb6edd75fbcb9ccdf57509c12df94aba365`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:57:29 GMT
ADD file:24600f06b432a9e04673d6bd74b3d5f9fb8f87f9d524ccaa69e514f07066ec23 in / 
# Tue, 21 Dec 2021 01:57:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:58:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:24947e316786bfd44a030e940d0ec2c4d3fab0aeab2fa2d321d1a81503c5fb13`  
		Last Modified: Tue, 21 Dec 2021 02:15:53 GMT  
		Size: 53.3 MB (53269326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0f99391548b08dd7abd566acb5087da1216b2ce43639ac7cca890876c9130d`  
		Last Modified: Tue, 21 Dec 2021 02:16:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:b53020932831c893d42d687b7de9202601ceaa79edc4ebf376952ec17fa236f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50895009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d8244a9735c9041184e9a298732c39d965ec88b8b5c4fa0b007f23706ca5b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:07:12 GMT
ADD file:0acb092aa8d8774cde746814fec54817786562b4484e764be80e077399d5a28d in / 
# Tue, 21 Dec 2021 02:07:13 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:07:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec0c270902b03e6df934deed1e0d86cc05add8587de0317cfa2902c563e7bc3f`  
		Last Modified: Tue, 21 Dec 2021 02:24:45 GMT  
		Size: 50.9 MB (50894784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e626fd6d5963089b8495a025ba1e191f09d75876219fad57ccc76aec36561fc4`  
		Last Modified: Tue, 21 Dec 2021 02:25:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:70695dd61c309a9352530aa11778225f1ac9ba8a3d38230fed2271e13eea9f96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54781096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19d944ae667df30aed2d652d5019fb0b77ff70d9e6d9c17fad3f0bd0b3d55bf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:45:13 GMT
ADD file:7bbfdc666ed306d3c9e28a2b869378806f86c1640ea684e9f14a54de89208f1f in / 
# Tue, 21 Dec 2021 01:45:14 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:45:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:067276bef0f1e1a0d26e7028971339aee89b0a9a61bc5b45aa7efbf4b08ab8ff`  
		Last Modified: Tue, 21 Dec 2021 01:54:08 GMT  
		Size: 54.8 MB (54780875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05072134342ecf6f3089ef264f4f833be7661975a24dbfcc25e105e8f6415c79`  
		Last Modified: Tue, 21 Dec 2021 01:54:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:80da6c305335ce03d872e0f13582d431ca5242e7428833eb1e5bda994ee2f51d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56851919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fdda4af7c02361723a8b762a99b3da05b73422bcc80c4d12b31aa2005e8dec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:13 GMT
ADD file:f52ad383331ad64becf207e93847af259a33309a89447a23e6c38c82aa9685f1 in / 
# Tue, 21 Dec 2021 01:44:14 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:24e98c1e6129732b99ca0b8ac8d6ecb76c94380d46f6bf54df2db7eb94bbb3be`  
		Last Modified: Tue, 21 Dec 2021 01:55:03 GMT  
		Size: 56.9 MB (56851699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c807ab96816302ea8431aafda6ebdd59787f1b62317676af8b0fd9c55d1a22c2`  
		Last Modified: Tue, 21 Dec 2021 01:55:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:1ac58b41fa8294371cdcf4e5aa768a92a960e6874bf939dc372210618cbdb11d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54504139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b826724145580c68de425bed50c501597e428912757f24790d9969403f7e40e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:02 GMT
ADD file:9154fee4b9065a7eb6f324b30e3c67f42b2a8834d157b96954a7ead7e3c21f1a in / 
# Tue, 21 Dec 2021 02:14:03 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:14:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8d71f621a92f23fcb5fa6acbb32cb5b2dd2c18b987aff70687648a1f76cac7f3`  
		Last Modified: Tue, 21 Dec 2021 02:25:57 GMT  
		Size: 54.5 MB (54503914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf14377e08f21ebd00251b602373c2ee17232c8b8b5d23dc35b64f8f266c2b0`  
		Last Modified: Tue, 21 Dec 2021 02:26:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:8e257a5d95c8f6fbbdbdc0ab8e1f58014cd4a1d9e9f9c87a5a71bb6c0a670a4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60199995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59624628834e21d9ffbd9a10d9a2c4146903285aac3d12fc677ee2ab168ff32b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:24:38 GMT
ADD file:9adfde6812f8a438d9e14754c951413a4fa0d088e7d3e7bf8fb16086235fb01a in / 
# Tue, 21 Dec 2021 02:24:44 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:25:14 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c825b774445ea3b85106841267caca3e17aac797ab631a81926ed2602be1035b`  
		Last Modified: Tue, 21 Dec 2021 02:34:08 GMT  
		Size: 60.2 MB (60199771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bbafc431670f4ec56471c0e5b66a89873033ead158de01aeb6fb0a7dd0f821`  
		Last Modified: Tue, 21 Dec 2021 02:34:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:b42df6358c874981b38cc36ed90b7d51c179009c06152872ed4be0e5f490b751
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51541667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60c409790298cd1f9d4800669ae114251123ae49683e95b5e772885fa3746f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:17:42 GMT
ADD file:781a0d30962b9bed950ef5ae89d839aa2e83d3aa8f7a9ec0cb26281d19643ea6 in / 
# Tue, 21 Dec 2021 02:17:45 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:20:59 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b4913aa804dd13a6069cbd8d425961a5de7bdbecaf3ada9150bc9cbc6f45f594`  
		Last Modified: Tue, 21 Dec 2021 02:34:04 GMT  
		Size: 51.5 MB (51541437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0bf735b80c5f72868e9ffb29dc0922136d63ccc058f6dcdc27b617cdb2de6d`  
		Last Modified: Tue, 21 Dec 2021 02:36:41 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:8e911f89e1853b29beaa5b5f25297e2ff2657aa9d2f678d2ecd4aaec7d4f0af5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54090402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75251548d1d0cd053114d0529041e5c6e4ac152d31bbd5a2c87d786c606abf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:58 GMT
ADD file:e76938b8ad072e015b92e5de79be47dd882886dbc87218441c2ea6c4023aa989 in / 
# Tue, 21 Dec 2021 01:45:00 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:45:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1335c6a8992ed83758a594f9813a6eab266e49fa2cfb3cd09413a599ae0941a3`  
		Last Modified: Tue, 21 Dec 2021 01:51:03 GMT  
		Size: 54.1 MB (54090179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c7e653d714f040d14cdefed97fc39acb48b66a0264996fa10675a969e5594`  
		Last Modified: Tue, 21 Dec 2021 01:51:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
