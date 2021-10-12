## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:fd9f6cd66e12b539bfe6b1f67869d99074ed7adf1d9274f7f271dc2712ffa0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:5f16dddc82e7eb45b787d53324417557ca5010b80afb71cc4cff6957add2b0e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67333840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88807efd01d99ce9eb60c83ca50035afe5e146d72cda8249aa42843e753e0df5`
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
