## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:3b9d34ab49b08effdfcb29cb0e788e002b58130ec2472bbc064993571fa118b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3db4a27241d1c94b2e9954e21465a20f23fbb00d37516f343ba14ae261622003
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62664164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c476935788f06df0dd2d69705774a7c96b208c3c32a68b93d739056cdedb8fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:27:09 GMT
ADD file:3feae44a900d0e1e835d12f1ea607313fe008d55842495a8cc533e7cfa75064f in / 
# Fri, 15 May 2020 06:27:09 GMT
CMD ["bash"]
# Fri, 15 May 2020 09:18:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:18:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 15 May 2020 09:18:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 15 May 2020 09:18:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:18:30 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5acaaf333e788954dc63603194f262baba7644709169c9584c92237472fe3a9a`  
		Last Modified: Fri, 15 May 2020 06:36:49 GMT  
		Size: 51.4 MB (51391128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f93b6ec3be38d3067d24c946a3decad163a38e87f9c1c47b70313f53176e35`  
		Last Modified: Fri, 15 May 2020 09:20:20 GMT  
		Size: 11.0 MB (10971303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4597f691a3a4c2c87a20f0c275455baaa29e90393d6b05eea58ea581ef59db9e`  
		Last Modified: Fri, 15 May 2020 09:20:18 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f4280227bb7fdc2ba216d49b18a2a39441f51a9649f75414b1609407b0cec`  
		Last Modified: Fri, 15 May 2020 09:20:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a4c8664683266852a54ebbef2d1910b41df85828050eb6e893331e61a2be7`  
		Last Modified: Fri, 15 May 2020 09:20:18 GMT  
		Size: 299.4 KB (299403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f3fb38c6f274115d19f2341e2a1692f6b0c9ff69751e810234131f640a378`  
		Last Modified: Fri, 15 May 2020 09:20:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
