## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:9735d3338714ef4bf8a9731998f23d716e4566c02345965612aad8820d4dd046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c1150bdd217bd68536d90c931c4bd6dcfd01b05cd9aa2e103df811006291b256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd50d187e2fe505ffe928af1241059e43a216a2fc2025ec3c54ce4a75f53463`
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
# Tue, 13 Feb 2024 11:26:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
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
	-	`sha256:fd80eb821788b3f4fefe7beadbbe8196006f026021883bf5c934c1010f0e80dd`  
		Last Modified: Tue, 13 Feb 2024 11:27:41 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f3784dfab8ec828ea31088933a847225ebdc464356d6e333392c16d285055a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60101167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd7aae38c094a73c6745db1523408720744fbf08195af4495ca26870522dad0`
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
# Tue, 13 Feb 2024 02:27:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
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
	-	`sha256:dc3f124254d5595783d51dc61aa3013384a525787d0dcc5cce51aaa31904ec1c`  
		Last Modified: Tue, 13 Feb 2024 02:29:01 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2ead593cd6cf1c9287b381741cc8f533d9dfde1c1002248f5f3227fb35a03c48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a9e4b85c7574a7cb51eac1827487c4b27214f0ae5a0ba2f037bee5e311cc60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 01:36:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 01:36:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2ac4b212736a73cd9420f691156b31147eb1ca8ee1988c115e09909c595d3f`  
		Last Modified: Tue, 12 Mar 2024 01:37:48 GMT  
		Size: 10.9 MB (10868439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484a1c6f30ccf9fb7ad141bd0f7e4c51ed79e92410c164ce5ff7a08395b25a7b`  
		Last Modified: Tue, 12 Mar 2024 01:37:46 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb8ca7dd34aa93f70d8776900c60c23e74800fd58581f2c48f36c87a67b90d`  
		Last Modified: Tue, 12 Mar 2024 01:37:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f011bdbe7a6cac4b1117d2e44d44fc948dbb3268ae3455940c9558ab1ab07cf`  
		Last Modified: Tue, 12 Mar 2024 01:37:47 GMT  
		Size: 299.4 KB (299390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56739c2f2407efec65fd3cf1b64a28d3dc838b52a31e2230a779f0487157907f`  
		Last Modified: Tue, 12 Mar 2024 01:37:56 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
