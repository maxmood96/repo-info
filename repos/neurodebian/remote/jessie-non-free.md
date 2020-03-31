## `neurodebian:jessie-non-free`

```console
$ docker pull neurodebian@sha256:d98fe2c319e38f60c7c1874733dade2d770f7f860d8fa26072a3ca9b66e60f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:jessie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:71c0b8542f9aed2c5fbb381eae6631011238773a5342fc112580830ccc0c9411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54695950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cf405e863a434ac2bcba2494048185bcc6556c88671e26a98c0f0672155a59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:15 GMT
ADD file:00e3c0ca649cf82da02cd7fec7b3121205c2c54c4569209a2212c4924c73d5a9 in / 
# Tue, 31 Mar 2020 01:21:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 20:47:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:48:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Mar 2020 20:48:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jessie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jessie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Mar 2020 20:49:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:50:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:f27d6ed8cebc4be4a992767cb74cd433e5e145ae55c57e9e913e47d315b1dbdf`  
		Last Modified: Tue, 31 Mar 2020 01:26:56 GMT  
		Size: 54.4 MB (54389951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bc51fac17f55e47b723826a5fa2ab28f5ce0de99e4cbe3d42650878afd4538`  
		Last Modified: Tue, 31 Mar 2020 20:52:34 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c003bea6fa042c6a884bd9b28b240e28cc0a5b556e7706bbd3f4b7dc465c876f`  
		Last Modified: Tue, 31 Mar 2020 20:52:34 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b249a2a79f8e97fdd10a95422fbfacb71acc7c4f34f7fdd46a86c89ca3b9573a`  
		Last Modified: Tue, 31 Mar 2020 20:52:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d6b0008063addac631759a44b7f461563dc872e8aac54f0f40bef61e64bbea`  
		Last Modified: Tue, 31 Mar 2020 20:52:34 GMT  
		Size: 301.9 KB (301933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6f376b4d3fb7e03a99162ce5f3f3d250410f7f3db2203c79faa9cb3aa0a89d`  
		Last Modified: Tue, 31 Mar 2020 20:52:38 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
