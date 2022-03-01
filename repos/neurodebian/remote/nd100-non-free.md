## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:6fc4cab2cd06f9e7997a0f3b4f09f5f258ff2f60c1f08e814490cc18c0299012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f32ebe48ed6239d7e141426b250c906f8a03945da2513ecaef93d62e2c2baf34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935e6ecf72c16f0a347d46ef1504c2558d059d98c8993acf46d26d945bd2b67f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:54:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:54:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 01 Mar 2022 13:54:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 01 Mar 2022 13:54:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:55:06 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9fbeee9a8bdc5381072190b66cc3a1dcc2804e7dffb2430ed34bda1bc6b51e`  
		Last Modified: Tue, 01 Mar 2022 13:57:35 GMT  
		Size: 10.5 MB (10500178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28999a09c04389931e7b7ab54bdd11b9fef2bb661acd43c5d25fab1d90385d58`  
		Last Modified: Tue, 01 Mar 2022 13:57:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b014685b5de9186ed5e06f1bbcc4b8b2560f44014202cab9ddac3dd9075492d7`  
		Last Modified: Tue, 01 Mar 2022 13:57:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec1397fd33e4fc48fc15096125e75716af7853b0775a83c633abe3fad3bfa22`  
		Last Modified: Tue, 01 Mar 2022 13:57:34 GMT  
		Size: 302.8 KB (302792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cede5ba0a53619def8b1430b72efe41af8a2305b96f4794148d98f64ffd1ff3`  
		Last Modified: Tue, 01 Mar 2022 13:57:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
