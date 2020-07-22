## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:5bb680b72d81a24843b2f79048769138bacb6ab71654a8aa0c15d587054948d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5bb347026834d0318ff388edfd8f5a688528d4de522a27a8c0489c6166e704fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61192577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d535e0e1215c172dc328f106f516c7132dcfe322fd6fea59739ae1cc4ad9bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:24:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:24:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 22 Jul 2020 20:24:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 22 Jul 2020 20:24:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:24:38 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952a8c46ed5cd7911cc6b2d60c22a9b7042a6a4b0a181dc2cd02529be1d073ef`  
		Last Modified: Wed, 22 Jul 2020 20:26:32 GMT  
		Size: 10.5 MB (10497424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a7bd7bc0c1f821a9fe7713ec37b5e0df4b487e075e0ae5e7b64a8c467141ea`  
		Last Modified: Wed, 22 Jul 2020 20:26:30 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97bcfd3841a82794325273ed8097a37945d2563ae0fac8d5de84a1823c4ef61`  
		Last Modified: Wed, 22 Jul 2020 20:26:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f866de3d751256dfa6c4b75b1baeb39cd3ab59a923c75fbb06de5e20cd5db45`  
		Last Modified: Wed, 22 Jul 2020 20:26:31 GMT  
		Size: 302.5 KB (302461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d08568ffb2c12f3405b14a44da696f013eafe99424fc8f29874b2181d949ed`  
		Last Modified: Wed, 22 Jul 2020 20:26:37 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
