## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:1ae453421a71699345e895c1129a8fb503daf7982c5fec4c51523c11d229034a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62820e5ff8aec5ab9d872ccc3e1f5a64ec85fc4849ebeae73e58d54b61c3ba95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8d8a0b6900a2051209904878057de68e54caff42553a1ff3f8b4ddf27c7b22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:13:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:13:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:13:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:13:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb16e254dc465c5893d6aeff18369662c8044c54f5c83bf08e442d3d0e121f9`  
		Last Modified: Tue, 04 Jul 2023 13:15:12 GMT  
		Size: 11.5 MB (11475625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b603511d97f2386a8ab3b1db7d9dee4088d3d7c6ffb7a26eac6df5aecbbbee9a`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0aabc1a8108a3a7a5ff6a06688362f7e3ef8a054d2681c47f391601395823`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b7ca55d70bd6c3371f54cd1a75a9fb89ba8e8dbbe6ccbd1edefcc58a520464`  
		Last Modified: Tue, 04 Jul 2023 13:15:11 GMT  
		Size: 286.2 KB (286218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df3a10e230ea51013bab8caba261407bfa609c9c15f5f03018a2b73e96d410`  
		Last Modified: Tue, 04 Jul 2023 13:15:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b94c90aadb2c204e7bd6394e5985e1770861ea491ebc26338ad53013efbabbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb194f65a1b70c1548887e06ca9e554d24f961aa84bb8e8e8af92a8eb54eba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5339efefb62ae359de57f76cc7c3abcddcabc209998c1163785b6d94dc057f0`  
		Last Modified: Tue, 04 Jul 2023 04:06:54 GMT  
		Size: 11.4 MB (11438867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2178be8dad69d8c80854a04cb17b21e471f0bbf2ae4a86464ff32e9970e33378`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58976cca48524ce8dd67a80e399d538d3fbef3d3f6162f96d5178183a1549de`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2da580b40ebc70f119ee6e12f89303261f8bdc03a02215e3d987f228e3067b`  
		Last Modified: Tue, 04 Jul 2023 04:06:53 GMT  
		Size: 286.6 KB (286624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c5b6175ba7c9e5a7370cd8b462ba718539b94f4b43ee91c28ceb2d38e0d95d`  
		Last Modified: Tue, 04 Jul 2023 04:07:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1f39faf94344b4725d91ca24cea26a9ce1a6a1a21cabe07df459db3cb190efc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62862289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a609a69a151edf20931cdebcdde41828431bb1b08d618a64071dcec52cfe0adc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:29 GMT
ADD file:f80411b5104f2db2a54b08d2fb1755fdc31ca042be72f3b3165979726a335a02 in / 
# Thu, 27 Jul 2023 23:40:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:27:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:27:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:27:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:27:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0cecd19dc43936e99574e6dd27db4982f7645bc158ab590b29cfc15e2c4f23a`  
		Last Modified: Thu, 27 Jul 2023 23:46:36 GMT  
		Size: 50.5 MB (50473688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7f2e1cde6914fe23854b6902ae0a8fff8f1f0a5d8ba072e01d078cdfdeec8`  
		Last Modified: Fri, 28 Jul 2023 00:28:39 GMT  
		Size: 12.1 MB (12099954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aabb1338e505c29ec6fa33c90e2e7459a0587bb0bb0975ecdf310f2e15df2f7`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153131614253cf9252fcb4ccf05b60ad52afc2fb119dd115527e601b2b76d46`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd2ce3714afd4b50e39cf699cef7cd43812425d907d1160bc9bbf94b9c9d10`  
		Last Modified: Fri, 28 Jul 2023 00:28:37 GMT  
		Size: 286.2 KB (286244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd05bf720bdf0a12d29d89a095980633f86f45b748e8ec46dfa8715f06ce9ba5`  
		Last Modified: Fri, 28 Jul 2023 00:28:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
