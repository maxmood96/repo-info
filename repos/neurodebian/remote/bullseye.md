## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:12f20bd2e800267e940bd24f609e61143217bf73dcf4f09cb04948118a58b092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:cdc79839ea7bece6c1ccd1b038825c279f5ad73fc3873510b524096fc64a9d36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66540222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fb4fc6464ba7479b5733ea679e68d92b0ad687016c8716d3abb1a3d33a4bb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:58:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:58:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Oct 2021 09:58:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Oct 2021 09:58:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90fd1a61422687dc90af7fcba5d6dbe7497bf8a9e2a8d952db1255a52e0cddc`  
		Last Modified: Tue, 12 Oct 2021 10:00:18 GMT  
		Size: 11.3 MB (11309473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838271a976c6a70566c168b2658370a1f0bdfa972e54f377866a1f24898993c`  
		Last Modified: Tue, 12 Oct 2021 10:00:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832cc04f9d989d0b60dd19a7520a89a1ef54953c8ff5af1eca95fc6a4334a27`  
		Last Modified: Tue, 12 Oct 2021 10:00:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf9d247c9912589f1d44dc2ea502147fa35c60bf52c64afd9e1e8fe6c0b31cc`  
		Last Modified: Tue, 12 Oct 2021 10:00:17 GMT  
		Size: 311.2 KB (311215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
