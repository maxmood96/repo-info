## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:06f7011942dd7a1f821cf4cb3d74873ba287142c34d5b2d70fbb8e6f045f40d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:282fe1d8a89999da7069eb31bccb8383864608e1745ba02a475af0ba48c60095
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52249285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ac51cda11e20e0eb1f6de933a44edeaf8af99d69cf9fea6e54879cda28b7c2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:19 GMT
ADD file:80aa4dde5bfd685e5e660dc6ff1db4713d69bacf53ff51b7e85f8fcff80513eb in / 
# Thu, 02 Dec 2021 02:50:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:56:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:56:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 Dec 2021 09:56:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 Dec 2021 09:56:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a44d60f8dd45ac8efc157e797930e23cf3e360bb4aae7c745efcb02c562c3e4c`  
		Last Modified: Thu, 02 Dec 2021 02:57:12 GMT  
		Size: 45.4 MB (45381394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6750291fc9643c27ff88749ef374721c4bc3e08a83ea1708cab7b01a1de861`  
		Last Modified: Thu, 02 Dec 2021 09:58:25 GMT  
		Size: 6.6 MB (6572286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f19581e4be1c28371b818e7529ef09faae2d773c9d2418a45c8d840b4e71dc`  
		Last Modified: Thu, 02 Dec 2021 09:58:24 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81afc7dca1e335a83b9a2c47c11f5a55c39633013d6c1908e869b74c649274d`  
		Last Modified: Thu, 02 Dec 2021 09:58:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476d569c091568cf6f5fbae159fa97ddd37d6ed2a0635ac8830c43d7d55ebc4`  
		Last Modified: Thu, 02 Dec 2021 09:58:24 GMT  
		Size: 292.2 KB (292200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
