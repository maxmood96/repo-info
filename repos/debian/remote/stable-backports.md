## `debian:stable-backports`

```console
$ docker pull debian@sha256:a9aeea7b3ab95aabbe9e01a4d2ca6cc74ae5f440ddb5ad87982c7594520cd29c
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:abc202038523c8cca0fea3e729cbc84d00b8bb9b4749bba18bdc05d395cb95e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54927922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674df3bd92e8313fb4527f8348ceccf81c1edd7e06e6995f4fa718a42c533598`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:24:46 GMT
ADD file:31a8a83beef2ee4f697ad94d45dbaba4232bec655a4bd8b1971b18aa84ae9239 in / 
# Tue, 28 Sep 2021 01:24:47 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:24:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:37129e212f741f9500b01b63da85f25e1c35df814e9e2dfb70b0892e66dad19f`  
		Last Modified: Tue, 28 Sep 2021 01:31:51 GMT  
		Size: 54.9 MB (54927701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279453c7f5698988b22d325f1e788e44969dd394a86f69e857f1f8b37fa9d66d`  
		Last Modified: Tue, 28 Sep 2021 01:32:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d8957be83e1cadaeb79389803cc02fb424adbf528f02744a616494f11537da6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52462826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2edc571cfed26d548c68892cfd975d2faf971d42096c38a83eb3a230ff2e484`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:55:06 GMT
ADD file:0e6ce2354abea399c141cb18810c73f794b26ee2b8977b475dea03738835b94f in / 
# Tue, 28 Sep 2021 01:55:07 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:55:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:842365e3248b639036bd02130125b2b175c493263cd89d3bf0e381d92f9ce63c`  
		Last Modified: Tue, 28 Sep 2021 02:12:32 GMT  
		Size: 52.5 MB (52462603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa2f2a4390b2e4982c6ba6e46d8ae4d003b0a667e63182587508c569937e7ca`  
		Last Modified: Tue, 28 Sep 2021 02:12:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0343c944cbb20c21065f7e14e4175623a839f26f6efd21eca21e7bcf67d11e1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50127483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6a820cd320091b4651e14036925b4e85d4219ee620305b0a44ec0052784838`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:03:48 GMT
ADD file:7464f26d5013556d325788672457271f1482968e327d19f7343cda0be98447c5 in / 
# Fri, 03 Sep 2021 01:03:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:04:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d7c64607233a772e86e7c98f2898a771ca7f1cdef55d721a73548ac0b16ff5ab`  
		Last Modified: Fri, 03 Sep 2021 01:20:44 GMT  
		Size: 50.1 MB (50127258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf076b2157aabeab3ed9cf411b2f86c1bf13f2deedb16cfbd70b0f3a40d1d6`  
		Last Modified: Fri, 03 Sep 2021 01:20:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3e4f1bb6e4a2f1cbdd7be178e6d92d07beb51c3846a875902f4efa845f4b63ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53613838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fa417fca7d1a8ed476dc31bbfd99e89ef01059a4afa3991f93845c9153a4b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:42:42 GMT
ADD file:eb34e054c7cc16b0c62d11e0cb3c2480d6f2c9929e49abacb5a5e9b78653806b in / 
# Tue, 28 Sep 2021 01:42:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:42:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:83cafb21119468aa543f03d39375d165a9e5ea883769c1c2a25fbb5e52e507f2`  
		Last Modified: Tue, 28 Sep 2021 01:51:44 GMT  
		Size: 53.6 MB (53613618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b996966c13ec347058b17acd8527d9ef62701ce94b45179103e28a66328aafb`  
		Last Modified: Tue, 28 Sep 2021 01:51:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:3cbf076dc7cb58fd8f4f4de129f42987a9b8b6e6faf68d343d3c50ca81061c4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55932399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93a24ac374665697a5358f1a607c6374c65c9715e2c4b66d254c89098e6a2d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:42:47 GMT
ADD file:53294f47559d8ef39ef7576d152d9199fc6e93d0871639ad9c7da6bd704fd210 in / 
# Tue, 28 Sep 2021 01:42:47 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:42:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbb4e8a30f04e26c75566f2f4089792bd5775b981f63587d20485d1bab6b29be`  
		Last Modified: Tue, 28 Sep 2021 01:52:46 GMT  
		Size: 55.9 MB (55932176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f67a2ddff1f221c7efcc7c62ae1ce2f501f0328dd3faa64994f5ef0c5d526d`  
		Last Modified: Tue, 28 Sep 2021 01:52:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:92b1ab03a3b185c265d9cab385edb64b63fba9825c658530024e3d017436d961
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53177406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23714c3e898bf9dc1e75f1c381f7bf7e05ff6cdc41adbf4fc4374ef8621a7e27`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:12:48 GMT
ADD file:027eda15910b8858f29e73fae2027996c266ea9b1fbb74e7e3702421edae5396 in / 
# Fri, 03 Sep 2021 01:12:49 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:12:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:def7717bcc5e494128c1aba2c8eaf9f5826d8b1a92ac1fde020434f2edc3ac34`  
		Last Modified: Fri, 03 Sep 2021 01:23:05 GMT  
		Size: 53.2 MB (53177182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaadc85450c3fa2b5403303675078a868d6cd840cde8823a9f472e56ff10754`  
		Last Modified: Fri, 03 Sep 2021 01:23:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c31ded44cb3bbffcafbcde92fa425e33363648bef803e19ae025d6215d3d4016
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58819650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0b25087a8ab592dbc57cac7a0fb2ede7387e440f306bfb9da070ac099bc8c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:26:59 GMT
ADD file:65fd9862530d73959aa4b1a794c58ad4fd4fef5e64c3a5a48386cbc75b5a1b77 in / 
# Fri, 03 Sep 2021 01:27:08 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:27:24 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a8d6f167deff8b537d96bc08a0664b47da9250cf4f4f5f2726008df2ce0db1be`  
		Last Modified: Fri, 03 Sep 2021 01:44:46 GMT  
		Size: 58.8 MB (58819425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d20444ab3a29a7f981bcdaf28c31848b34b558259b0423e3f31680a56b50615`  
		Last Modified: Fri, 03 Sep 2021 01:44:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:eda2212279d17b0e82a86f2488ea18b7186e3d1e575b036492a81a6d7acec75e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53202521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611383964126f93bd6f7d8575197e12156dd1cb71c3a52cd9f3cac53da60f5a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:44:35 GMT
ADD file:d66612e9ca6b439a1f226f6087e645fe6832cf8a082c07a700f77172f781978c in / 
# Tue, 28 Sep 2021 01:44:38 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:44:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d054f22f56a959516ae135da376b9575f1782619bdb475eca918b23ed206325e`  
		Last Modified: Tue, 28 Sep 2021 01:50:44 GMT  
		Size: 53.2 MB (53202300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ab1ad3585e49fa1f392a92932ec116aaf6442f37b87a60864276792211b739`  
		Last Modified: Tue, 28 Sep 2021 01:50:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
