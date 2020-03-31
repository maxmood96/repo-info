## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:118d4906a4c65886a9852116703fccf1e00c590bacf8ef2517c355f6547d81e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5db7d24127ce73c49b146de7e536a33da42576e2aa0eec1915500cc9de613675
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61183915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd85fdce30a9eaae7b40cbcaa602a1c3f398d28bc55caa8c1ad2a3382cfdf481`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 20:51:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:51:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Mar 2020 20:51:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Mar 2020 20:51:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:51:16 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6213348df44c43095f6871c3d111901c8d74130ec85a26ce3144fba62d2ebf1`  
		Last Modified: Tue, 31 Mar 2020 20:52:52 GMT  
		Size: 10.5 MB (10497139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c46a44d56ea616a5d381778a7ecd1c679c7126efbc7b6116a81cd58d7243a`  
		Last Modified: Tue, 31 Mar 2020 20:52:51 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff343ecc92322c169bf0582ead820113d1c9bb6096dd92673c052890c967578c`  
		Last Modified: Tue, 31 Mar 2020 20:52:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07e0754ba4f099e47d613aaaeb3674c80477070ecc82e03920bb8b8d1a1be0f`  
		Last Modified: Tue, 31 Mar 2020 20:52:51 GMT  
		Size: 302.4 KB (302363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f315dbf515a634b905977fc8aaa179cb387d228e4b4340035e8815726d7dec5a`  
		Last Modified: Tue, 31 Mar 2020 20:52:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
