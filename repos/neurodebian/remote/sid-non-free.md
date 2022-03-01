## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:c3e9d01fb21762ca98df8cf665711114715e1ea5680276371829801f9c87d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e66e8e01217036c3db84ad75e03b6dc7ec91dc6d510bc993362853e443085fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67663908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755e4fbf33c6af03fb6ec59c46bf28ecf79c5b32bd0db2de40542d258817cf94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:59 GMT
ADD file:62b7e1deca7e12cf507f0b06446a94bfbaff1760c4333fb3f8f92392b57d50b9 in / 
# Tue, 01 Mar 2022 02:15:00 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:56:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:56:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 01 Mar 2022 13:56:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 01 Mar 2022 13:56:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:56:25 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:740da9cc2bb63315fd21f4469ac9e44b2f6efbfd32f98a83c863fa9c1a145714`  
		Last Modified: Tue, 01 Mar 2022 02:21:38 GMT  
		Size: 56.0 MB (55974168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678902d65f6a75471be24a42828e5a6838dc1d69d1b8bcdd7f5bc7435821880b`  
		Last Modified: Tue, 01 Mar 2022 13:58:22 GMT  
		Size: 11.4 MB (11376471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff84077fe4b4ae25ef3735f30bbd3b41276c75f6835b964d5a7c24253a47e4c`  
		Last Modified: Tue, 01 Mar 2022 13:58:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b27fca2b6f3e2b7901e832aa563c25d52a7e78d098dbcd0634a5071a4f4c13`  
		Last Modified: Tue, 01 Mar 2022 13:58:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fb9a5ceebdd1cb4e54e8241aabc7b4c59169574d85aa88ba12e189677576c0`  
		Last Modified: Tue, 01 Mar 2022 13:58:20 GMT  
		Size: 310.9 KB (310948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05281224f36b8a9dc38b14ef5c71476caa5c6298472e5cdc2eb5b3e384ea8146`  
		Last Modified: Tue, 01 Mar 2022 13:58:32 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
