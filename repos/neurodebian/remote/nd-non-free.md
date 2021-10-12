## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:b94c3fc57e499e839428c1fd6e8466afaccfa93b00b7e81b7e7ab64069b74a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3b908021eac2d9c35805bcb971cf5be03c8420e1a13e9dcb412a9f3f37bec95a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67334156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16ed44c7be0d02a81a26eb7088eb15dc07f453ced697eb6a46b81fdde15ed30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:58 GMT
ADD file:2d684471f088173801ff86eaf94c1d858b74220b84642d73b02bd1bfe0d54b60 in / 
# Tue, 12 Oct 2021 01:21:58 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:58:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:58:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Oct 2021 09:58:34 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Oct 2021 09:58:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:58:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ba87283d9c312600aafb7f4149986884d524aae42e0701a90d2fc23c85e977b1`  
		Last Modified: Tue, 12 Oct 2021 01:28:21 GMT  
		Size: 55.7 MB (55687470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d20e6c928059ba15309df9f9220e5a4d69b7c4047ddc44732927d198e3dc4d`  
		Last Modified: Tue, 12 Oct 2021 10:00:38 GMT  
		Size: 11.3 MB (11337603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8ae0fbcb66b36d840b6178fddcd53d214a6f74778df763228c76900c37815`  
		Last Modified: Tue, 12 Oct 2021 10:00:37 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420dc3b7fc1ad15ea645f1046c38aec1d4793a30ce24ff8bbec91310de2f6b0f`  
		Last Modified: Tue, 12 Oct 2021 10:00:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b4a78043a9f25e9f79a679775e89c978fca043df07912bde6d47d65fcbb66`  
		Last Modified: Tue, 12 Oct 2021 10:00:37 GMT  
		Size: 306.8 KB (306756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e044adbb09cda3958278d99d339d93e12307bc2c4ba645dca4db312c7f683d2`  
		Last Modified: Tue, 12 Oct 2021 10:00:48 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
