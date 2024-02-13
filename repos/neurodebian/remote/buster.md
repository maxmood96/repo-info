## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:1a6f003fec0c5fa90132e7ba5e9a88eba5effd389553349a7d112a067afd6dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:6d208988aa2ae1de5d68bb55c4213bc542345ab30a85c84f613c79efa73c4505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ec10d734c0aefd1d45825f8cf3f0b5bd05bde2a67b91d83bba1aa077f2f826`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:25:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:25:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 11:25:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 11:26:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b1ea3fcf8ef5a959f1693e053afa8bf2cea507be5cb67e4b6b2c89b2395ae`  
		Last Modified: Tue, 13 Feb 2024 11:27:33 GMT  
		Size: 10.5 MB (10504697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378912e11e45fe079c7e4b5b3c3e56fedfe7cb495ae0a1f7182e9376b4743982`  
		Last Modified: Tue, 13 Feb 2024 11:27:32 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c0a4fbee81613df362e196ac310ee64a8c01912199e04d8ea851511e5845c6`  
		Last Modified: Tue, 13 Feb 2024 11:27:32 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d36347ba7ec94279d025eb4f34afc5e8c24ddef31f86192a074a9c543d6197`  
		Last Modified: Tue, 13 Feb 2024 11:27:33 GMT  
		Size: 299.5 KB (299515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f67ad3b15f9c9e364820b3508efad050840475c11f270be57c380515688dbcb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332ecbfe6cda6cb637adc989925b16b605251c26f34f5298fad5129d3271e770`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:27:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 02:27:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 02:27:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf80402a444bb8855219af62c6fb666762ab3a25999f9875cbbcfc5a460098a`  
		Last Modified: Tue, 13 Feb 2024 02:28:53 GMT  
		Size: 10.5 MB (10510597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f8d80f8bf98b26746329b5215ece27e0e0ba4d31ada1106cbdd014ce1648b`  
		Last Modified: Tue, 13 Feb 2024 02:28:52 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f36bf2507fc7844a05a47f5b2f99204740f06029d54345496940c8f01db582e`  
		Last Modified: Tue, 13 Feb 2024 02:28:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402acd463aa46a689f76f804770aba6ef1b93675e37764c38eb62085793b4b7f`  
		Last Modified: Tue, 13 Feb 2024 02:28:52 GMT  
		Size: 299.4 KB (299439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:c5f26fbf1b8c7c357382c7cebdfbaed9f2be87d48f3c458ad5cd154f2de89ad0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba6ce5854ce738ff4d8886c01f345eb3ba896e854c716c99f0d8062840ea216`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:51:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:51:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 04:51:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 04:51:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe762a18a688f9c579732d93875f47e428e1db13bc3f93f0eefe8c0dc655afa6`  
		Last Modified: Tue, 13 Feb 2024 04:52:53 GMT  
		Size: 10.9 MB (10868340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca644617f4a879153d248f1e1c36faffd8f2cf532c47bc52e7b113a2c1593fa`  
		Last Modified: Tue, 13 Feb 2024 04:52:51 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9923b5d49e21b49a80ad7130aa69c3d2fd07838e07b5bfb1eea78add251ca0`  
		Last Modified: Tue, 13 Feb 2024 04:52:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f480e56f2571b6a9e46f1199b10aff770f2d4340005a4c00b2d9a7546b93e89`  
		Last Modified: Tue, 13 Feb 2024 04:52:51 GMT  
		Size: 299.4 KB (299418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
