## `neurodebian:hirsute`

```console
$ docker pull neurodebian@sha256:7385a5023129b01a4b02ed9229e193d33810441449993c9f0f82d258cd47143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:hirsute` - linux; amd64

```console
$ docker pull neurodebian@sha256:bff1efcd9743c627506e21e0d1dc5f455ff4963b1c5168a812ec623c3cb9d3dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59636c0452ae01455d116c48f4ac2ebfc4e6058b46a920090363ca3d157695f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:15:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:15:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:15:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56df5ecf752059653014e714bae6507778c2fd9f6c3f864fdeb0f11be5318b`  
		Last Modified: Tue, 27 Jul 2021 00:18:24 GMT  
		Size: 5.6 MB (5597737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d996b67eeee2532d9643e28004d43fba9c80c19ac98f2b5378cc7fd200041`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35723c871426551f5e5c91aa3caf285e3fbdd3819e9baba7432cc48fa90afc25`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df43dcede292226ffbef4971d7b79425f61a336e7bf892f24f89f0cde937e57`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 249.5 KB (249455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
