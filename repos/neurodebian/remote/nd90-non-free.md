## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:3a7da32d4bc1d0d8aaf10ac9d3f8cb877c12ff0f24264e8b49a6ea8b87b3170c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b28517f415f4fbb2fd82e2fc1c398f8590e269461a8ad373af3886780caddf2e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52238038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97c1c24c2947e2f757bc1d682bc20ede75a105f2404830e451845ea40b49022`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:24:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:24:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Feb 2020 06:24:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Feb 2020 06:24:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:24:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03652d539f4bda6c178c7233eefa94e9e33ba545974209d2c95c1c2c406c9243`  
		Last Modified: Wed, 26 Feb 2020 06:26:49 GMT  
		Size: 6.6 MB (6566584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f22fda5774df4d376809c38183671dc588a7bef2097b6fab9d9ed10df47546`  
		Last Modified: Wed, 26 Feb 2020 06:26:48 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece0b84543e485099d1e4599f9c6a4a0a910e816b46bf2e6832655720bf0b8d3`  
		Last Modified: Wed, 26 Feb 2020 06:26:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0780d0b92a8e6a4f9786792e9c60df90482cf82c848d5f60738ac1f11fd9f0d9`  
		Last Modified: Wed, 26 Feb 2020 06:26:49 GMT  
		Size: 291.8 KB (291763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7afff2970874823af8ae1bc6890f15c27c443f881ba2bdce207b16f297f023`  
		Last Modified: Wed, 26 Feb 2020 06:26:54 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
