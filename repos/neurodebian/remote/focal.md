## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:bccb027a7ee6016c0a98560e51caf98f68f947b948222c7bbcf90884f08a2f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:33321bd67f5c4092724b3cd7c84390a44effe62f516fa528cf835068466ea750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712d68e6912e2dadede90156365035ed83ba26b955c56a9b6743bb689ebb8d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930f573b2289c54f50a7b09f6d9445bd27f0cb1a48348833d5e6e0986d46da3f`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 5.4 MB (5360160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56884c4edd0cbca3617ec0ab7f4eb2f2db8594b9b0cac16d907a38c0fc6c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:10 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dfcba298667a425ac0464a6b4a731a25e47be2f31f0a80c882d1cca00ebebe`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779280839ac6c6073401d79c852c9d696e3eace1c131d11108e53c493df947ab`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 105.2 KB (105242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47328a35876e2dd7e853351f6352f66a75141ba91a935a0c3cbc331e91ef99d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc66bf80d0b2dda8634ee73d7770e19baf3a5feea2a59971ada23eb86492d478`

```dockerfile
```

-	Layers:
	-	`sha256:d332d6862683e5d1b3ab2a9b95808810e88d2ff242476a6404c0dba1e73252f4`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09899de5c9a6030d4c0a7373ef9c207b4660e941a72ad0126b2268b979db356`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d037a60f85e3420771a09c5095426ed874d09300fbede4cb3573387b012275cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685e5e5da9030956235506036387fc62634485c42ed3aca5b1ae6bceba9b54a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f8f3f5dcdbb8d4a376f39a0a97981fabb7e6ba9a91bb9dab61851e0cfeb3aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfc5c521f200740f1d1f0487bdb2674953bdd1ee81f47919ed971ca0ad86e5`

```dockerfile
```

-	Layers:
	-	`sha256:29772dc3da77b6599d1cbf04610642086bf317e3c95fe67f41ac60c212428c71`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53c8b58100f31c59ec8233e0b9ba2b19ba33bc61cb1ea4e2294612be841cb1`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json
