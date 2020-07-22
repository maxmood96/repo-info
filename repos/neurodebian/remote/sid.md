## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:6256eb6fe0b4129ca8e617622ea6bb06eaa080c6c8be081c1cd992ab85371cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc97fef41ec4cac051cc51367f576ce71875ddfef9f2251da36d4cd7771299f2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63731331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a7175f9509593a67e0c0e58a5373d3a86e8ebd5f053a450ad52596e30095a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:41 GMT
ADD file:388f29164844b8493d30bf1feffd1158559ab161886928f977604c10f983a704 in / 
# Wed, 22 Jul 2020 02:05:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:25:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:25:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 22 Jul 2020 20:25:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 22 Jul 2020 20:25:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:babaea2ea26ef0e3e4a90ecc928d26bf25d699e1dcba843f16b8a2f0a153b3d7`  
		Last Modified: Wed, 22 Jul 2020 02:11:28 GMT  
		Size: 52.3 MB (52340330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527658e52f0609345e4c11440758ee274fc25f7519e56181585069869d3a98f2`  
		Last Modified: Wed, 22 Jul 2020 20:26:57 GMT  
		Size: 11.1 MB (11090108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be70fdf3841de13f8d6715fc6f5cb698f8b5c2f37a0c605ad82db251fba17ce`  
		Last Modified: Wed, 22 Jul 2020 20:26:53 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dd0b9caa6e39dd0336b74ea0de2b6b47c8b834747e9e2e672a91ef56127126`  
		Last Modified: Wed, 22 Jul 2020 20:26:53 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faa4dcb565f0b28c23e46693a838c58a183b1c14c615661fc8daad3def01147`  
		Last Modified: Wed, 22 Jul 2020 20:26:53 GMT  
		Size: 298.9 KB (298893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
