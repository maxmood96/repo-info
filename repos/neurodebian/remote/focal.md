## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:4edb28dcbd20d4d4edfedc8c1c78de5933e918c2cd537025fa8e7795216226a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:fcc9975228aa54c9b819de450a91c96d06a3723e3a6e7b653cb568dd2393fe7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeaa060e12baeb84bf1b41aa26cdbf4c2c53d3726e69e0ed086522a7175f6a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:12:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:12:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:12:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181b23a20725abd31982685ba6ef94f9c18f9b4715d5413a59cf785746d88b23`  
		Last Modified: Fri, 18 Mar 2022 08:16:33 GMT  
		Size: 5.5 MB (5488532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc0a34dbeb5ca294abf88cbffaceed4bcb3a84170048e12e84e38d9c8675d22`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09414e5157753ac2e1ab73492fccc7b48fb65f1937bbfe26e3e959a1fae9e0e`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dcb7d6ca3e3b5c1f15c6c7bf23a38ad1e13b919a24a1b6169b625a3a7ee9a`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 238.1 KB (238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
