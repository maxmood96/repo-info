## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:e1e906d3d393bddb95e096ebd53108bffd3892fffa7857fc19ec9dbd65bc11f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e5f77f3b5217b06e30d4fd39792e17ccbd1f068710e2dbc19afc5577e96021bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66540398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2503e02227b8af29be7d0cf71fa34b579b725099e1ae25591ba57cf287c1d8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:55:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:55:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 01 Mar 2022 13:55:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 01 Mar 2022 13:55:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:55:46 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f77a7899f1ccab5dae03d8e35d6dbe1355b2ffd5671c004e3b0ce919fa708b`  
		Last Modified: Tue, 01 Mar 2022 13:58:01 GMT  
		Size: 11.3 MB (11309644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8367f5c45c6778aa1245842dec42378cf063bc403945f6436fb23113d03767`  
		Last Modified: Tue, 01 Mar 2022 13:57:59 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9486516db173ba548e9864258f465a885a89dec0dc3f61f985facf5e684181d`  
		Last Modified: Tue, 01 Mar 2022 13:57:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cd3b38ef1fe132ea4775e7c6ea7c88aacff4df55014214729c012f881603f2`  
		Last Modified: Tue, 01 Mar 2022 13:58:00 GMT  
		Size: 311.3 KB (311308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d4cf83a4074cd9be2205e9b330ba0cb95a6695700b5c0fa89db33a91d75b8c`  
		Last Modified: Tue, 01 Mar 2022 13:58:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
