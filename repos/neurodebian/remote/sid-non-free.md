## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:abfba739fd3e35a32586532746e52a4fcc93fe50374682aae2ac7b13c7557c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c515edabd366dc893852089eb86260a3df5b3ad709bb0efea4de241a2284b00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62671454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f90518e6b1c19e4ddca43a4fc0662edf298b08030612fa21b5a7f383f72e23c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:32:06 GMT
ADD file:996aa79c0149eba494ac6e8283d067afe487aee84826f7465eec6c90b31702b0 in / 
# Fri, 15 May 2020 06:32:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 09:18:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:18:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 15 May 2020 09:18:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 15 May 2020 09:18:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 09:19:07 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8ac18c4af62244baacc9c403ddabcbc93ff4f66dd511fad1608635f249ebee97`  
		Last Modified: Fri, 15 May 2020 06:39:45 GMT  
		Size: 51.4 MB (51398338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2493a7e842b403e623d53849472cba907aaace140fc1504832b8bbedd75b8`  
		Last Modified: Fri, 15 May 2020 09:20:29 GMT  
		Size: 11.0 MB (10971354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eec73f58fbfe92ffb8143912cf6ee367f734f1a9c106406967fb25f6a69e73`  
		Last Modified: Fri, 15 May 2020 09:20:28 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cacd4f72194a6d362ec1311a334df444bfc98265482cc175fda86789567dff`  
		Last Modified: Fri, 15 May 2020 09:20:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3b85b939c7c2c747df475b4e28901e708b7cf4d1c6a971a380138146e7b819`  
		Last Modified: Fri, 15 May 2020 09:20:27 GMT  
		Size: 299.4 KB (299438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ec4d4a3f24344d6637895dad996dcf41a34fd8b3a762ee4b924e70bff05d2`  
		Last Modified: Fri, 15 May 2020 09:20:34 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
