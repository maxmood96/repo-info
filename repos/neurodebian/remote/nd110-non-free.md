## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:b1b981ecb89928db19bcbdc993aec4d1c3401b98137b8cd41f5b89e330dc079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:640e3df9e4534d11a9a3ddb222692cbf072d8a3f5824aa24a701299db25035b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63255795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2fc6426dc97948ce484f6edd20201687eeb6e7a4cedf32fc36aacd6c8cfcbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:30:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 10 Sep 2020 12:30:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 10 Sep 2020 12:30:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:30:48 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097e1f2a4104cccb08e4ebb1070cb616cc8236ceb3bef30386232738027c8d1`  
		Last Modified: Thu, 10 Sep 2020 12:32:14 GMT  
		Size: 11.0 MB (11048112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df42e5e80b44094569cd2182335dd6836096e2b59a73bbc60f2a8954a839076d`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ea32ef57970562a16018ae9eb5ca81d1ae43c4b53dc1070d3fbc96b2be4c3`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a541b17e9df3c1774a284d312af41f23d684cbe13dc3c10c111e93cab815d73`  
		Last Modified: Thu, 10 Sep 2020 12:32:12 GMT  
		Size: 298.8 KB (298777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c8493a6fba4e132eddeabb99fb6827fbe71e39be45fa65694c2e77f381144`  
		Last Modified: Thu, 10 Sep 2020 12:32:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
