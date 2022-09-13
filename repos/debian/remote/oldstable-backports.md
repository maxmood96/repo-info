## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6a5da34cde7372253a2aef6bb0c4b246813a8ba1a613ccb5f799578c6de7f602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:950f772a83d9b163308a2cf34f1a9804b324e968a46152969da43832f20e68fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50440602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a741669898e8a2911e2674b401ac93bb880b33810826a03b6ac13844aa827357`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:57 GMT
ADD file:ee981dd66a540953de72a5a2eedad3dd86c907140a949981cf8f3a879584bee6 in / 
# Tue, 13 Sep 2022 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:57:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26cf2e88423366fb12dd62fce8e546f7debcd8109023d26952a00572917dd10e`  
		Last Modified: Tue, 13 Sep 2022 01:01:36 GMT  
		Size: 50.4 MB (50440379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039790036087637f4795fd922b4b4cd7bc1db5169cf3746b9c35b26379d8bff7`  
		Last Modified: Tue, 13 Sep 2022 01:01:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c114fc25023213f79617e1b474038ccf3dfec03118b6042e293b557a854da10d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381120fb05dc4cfc495f7b5a727190a8fff1757727837191d678597d56f39f5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:43:31 GMT
ADD file:da366e73d3a38bff8247b3823c985ce384b055ef89c30aef5da216cf53875e85 in / 
# Tue, 13 Sep 2022 03:43:32 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:43:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f418d594816d516e165bb0f2f2fe8b3af83f31b6076c9645e7c8319a5f553f2b`  
		Last Modified: Tue, 13 Sep 2022 03:51:21 GMT  
		Size: 45.9 MB (45914886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7210d731e75c53ff7fda0e790f9116584b3e46510ccaf262f8188c56b5f8f0a`  
		Last Modified: Tue, 13 Sep 2022 03:51:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8ffe9ac1bc3641cfb8d110fe478b3e9c8e9ea7d9d73142676653e04ee4014829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49228502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d147c8e47f41950f8479582febce98fd3784f11955146b19c24c3845a8cd76`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:31 GMT
ADD file:13b72595a2f5ef1cc575252308cabc6a30dcd88889ae2ed5c5ce852ddf6452ef in / 
# Tue, 13 Sep 2022 02:11:32 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:11:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a908df6e35e096efbea91ddb7a6cf5d32f7a0e3c5cf9fa8f43b1e42a1d1d0433`  
		Last Modified: Tue, 13 Sep 2022 02:17:33 GMT  
		Size: 49.2 MB (49228275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163d8926a8c3ab851d9242f0914e51926ef594de499af2066bae800746b057ed`  
		Last Modified: Tue, 13 Sep 2022 02:17:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:19e112c0ba69fc0f6bd63666f1b1a613b950bc751f3b5e2c5ebfb53317c6b52e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51203212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6035e882fbfbd5ce57f8ad3d6ae958b50298260f89ef755dabd1693fd750a87`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:23 GMT
ADD file:3cc7f0418aa4cc909283ae51b68f4e0d8c8f29c0e2cf42045c0c13a9827ae164 in / 
# Tue, 13 Sep 2022 01:40:24 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d005eadd3a7602c72388e3093f867e996f3823afe5bfba0140edb01842237ce8`  
		Last Modified: Tue, 13 Sep 2022 01:46:36 GMT  
		Size: 51.2 MB (51202988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b8e50f823dc7e46b278ee4e594623d5418bc6ab217eaddf8a7d9b87db598ed`  
		Last Modified: Tue, 13 Sep 2022 01:46:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
