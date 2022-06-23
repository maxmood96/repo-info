## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:b19025849b1c36591bec323fb4be24ee4e6bd9eb3205ee44f6c021056655a550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:52cd0e2e122c9b8c4e9b11ecbf50377c98c4ec81b5cab6d42108f192de50443d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65155050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89593987c5bd9ca62ebbd47dc8eca2f3f660ee16236177cc7ee02578ccbd743e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:33 GMT
ADD file:5d253befef9729db59927d6e0d60fc3d68d46edea7e014babd24f72ac3a437bf in / 
# Thu, 23 Jun 2022 00:21:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Jun 2022 04:10:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Jun 2022 04:10:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:10:29 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d3673f28ea1768e72855620961143c989d7f371e6bca9954aea151e92c37b180`  
		Last Modified: Thu, 23 Jun 2022 00:28:29 GMT  
		Size: 53.2 MB (53218973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844328a253d484e7224b13180445ba3ad7c23f089bb743954bfd25524ca92da5`  
		Last Modified: Thu, 23 Jun 2022 04:12:39 GMT  
		Size: 11.6 MB (11642281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee3deaf400fec71355a69e39e20d239b8567e22eed02736a716920ee37b73e`  
		Last Modified: Thu, 23 Jun 2022 04:12:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ace2bb8a17a61b1d079aa289a3e7e93e431f95e4a62bfa6e363a8b26722978`  
		Last Modified: Thu, 23 Jun 2022 04:12:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5d7ec8a7ba32a8fc5006ad06558cce39906db0baef5ca078ab36d9479a7af9`  
		Last Modified: Thu, 23 Jun 2022 04:12:38 GMT  
		Size: 291.5 KB (291471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739ca3ca498c9449e2d4d77507bac6368df5bc988cc7ad90d9254c770bf9251c`  
		Last Modified: Thu, 23 Jun 2022 04:12:48 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
