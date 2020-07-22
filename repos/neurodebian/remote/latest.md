## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:c8510fb397b1a7d719dc27983116074b6a9a1ce3a0bb9fac211753f5d9c50631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:0b2071537b6ff9084afead34eb5157524470326e7909662b903c1ca3742d52d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61192212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eeefca8820ed446c7065b02c97d21510696bf7225a297bed6c1736c57d8639`
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
