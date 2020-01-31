<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.4`](#nats214)
-	[`nats:2.1.4-alpine`](#nats214-alpine)
-	[`nats:2.1.4-alpine3.11`](#nats214-alpine311)
-	[`nats:2.1.4-linux`](#nats214-linux)
-	[`nats:2.1.4-nanoserver`](#nats214-nanoserver)
-	[`nats:2.1.4-nanoserver-1809`](#nats214-nanoserver-1809)
-	[`nats:2.1.4-scratch`](#nats214-scratch)
-	[`nats:2.1.4-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.1.4-windowsservercore-1809`](#nats214-windowsservercore-1809)
-	[`nats:2.1.4-windowsservercore-ltsc2016`](#nats214-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.11`](#nats21-alpine311)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.11`](#nats2-alpine311)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.11`](#natsalpine311)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:d0de93952d9f9719d01aea93344175a923bbafb81b8ae76bb4f607394ba1a529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.973; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:d0de93952d9f9719d01aea93344175a923bbafb81b8ae76bb4f607394ba1a529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.973; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4`

```console
$ docker pull nats@sha256:d9afbe956cf65a229bc168536030da44c4ab639361d2540b3b5d68ec252f17a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	windows version 10.0.17763.973; amd64

### `nats:2.1.4` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-linux`

```console
$ docker pull nats@sha256:59d691ed3578e01695053510d3128c00f9d1676b5a4965bdb048a78aed1e4bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-nanoserver`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1.4-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-nanoserver-1809`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1.4-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-scratch`

```console
$ docker pull nats@sha256:59d691ed3578e01695053510d3128c00f9d1676b5a4965bdb048a78aed1e4bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore`

```console
$ docker pull nats@sha256:f635e84db146077c8ef8f2aed7a35a400e56b88d444d8043d9f021cd43d014d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:2.1.4-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:f260d466cf5497a8d982b10082a9be701726540030aa317161623e5ad23b8cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1.4-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:6d3bf1780214fdc169539a34a011b65e0cf341710c60d683a5e29f461a5b4ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `nats:2.1.4-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:f635e84db146077c8ef8f2aed7a35a400e56b88d444d8043d9f021cd43d014d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:f260d466cf5497a8d982b10082a9be701726540030aa317161623e5ad23b8cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:6d3bf1780214fdc169539a34a011b65e0cf341710c60d683a5e29f461a5b4ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:f635e84db146077c8ef8f2aed7a35a400e56b88d444d8043d9f021cd43d014d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f260d466cf5497a8d982b10082a9be701726540030aa317161623e5ad23b8cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:6d3bf1780214fdc169539a34a011b65e0cf341710c60d683a5e29f461a5b4ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:d0de93952d9f9719d01aea93344175a923bbafb81b8ae76bb4f607394ba1a529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.973; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:751d689d4eb3ec61dfd636ce35878fe4416473980b683deb48d056dd68fc89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:a915a74a33c178bc56992ba92f1dac6e793a15695b2ba8686921ff126231c0d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105080703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc5090a4417ef6c4bf289a117e63976ae4ae1873bf9ed527cd3d6144649cbe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 17:50:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Thu, 30 Jan 2020 23:22:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:22:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:22:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:22:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:95d31e7189792498b758db35ae56b1ca97128d8063404cbe62a32205d08d1d4a`  
		Last Modified: Wed, 15 Jan 2020 17:54:30 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46af9449d934d719c0364b5c93cb954441f53860dcaea1a4116e592cc0b3d3b5`  
		Last Modified: Thu, 30 Jan 2020 23:26:25 GMT  
		Size: 4.0 MB (4021080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaf30278335c0a205ae398e0394451ddeffe52f49342d53b2aed5f5f16980cc`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a716bd8f7fccddf2ef8bae3878794e53786f3b6c22eabc19edd88d645382a8`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b737ad14091edd6e4a7ba6e079a6d2294a44b93179e67f961f6afc025ebbf5`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad080ffd77f31e642dcb648be07f8bf0ac770749b581badc4f9a429d2cfe4a`  
		Last Modified: Thu, 30 Jan 2020 23:26:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:f635e84db146077c8ef8f2aed7a35a400e56b88d444d8043d9f021cd43d014d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `nats:windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f260d466cf5497a8d982b10082a9be701726540030aa317161623e5ad23b8cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull nats@sha256:3cd1d4f67d1be8ddd5ce24eee17e14d4ee01ce9cdd54ee035ba49aee1ffb0106
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230544935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64e3e55e102dce9595319163c41fbc2a3817842d949f09ed00f6abf7e6b612`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:41:54 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:20:19 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:20:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:20:51 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:21:50 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:21:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:21:53 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:21:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:21:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23c268ec0520ea9af1e83b69008728041b2a5f234937b9a6272d2a739fd92e`  
		Last Modified: Wed, 15 Jan 2020 17:51:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64db2fd4fc94c96bf74d4ceda66e789cc94f8564a3e7883c4ed1342bbafcf73`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95109215dcc59b85e8609afe1f1a937ae8b0e371b6e3fc87a312dca652bba88`  
		Last Modified: Thu, 30 Jan 2020 23:25:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abe00c43ab7107f68a12e1168c1dcf4f270ae2838f9dbee912fffa64b29f8f`  
		Last Modified: Thu, 30 Jan 2020 23:25:45 GMT  
		Size: 4.6 MB (4572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebfa1af024a4a9c5c405f8e90e7516490239d94819cb2017d64f4e986ff97a`  
		Last Modified: Thu, 30 Jan 2020 23:25:41 GMT  
		Size: 8.6 MB (8551363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e85db3ba0a6f65fe27a002088f3e8e56d7e44e8505538fc3184b1004b67d0d`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b6720c8426d9b09c64fb77d91a4c52cdd6fdade7b5861b7e3b6a7a71a5b01`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d3d6953ad42f738ea691168e451f77533bff19e02ca60651cc5ea8b0909c98`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be73e621a1b74a2c24116891bd94204ca37d37e42e009c8b5618f9fa4ef59ac`  
		Last Modified: Thu, 30 Jan 2020 23:25:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:6d3bf1780214fdc169539a34a011b65e0cf341710c60d683a5e29f461a5b4ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull nats@sha256:b93a92c7137ce9e49e77908d56639a7979de1576fe2392dbad574eaf3b6af1b0
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5739398111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d621c7c840a5096b8f22cb481c70fdfceb17ae28ac91d1d0e2f0c03c51b85`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jan 2020 15:20:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jan 2020 17:47:08 GMT
ENV NATS_DOCKERIZED=1
# Thu, 30 Jan 2020 23:22:31 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:22:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 30 Jan 2020 23:23:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 30 Jan 2020 23:24:55 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 30 Jan 2020 23:24:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 30 Jan 2020 23:24:58 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:25:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 30 Jan 2020 23:25:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43da502775fb34b738d9f908cb549c2825c04f1451d1039ec99749be127e47ef`  
		Last Modified: Wed, 15 Jan 2020 17:12:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6771e606bb5340710c7ec7fa3294903a0a1f901e5c1e79211ee54fc1f074179a`  
		Last Modified: Wed, 15 Jan 2020 17:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726042a1cbbb18db11b01cd4afb9a1827a05f1762d628efdfd36f44607d587f`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e838ce5d75be430b4249e23414b64cfaa1fe44c2ac38610b5309614d2085deb`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe1a1b70129b898aa43665d07e08975be6969c32de34dd93c089d2d61ce532`  
		Last Modified: Thu, 30 Jan 2020 23:27:09 GMT  
		Size: 5.4 MB (5382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c046f50b9363080341b7a2690e4a9be42c7774ffcafa964d579a0f8f710cbd`  
		Last Modified: Thu, 30 Jan 2020 23:27:07 GMT  
		Size: 9.4 MB (9406281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f4452a72cff84b1af502f71920172156ce34de4e7bea4f0bdc0ea3fbb9396`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca833ddc6c1c6e6affb374a6583b04a19307e144be67482ab44ceeb7c93a717`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ec24ad2af324939951cadd30c9e492bc03eabc126e51ea070390dcd4ddb8d`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadd053a880ff838580bf99313b315b9d5fdb3ae9f14aa2e8057b2557d8390e`  
		Last Modified: Thu, 30 Jan 2020 23:27:04 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
