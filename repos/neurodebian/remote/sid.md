## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:8fa2edb0a3acec90be3e267dbd486c3d72ef24d846c262198965aa9079e3a7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:ffed9751a17ac2f0872f7f3ecc27720cbe03623a464ae89f3195ab303d7a717d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62918252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7358bf8e3c1fd9dcbefc3cdb7b7ec0e975ba2fe7ba6ea0b378bca6811f9df4cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:40:05 GMT
ADD file:bec180e92743e5024fcf273019085a4de227f49fe65e76828b9c7f740fafacce in / 
# Wed, 26 Feb 2020 00:40:05 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Feb 2020 06:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Feb 2020 06:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ea0d19362f06fe2b59b222ce913ba48c67c375897c1011c35ae714403602dae`  
		Last Modified: Wed, 26 Feb 2020 00:46:06 GMT  
		Size: 51.9 MB (51852485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf8533d1ee23b676483b766a3a686c86db8295d8f11e4bbc8dc4be24c13dca`  
		Last Modified: Wed, 26 Feb 2020 06:27:26 GMT  
		Size: 10.8 MB (10764570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985a2c37ac8316814a1171103bc308597b264592c38d6edcbf1d4945332d523`  
		Last Modified: Wed, 26 Feb 2020 06:27:24 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae03c42f6ae856b8fc9cb2004f560a222a29e7689cac7ba3e1d32d10789be66`  
		Last Modified: Wed, 26 Feb 2020 06:27:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9703e8bf7a1adba7373ebf8be2d20d51448ea1a30df122fb94b3aaa883e4a93`  
		Last Modified: Wed, 26 Feb 2020 06:27:24 GMT  
		Size: 299.2 KB (299198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
