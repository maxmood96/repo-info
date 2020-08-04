## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:e76b782c2b8e4bff041279cddfc42f84ecfb6308e0904a9f19dbac8337aeed66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:65c98c36cb3c004c0a6aeaf21804e6248efab014c6410699b23497b0f4093589
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63229697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b0909c2bf8fad4c0b23a3b1b24ad0982b20148dd81a722faf8fe248cfe95f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:00 GMT
ADD file:91c81aa3735ab11fcf7db3eb2dc51c94759276e7d3657f0fe81829c133f7c8dc in / 
# Tue, 04 Aug 2020 15:42:00 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:07:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:07:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Aug 2020 23:07:37 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Aug 2020 23:07:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:07:47 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:a7bda3d6de74128f57cc726f2172127887e010c6a291320273a9c9eb8ad29209`  
		Last Modified: Tue, 04 Aug 2020 15:48:28 GMT  
		Size: 51.8 MB (51838182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51be9b0aa50d9f631bddd5aa4fdb0aaaad7d05d3004a41d7ea611faa0bb85b9d`  
		Last Modified: Tue, 04 Aug 2020 23:08:55 GMT  
		Size: 11.1 MB (11090256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff451202d63fe992f03306eff5c1a6f6a9c41fda9e99f984a53ee8d8231f7b5`  
		Last Modified: Tue, 04 Aug 2020 23:08:53 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140f40caebcaec842b6526688d2bc1df15328b088caf674235c99ded63111d6b`  
		Last Modified: Tue, 04 Aug 2020 23:08:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a6dacdf2501a3fa421ac920d90300939ee9c4e1b65e5c78a2c6ae6df41fee8`  
		Last Modified: Tue, 04 Aug 2020 23:08:53 GMT  
		Size: 298.9 KB (298933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0395b94a83af79f949e21362dce0d0670cf56ba0c36e94753b0e50476007f88`  
		Last Modified: Tue, 04 Aug 2020 23:08:58 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
