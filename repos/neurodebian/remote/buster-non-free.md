## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:94bd425d53a8c927244313bd449f95998f68ad67fd05809ad42b3a8be9c41619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:72a41b30b41c24c0808954df56027897dc4eab73df1939d481ac0f0296d8d6f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146ac8cf8de7c83dded2b3563592deeff66652d2d2c0485fd8698a6e0403b0cb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:56:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:56:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 Dec 2021 09:56:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 Dec 2021 09:56:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:56:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d9f6aa9274b18451de391ef01e3243ad95145ad95b71c44d2c4d70bff4695`  
		Last Modified: Thu, 02 Dec 2021 09:58:44 GMT  
		Size: 10.5 MB (10500043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c9a7179822b1886169eb6f60bc8429a8b1936b71f48c6c1198cca66b5aa21`  
		Last Modified: Thu, 02 Dec 2021 09:58:42 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458d044f296f74c565306af2875e6c17dbb84254b77c25121837c250ed8c7ca9`  
		Last Modified: Thu, 02 Dec 2021 09:58:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bfe3af66b26c27a1a3ab5c3a21d235c8cbafb93e59cc06d123b3cd6efea2c3`  
		Last Modified: Thu, 02 Dec 2021 09:58:43 GMT  
		Size: 302.8 KB (302764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d7621f9e4034e7d9fda9640351791d490cab04ffdb2d6a336bdca098e2e529`  
		Last Modified: Thu, 02 Dec 2021 09:58:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
