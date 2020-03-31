## `debian:experimental`

```console
$ docker pull debian@sha256:1e6368c7abdf92940f4c3abe8f0d1d97c1efe19e3259fb1187cbde32fcbc4abb
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:c7373e7ea5d8ba737558796032703d81347a1e17b32e46120b56e7e880141efd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51949863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f247d2e133ec7647447b486a1b828f410e5611235b0cf62451140ad9b0dd90e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:55 GMT
ADD file:eb55e131be32f7ea28d64283a0a3a09c157c58a7b7aadee1acbbe29762740b59 in / 
# Tue, 31 Mar 2020 01:24:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:25:14 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5849424bb1bf5e300d7218e461c40939164f8a60a7cfa279ea53a0d0fae8f267`  
		Last Modified: Tue, 31 Mar 2020 01:30:14 GMT  
		Size: 51.9 MB (51949642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eba7b1f65ae7e782e816095c831d5ef6da4964739881a2a4a22c1f0420180d`  
		Last Modified: Tue, 31 Mar 2020 01:30:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:e2c39563958034f44b400acc2d65e74f037ddb0ceb9da0dc75fd6bfb4b1f29c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49891534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de5794a5f262cc77ee968f6243fcb0b187bea35c7ab37b01ad1a96025bd6ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:30:22 GMT
ADD file:3f4ed2046ae106e159bd6244daec6b1938f1e2f4e160a9668d8c3f73e368c787 in / 
# Tue, 31 Mar 2020 01:30:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:30:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2a2aa4a2e7b160113fb77d1857da4bc3115b0749bd94c13e9180641e734e2eb8`  
		Last Modified: Tue, 31 Mar 2020 01:37:58 GMT  
		Size: 49.9 MB (49891310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab676c267d8fd42c5217362beef9c9baa2b1620ba9cb28c0e709e3c1f0160bd`  
		Last Modified: Tue, 31 Mar 2020 01:38:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:1d71510d1f93bba4358fda17451dfdaf42c8e6563dc0e99dc66d8cd7016a2e2f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8423682e293105311c9149366684596a5ac7a01377a7424f8c83587cb620fcfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:54:01 GMT
ADD file:71ddde9275f6a2f23aca3ab9f782d22611c0dfdb0232646057873e1deccbd50f in / 
# Tue, 31 Mar 2020 01:54:02 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:29 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1472f2c1796028f8daeefd99d774120f9bb89f41ccba518334782926381cc36f`  
		Last Modified: Tue, 31 Mar 2020 02:01:16 GMT  
		Size: 47.6 MB (47626183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb612c292cc94379c05511b0acc7eb08d37c1faaca34f31e3e6dd4fa7c04080a`  
		Last Modified: Tue, 31 Mar 2020 02:01:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:571604dbc1f1660ee7511c86960ba3b67ce1f689aa6292bbf4ec5edfbdb7afea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903e22e529de328bf05bf6c1f46badda52c6c14d7f10cf0cac752bd04fddcab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:52:47 GMT
ADD file:45b0bf38929542776b712acf57d6bb864b988e78c51e9aa3aa379bf350aaf1e8 in / 
# Wed, 26 Feb 2020 00:52:50 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:53:45 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:28437fdb5bde91523026f69fbbd2192d251796689c95fa802cc0d7aa44b311a1`  
		Last Modified: Wed, 26 Feb 2020 01:00:14 GMT  
		Size: 50.8 MB (50825116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7100571b29d09295c0cd7a2493fe02a56c727b212aaf7a6fec9cd962b7dae7`  
		Last Modified: Wed, 26 Feb 2020 01:00:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:3aefe45ee78c2b11f2b2114c516d05294eb2a21b11dab8687feecdeb75623e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53085911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12901ed6b0618874021b04e1a5cb011ac3b1be515c3f698062da2db087838883`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:43:39 GMT
ADD file:88672776988a857aec646e66129c02ca354e07356c08ea8685ba7cdd8488dec3 in / 
# Tue, 31 Mar 2020 00:43:39 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 00:43:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:184cca0a947c292018eeb70034b2a59867daea7475d6a49f87251467b37969c3`  
		Last Modified: Tue, 31 Mar 2020 00:49:39 GMT  
		Size: 53.1 MB (53085690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4412beb36d1152b55414e51b9bfb58de1f7e331e05b5393400cbc273962bf017`  
		Last Modified: Tue, 31 Mar 2020 00:49:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:39a6ff67edc3c9bdda1c75075071d727b633d76a34956fdb4738891e6d93992b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55835144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2346fbbac0ddb5f17d9f3f66a8b8c379b3eeacf6c93849ea03aa7223a4e58bbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:38:23 GMT
ADD file:74a80c387973a5774f4fe95d7dc55f1b6c519d240c59edf690627d9a0e7f6171 in / 
# Tue, 31 Mar 2020 01:38:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:39:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7ae94100b5293d1ee61294c40974056b2c12f787904b73a1f9f3bd236ad387a2`  
		Last Modified: Tue, 31 Mar 2020 01:57:42 GMT  
		Size: 55.8 MB (55834920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa76c98211a7946c222da6c0dbaa628101d5a4472701e28977ad3cbe8b4b3f0a`  
		Last Modified: Tue, 31 Mar 2020 01:58:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:0c227041cff0e2cb9641ba9cac5ac66be2cb33f8c17ba8f431d4841b22035511
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50546227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d222bfcf1a46b3999948f88a0a8b3a74352f3a958a524fadbb52ee7cb7776725`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:11:12 GMT
ADD file:128e9d6b5ebdf37db9e2eda52492809f86e74876d083fbe1a337056a635dfcb9 in / 
# Tue, 31 Mar 2020 01:11:14 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:11:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:44f8b130903430a702ebd476ecb940fb5e3caafcbd484d8f6e6e05cdfafe1fbb`  
		Last Modified: Tue, 31 Mar 2020 01:15:13 GMT  
		Size: 50.5 MB (50546008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78721e5fe8dce7df5d3a272ca2040cb2471d475976554cc28f7cea5b2024a2`  
		Last Modified: Tue, 31 Mar 2020 01:15:36 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
