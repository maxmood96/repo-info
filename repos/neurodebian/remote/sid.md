## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:9796b81df9997efd90e294486895efcab270be12db718e32ff5465832910a30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:e3fc4c199a78bd720c3d6efc1480921059acdba29d14aa0e0d2b027fb4840452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61425712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5c862757fe429e6f9c7effef1ed6e49ec047015399a724c45866d6a77c9c47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:24 GMT
ADD file:89538c836015e15bfe955d940c080e251ce5b25e2cfaac73d8ce77f8475cd08f in / 
# Thu, 27 Jul 2023 23:26:25 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:27:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:27:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 02:27:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 02:27:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9828fc546889681c4c23160b0ee9abb2a08f99ec58b166856cf38d03e0173700`  
		Last Modified: Thu, 27 Jul 2023 23:32:15 GMT  
		Size: 49.5 MB (49462924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840aea7030d9b7dabc9a9e7ac176c2afaee036b8822e4e235737c372f3c45892`  
		Last Modified: Fri, 28 Jul 2023 02:29:20 GMT  
		Size: 11.7 MB (11674727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc14ecfe964d836194b6df1632947dc79cdd55228bb33fbb443297e60c5b75d`  
		Last Modified: Fri, 28 Jul 2023 02:29:18 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3042a376e8a0a0b92f5871751382e18bd488d3ba9f193154dfa0e67916662f`  
		Last Modified: Fri, 28 Jul 2023 02:29:18 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0d0a72915d5c314e64c3c44c22db8c37e1d86c28686f064258c7b7b42ae54`  
		Last Modified: Fri, 28 Jul 2023 02:29:18 GMT  
		Size: 286.1 KB (286051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:26c493c1871d1cc2caeea5e545e5b2c631929abafb545ecf4957f7b83bf1d0fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61210069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed1e107f267b91f3daa33a4eda91c308b6f77e77317ed626441ad1586d6f3b`
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

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8de06f8e3299736ad3ce983e2f9ef19372787757135eb8387320d7ddd052b938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62861896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edec188a835e550ecca1cd7eacd796bc31389979e13e512a9f4cdd132aede9`
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
