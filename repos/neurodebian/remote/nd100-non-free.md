## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:b9c46136a8766cabf3075d0c692e0512224c69f04cc9879c31c0a3ecfaab4d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:268be796e6d03fe394e321ecd348f4a144fb8ea22185e5a6d5988a48d9e414aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4c1b3d5cb79f691e568f7355790ef8ccadb57036ba8e332d62462c295c680a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:09:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Jun 2022 04:09:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Jun 2022 04:09:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee300f013dc064203078ae7d6f274a9e8b4e786dc742c675355ad503d1184ad1`  
		Last Modified: Thu, 23 Jun 2022 04:11:35 GMT  
		Size: 10.5 MB (10500341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c189bfc5fef2d92e33e872b998b588a625d611580bc9a65f07ff1d40b271ef8`  
		Last Modified: Thu, 23 Jun 2022 04:11:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d2dc0ab943724a75b3bb8033b003f7b0906d8cc525808ac1f86682d1ce80e5`  
		Last Modified: Thu, 23 Jun 2022 04:11:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73cebbeea1bac8521821776ddcfa64934f572eb2b27b4eb52c5c1c60e621145`  
		Last Modified: Thu, 23 Jun 2022 04:11:34 GMT  
		Size: 302.8 KB (302809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5385b650712e5f2d374444604999d21c4e9db9342ec50d9a21f58a58d336fa83`  
		Last Modified: Thu, 23 Jun 2022 04:11:44 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
