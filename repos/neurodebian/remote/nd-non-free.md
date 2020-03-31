## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:423f33e72d6d99255d3a2af379c4c3e00f7eb39e0e85cdcc20a4734b52265663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5e5ef6cac2041b5002fe0efa030b6f57c4ca5c18ddb7e06a0603dc6f8d94c7d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63053938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda357f5c3a12e4b87032eb80f958cba6f10e814f0ba5bb4f5fb130ccfaed6a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:22:48 GMT
ADD file:7562f01f4040e4f21a40337301dd14e4377f3d101bd0919a96ae05bff37d7087 in / 
# Tue, 31 Mar 2020 01:22:48 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 20:52:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:52:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 31 Mar 2020 20:52:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 31 Mar 2020 20:52:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:52:16 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:616821eae326bcd1b2974181d172e5949f2c8c091398159b63b0f483913be88a`  
		Last Modified: Tue, 31 Mar 2020 01:28:20 GMT  
		Size: 51.9 MB (51949680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55635e40633f5914592aa8c03d8d7ee0d9508b150ecaf439e6fe4ace02aa663c`  
		Last Modified: Tue, 31 Mar 2020 20:53:14 GMT  
		Size: 10.8 MB (10802474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f135786996edabc414f63b80519e83790103c1037a26fb774ae55a1b3d3a914`  
		Last Modified: Tue, 31 Mar 2020 20:53:12 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b14cacd012663b2fefe11222c8bebfff233faa63ba17ad00a7989d737f5d64`  
		Last Modified: Tue, 31 Mar 2020 20:53:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0313736ebede4335ed0e6b27881ad34e4930177d8669b6cb0cd7ce768a92b1`  
		Last Modified: Tue, 31 Mar 2020 20:53:12 GMT  
		Size: 299.5 KB (299462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81aeef02e259c1d714a2a81c8c497e4596b4e7a8c043ccf9e61c8d39ab2e40f`  
		Last Modified: Tue, 31 Mar 2020 20:53:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
