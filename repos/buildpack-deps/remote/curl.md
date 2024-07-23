## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b285b1cfe7eebe9a09b12fdf16d7e326ce902037c687d784bdec62cf0f512256
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5c00b1b02a702a0a5c10a0c39de2b3534ca77f48014eb9369879b46822682885
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57307da48a041f146ebc02cade9cff052aedd24b9c9c797d99cc488097c920a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d2f44c22fd4532965fb02333473e85c6d3ab86609da43e49d723754abe3d1427
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722b23eda8fb4d3431b7031cfae4c188bd177309d8390d5b4e53e97e3495e498`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:56:49 GMT
ADD file:983ad82e1f35e444cad37dc64834e9c9e172d4335ea328a24fe5d009d70d58ae in / 
# Mon, 22 Jul 2024 23:56:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2103702bb8398b16f1bda2e89255e26b7a0141cd10dcf946690d760d4402196`  
		Last Modified: Tue, 23 Jul 2024 00:00:53 GMT  
		Size: 47.3 MB (47320379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee1c099139cbe59b1878b46c83329d4cf446719eb18cc9d218c3a093a7a059`  
		Last Modified: Tue, 23 Jul 2024 03:51:58 GMT  
		Size: 22.7 MB (22729513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:425da63e21a8968bab7eab3050f542ae6a46e81ba6972b5aa4198380192c407d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67102785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0795e70b98c0048818600534dd4db827d5f7683f4a675ce9e2b8f51cf5a89d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a8155f724f1e6e368526d3793b1e62b186bc19d14d3bc9017ac2b29aa075cb8e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc5c4b620ecc5a3f564f49bbc825a6843e429303da6ec5de922ca9a2fe13fe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bdf54b2f808e3990b7498c35f230d3eb509cd2280622e6529039bd2cb64795ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8183189c4f926141d9fcd3f4ba7a1c216409847481eeb12165c1774e5e2338`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:59005510b61f0f0ef977e4f2962bab45b50e47a53845aa5cc1d7786d44a5ada4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84595c9eabc4b54f273d65e511c9cf48b6e5d6e8409b6ae5813074faa4797603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44a13b4fd2ecaf87d3361e50327286868a7ff3b7a41b6e877c1b5e4b22990de1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79252579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3cedc1cf1f38c69c9e9ccb44c8ddcdb8c4513da74fdf516f7837f69ad38b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6b42e6b8dbdd9cfe8f865b7b7e3f24f0c902f08fad4f5ee71ad91cfc1eaee04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13456429367f068f0a2cd22da31db81103299aa4b4714e95244a0eb0a3defd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
