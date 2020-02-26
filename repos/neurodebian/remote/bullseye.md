## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:e9af24eda42156cd0809ee652554b2e83a2870e906eb27d5b1d1af12f5a1e8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:72710749a4d60bad87a2ce281307ab82138e6d27e4ee2608bf61cc59f00aa1ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62918247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffaf93441da86edae7b338ddbfe989b2cd02e315a5dd08c6d17d0ed4ff28269`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:36:28 GMT
ADD file:7d01effeba890adb1756ba0a76c42c1dde5a189003943fbf4cb9fae0c0e1a046 in / 
# Wed, 26 Feb 2020 00:36:28 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:25:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:25:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Feb 2020 06:25:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Feb 2020 06:25:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a4501da464e996edc2ef85325afe9881a58061a9a35b142ca7f0ba598553e49`  
		Last Modified: Wed, 26 Feb 2020 00:43:35 GMT  
		Size: 51.9 MB (51852739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a550e5eff384596c11b67936cd85e2b18bac237b68bd2060f5d35edaa4065f`  
		Last Modified: Wed, 26 Feb 2020 06:27:13 GMT  
		Size: 10.8 MB (10764418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e46841b2950d9c62854b634919f0262fc93babeebe461eb58c64bd7f6d440a6`  
		Last Modified: Wed, 26 Feb 2020 06:27:11 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7fcdb4bfd8ff03d7fb0ac7559473f437f9e6e06960409708487b8ce3b4e6bf`  
		Last Modified: Wed, 26 Feb 2020 06:27:11 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3219c7326f610e58a6a6f6c8b15dd7647406ea21c86b195aaf695a0af8e27b95`  
		Last Modified: Wed, 26 Feb 2020 06:27:11 GMT  
		Size: 299.1 KB (299090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
