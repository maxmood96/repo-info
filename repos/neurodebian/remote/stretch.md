## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:0867d9a73a12008748c5e5006eb34ee0114c45eb2f48a153c57b273022a15923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:e0037e8f72180a2656fe93b276b2b2151c54e65444beb1278df8ed5fdc2949a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52230350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5885fdcf2d75a5e5026ee9155c51558eb7eb8c9dd69e97c6c86189975996713`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:06:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:06:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Aug 2020 23:06:50 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Aug 2020 23:06:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fdc5ab617fbd9aa250424e00a6e162c19e20b26e074bca1c0a3a63e2cb0087`  
		Last Modified: Tue, 04 Aug 2020 23:08:37 GMT  
		Size: 6.6 MB (6568124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b26956b61afb1cd292657cd3c6ebf3c1e4feb5cd0144dc9c0dcd09182e68680`  
		Last Modified: Tue, 04 Aug 2020 23:08:36 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d301889fb0f7e5de1725a9495d9e373821c7593f21fe2cf091d620b61428519f`  
		Last Modified: Tue, 04 Aug 2020 23:08:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e56662f02522267ec0d88b0f332190960f5c1617f23e001ac1412f6fc1e67ea`  
		Last Modified: Tue, 04 Aug 2020 23:08:36 GMT  
		Size: 292.1 KB (292124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
