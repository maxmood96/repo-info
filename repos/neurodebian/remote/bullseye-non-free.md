## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:61b49308851457103ff81b30d7cec84af48f84aac14f6ddd1735338df94c5d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:88ca621344463ce5620b179cfaeacb2109a6a1286e1af5c6552cb8065bd4c037
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b64e893ea7ed9a94aa49e8b1bed3684854cbec3f3389edf3b542348f7079f50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:09 GMT
ADD file:edfe2fd644e397f293f4634d48f0fbdadcbf9e5d3f226da6daa213811d4bfb90 in / 
# Tue, 31 Mar 2020 01:20:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 20:51:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:51:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Mar 2020 20:51:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Mar 2020 20:51:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:51:51 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ac0531d9afaea848836097ce37941ab7f0d2533a1b6c1cec0eefed4bb8d4d9cc`  
		Last Modified: Tue, 31 Mar 2020 01:25:55 GMT  
		Size: 51.9 MB (51922687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f290dd3e47701e6f8a4c9f05d2e16be47d91e88a574efcd7abceaf36ee89ab`  
		Last Modified: Tue, 31 Mar 2020 20:53:03 GMT  
		Size: 11.5 MB (11450465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acb0a847be059799a9d4feba0896feb33406f31d11eaac2bada8800195db583`  
		Last Modified: Tue, 31 Mar 2020 20:53:01 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9cd7cfd1937ab60bf7ef0554df0ec36b0ecc21fafe1888a1aa0634fd8bc057`  
		Last Modified: Tue, 31 Mar 2020 20:53:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532574d39117b74c2bdb2d4439e6d21824ba560ddae54b4ad64b620d79f68ace`  
		Last Modified: Tue, 31 Mar 2020 20:53:01 GMT  
		Size: 299.6 KB (299589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20144b2bb1eb1347d93e57c4f36b0428436320a80aa26679bee9ac68b8f525c2`  
		Last Modified: Tue, 31 Mar 2020 20:53:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
