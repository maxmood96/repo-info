## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:ad31136894fc55b709586877d938f37923b1e98429e3934bff70a73c633fed4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:18e0704bc991feae346f506544af1a019eeaa64665ad31142e4ca778d8ed002e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52237968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c82288a824ce3b90ca0d81cad00ab3679db3fc60ea396766f54903bbfa77dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:05:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:05:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Jun 2020 08:05:50 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Jun 2020 08:05:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692046f65c2012df2d01ae6a4047a6525c5d259652abd0dadc391ae550af5854`  
		Last Modified: Tue, 09 Jun 2020 08:08:16 GMT  
		Size: 6.6 MB (6566670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff00112ad852cd8d6037b787b9ea2ef15294e1fb853f7a1bde6bb7f3219c080`  
		Last Modified: Tue, 09 Jun 2020 08:08:14 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969630eb72aeb06e68ca13e32082ed4bcecc5af2c1c46943d48a3ad9f51d55fb`  
		Last Modified: Tue, 09 Jun 2020 08:08:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab58cabf7dd549523e2aa04e79780e17b91e7ee2998d12f16d8db684f5ec851`  
		Last Modified: Tue, 09 Jun 2020 08:08:15 GMT  
		Size: 292.1 KB (292108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
