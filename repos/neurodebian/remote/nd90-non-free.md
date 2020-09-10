## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:a40fba63307f3dc0b4d893d3a1cd4e63e6dedce10d39ee87a144c9f0f835929e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6fe795b37c83bc87e0bbab26feb801298af553a50cc884a9b33bebb26915ae02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52231134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af55ab4ccbc447fdfc620792e4b61eaf67c43795e5c448aa6e2c5f2bbf99c9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:29:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:29:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:29:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820b59377bb61d09daa8ac34a9f3df25be48972003704bcb12e6e13a7f00009`  
		Last Modified: Thu, 10 Sep 2020 12:31:49 GMT  
		Size: 6.6 MB (6568552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdb1d1978244c3811191c8254dd83e882436c19d036de00f8564404db24aa4`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9d62565b438b5f15905601c72c67a69d1809d385530c74fdab53e8cc0db88`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12442eb22cf1320c74e5fd16277cc2dce1ac630bbb80b8056d2a01847a8776f7`  
		Last Modified: Thu, 10 Sep 2020 12:31:48 GMT  
		Size: 292.1 KB (292093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd4c3862e2ba86b98ac096657efa1bac320e289dffe4ef95a7267471b092815`  
		Last Modified: Thu, 10 Sep 2020 12:31:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
