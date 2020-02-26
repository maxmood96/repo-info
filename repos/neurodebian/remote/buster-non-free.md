## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:2f407f148f4c6852aa8469edba2df3b16d9a6cabd0e419fda1d1d2d9767ff61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc3b28e35c306aa81d2b5c491730b576085db367e84856e689cb7d002e8c8970
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61183149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8484fd8783cc1a57af23b48308b5b4f8d9ab32d9171b167fa508172ba9aa3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:25:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:25:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Feb 2020 06:25:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Feb 2020 06:25:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:25:27 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8238d476f2405997d6ef6c05578102d634d2b5b686ef421b81e5bb879ea6112`  
		Last Modified: Wed, 26 Feb 2020 06:27:00 GMT  
		Size: 10.5 MB (10496946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f71007ca951cbfd161961c69f5808617f744a7a67a3109f238497a6d18749`  
		Last Modified: Wed, 26 Feb 2020 06:26:58 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93576a4d19d671a7921b4895e2f05a731c3255250d1a3cbc88b791ee474a9044`  
		Last Modified: Wed, 26 Feb 2020 06:26:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870df3caa1d38885d94f35c7f6b3b07fa30bc3e47278def7694bbe6392eb99d9`  
		Last Modified: Wed, 26 Feb 2020 06:26:58 GMT  
		Size: 301.9 KB (301864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e7b03f95ea3a917b89b50ce343a579f3422fb9178fcacaafdd245bfbdbd4a`  
		Last Modified: Wed, 26 Feb 2020 06:27:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
