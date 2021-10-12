## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:640fd7ebc12e19d4b04e8719435af620d21597736e0d4a85a394aaece44e5dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc7926ed69f59c1417c93119a94e76335cd8080a1147f13e3600fa78a4c031cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d858c30a5da56ca1b6936401b8a30deb54c5c1f9f8e5faa9af7981278133ce91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:41 GMT
ADD file:084c8b3d38d578aa3910f3786b67b058962dbfdfd4a49d6e0201f2e91670873b in / 
# Tue, 12 Oct 2021 01:22:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:57:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:57:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Oct 2021 09:57:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Oct 2021 09:57:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f0ef4316716c8b8925ba3665932f8bf2cef3b072d82de1aeb269d6b8b61b84c`  
		Last Modified: Tue, 12 Oct 2021 01:29:27 GMT  
		Size: 45.4 MB (45379651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7699f8bda7cfad1091db29f6f9637c606fae3fa8fdb1a2cc344cd5a60aa5f51`  
		Last Modified: Tue, 12 Oct 2021 09:59:33 GMT  
		Size: 6.6 MB (6572353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7cb83ae6a7f2cfb0c57b1d6e82fe2e25d13979b958149cc547bc96c5c5f96`  
		Last Modified: Tue, 12 Oct 2021 09:59:32 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ab45172f5262b8e8f4b9ec42b97d7dcf1c5134dd18f0307d4b7bc89b26ca12`  
		Last Modified: Tue, 12 Oct 2021 09:59:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927c4618195b4ff2073c461de67a16467f16720c1b7590a541f9aeb28561be14`  
		Last Modified: Tue, 12 Oct 2021 09:59:33 GMT  
		Size: 292.3 KB (292258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
