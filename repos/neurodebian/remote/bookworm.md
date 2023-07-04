## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:d704ad1e2db79b83b704dcd02e8d45d5f190b38146cc090d2cbcb683e562bd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:9408c6458846d7c42a21b7c302a322ef199d8344ae1c519c81e970aa329d45f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c705dc58062c3ff83585879d84a591b8da0f602fbc704b07b8eaea2c6d025e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c1f16cbc7d1bcc96dabf3be292b695386d113dd9f6641ac53d6214dd474525e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61287919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b927c43cfa476937ffa3952f9fe68f9896e10dd2c6a3e57330b2c9fb455a52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:1a9ff6f00b37aee4da2fd5206e2d3ca904a66bb863e64b8381ead1e3d3b68972
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62733956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961a639d180e3b194c4566a832aa0f16dafd4dce9db72503f7e25e9949eaab3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:25 GMT
ADD file:e0a25fe261e09183ec383698ab2c800f93c5b0805564d7104ad5119db52cccb7 in / 
# Tue, 04 Jul 2023 01:38:25 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 08:58:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 08:58:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 08:58:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 08:58:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:381263dab43af8bfb8e85c7a9a32f35492cbdcc3a046b35f947cf3bf3a55f4c1`  
		Last Modified: Tue, 04 Jul 2023 01:43:02 GMT  
		Size: 50.6 MB (50562388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271310138079c7c38841b341c943a05af54e12fdf28ea867dbd8ecea50d3869`  
		Last Modified: Tue, 04 Jul 2023 08:59:55 GMT  
		Size: 11.9 MB (11883208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4486799c92d32c3a019e571b50d6fba06e3b733cefe9f393aabf1a257f2f1428`  
		Last Modified: Tue, 04 Jul 2023 08:59:53 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a145ef79f2e80a5cec92ab07168fcee7bf316a1894add27bf4cba79ba175fc19`  
		Last Modified: Tue, 04 Jul 2023 08:59:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def654c88e499a00447e795a6fe52ad9bed8e53bb98b18404134acd70fa51769`  
		Last Modified: Tue, 04 Jul 2023 08:59:53 GMT  
		Size: 286.3 KB (286347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
