## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:2284e71395ebbe264bfb288fc422101f6c3e7feff66633f373f68ae621ec1783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:409c2332daa7272d31aa886e9658768f7ef8203669036c3a11c48852a8d06899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81109e92014c733ae52e6b4661be0aab21dfbffe6e1428e2b4ed57138ad3c7e7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:01 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edd9cb2b95dbf7f48618c8e86c46c24ebbd1e88faa80bb6299f17474bdd2b3d`  
		Last Modified: Fri, 18 Mar 2022 08:18:22 GMT  
		Size: 11.4 MB (11367941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb7a823070655e625d406d231cc6a2f192054cc327c4730783974f7e9c0a4`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7330b95115cc239fdebf118defcb0e3cf76bcabf611950715ce2cf8cbd7acd81`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89deb3ade5987120d2bba15db10e8be7a48a9fa3517fb6395fc5952e4bad04a2`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 307.5 KB (307473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be8b0b9c55260fa6b3d724c6f7075078c1f4b90a2fb916071bed9314952e804`  
		Last Modified: Fri, 18 Mar 2022 08:18:31 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
