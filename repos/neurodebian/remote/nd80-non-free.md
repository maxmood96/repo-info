## `neurodebian:nd80-non-free`

```console
$ docker pull neurodebian@sha256:c2bce196899041e0ae6d07a8423127cf56b7675736f954820df2434ff74b3fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd80-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7481f92c24adde6bab08a1ad461e3f5e4ca312da887ee06eac972ce77b847900
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54695021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0865adfb16e2effc70cd7adbb7b203987e4f1ea9352d08d00fc48c2354607f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:24 GMT
ADD file:e48eee8ab995f46a82f22f02d440c47dd43ef32a3571025bc45f86a2c91e7172 in / 
# Fri, 11 Dec 2020 02:06:25 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:09:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:10:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:10:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:12:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:12:15 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ddb275440fbd86c77395ede5bb7c40089858ac72f636975926ac7e6eede3ccee`  
		Last Modified: Fri, 11 Dec 2020 02:12:45 GMT  
		Size: 54.4 MB (54388992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bccc7f9098027aa282bd8bed03daf55b6ddab1e4b5f39736d71c305d186589`  
		Last Modified: Fri, 11 Dec 2020 17:14:46 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fc4df7762a98c24d70d7bb76248cecf8910a66acc02d52d48818b6c24133b`  
		Last Modified: Fri, 11 Dec 2020 17:14:46 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f13621a999b1fc559f5cd55f36dabcde2f592efc6732d43e0d0edf9579b3d0`  
		Last Modified: Fri, 11 Dec 2020 17:14:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2c8ddfcaa3ea891f9b170d00d9eb7ee7dcfce5d866415623156f64fe4c96d6`  
		Last Modified: Fri, 11 Dec 2020 17:14:46 GMT  
		Size: 302.0 KB (301972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f3f758e4213eae9dcb9531d23f220d148d3d53b1b446054c7d2d33efb3e97`  
		Last Modified: Fri, 11 Dec 2020 17:14:51 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
