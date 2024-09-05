## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:e653be36a28033fe24bfdc6d7974b400d7b167573990202acfa3066708ef65af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:a546d8ed9ffe1cf9bfaa5f41e6990494d4161f32f71c2912d6ff8a323fd891d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf42119ac53bfcf848e5c69c4b517bd04ed962dfe730d51ec7ae87855959ee1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4d57c723071fab9db60a4db2147e17aa66dc83d2eb2eaa6d6579487ee0405`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 6.2 MB (6245441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5e26a0664131c25e2eec527fbcf80640e1dc3a81b7a9f1070f1b76dbfc976`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f414c1a656a41c98a86a7e5ab714d0c744b0d0e057887321cef5c818745e553`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 91.1 KB (91108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90095457c2c3217e470366efd9f555dc4106a4f43a068b16fda1a15a50cfe397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1dd60de3b0104390f365e269fc3dc0c0f82664e1ce82ddb3bc0504bdf434f0`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3bd20bfbe30fc6feb1760c58ab8f8348ba270666600d2970d9d6f00bf0e47`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 3.5 MB (3533284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f3317280d884cdafb352868dd83567052bbb80f73737cf10ca00dbbff1c8a0`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4902d30efab700e1e0e7523ad44858bd58a9039c36ac78d7c66275ab9b3cee2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59480755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daccafc1f00787667713fbdf34071b12f94780c42ed253bb68afc7b749d22869`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:89a4a17aa7e58a5b71aa52e99a139b5b58f4b64bb4d7f6232dc569fccfc738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ebefda3efecdb73baeba3204318196ebce232572ff0bc926c70b78d5354c0`

```dockerfile
```

-	Layers:
	-	`sha256:844f178c4ab0992a80f84dca8dbb6ce33a4411dc7b869065ab23976c51f13e50`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 3.6 MB (3561367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd21adf8224349c32874c3825d25d8472c8564d30be72e731e594e359c63b3`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:8c6f454fc37a587a37624240f1acd6d8dbf71d5c92ac97f493552153d17fa9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9f707f5d52c73d7b0994b2358dbf7b4d9b644478517495c838e2051b32596c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1333c78cbfd9aa52271e569479d48c943ad9147e43a75caf4a8cae6c51a`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 6.6 MB (6572980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6b4321ab18ed6a12a8a49996eb7eaf67fc9fc9db20ba96a3214a3d80b865c8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8051b1ddfe08bc83e829b01b93c1f7dfd61e675799ab4cf86d902006a595637`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc98573a9f3b01e547fed3a2007311d20d901fb130257ed478663d1c22c1dea`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 91.0 KB (91023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff488a69e1a4da2f2c98f8a1dbc2c21aff9925cd26db0669f340f7dcbb8ce9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301b4be982550abdc5bdbae672d097cd83368244bba2b73beae3c0a031a62287`

```dockerfile
```

-	Layers:
	-	`sha256:9659a39acdf1d37656ff78a42feb51c0465863f64de1cdd905cf0b9ae53cd6ab`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 3.5 MB (3530382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303a1eb21faa30f54762d880b213c9b9a2fa67fbd348e157b296527b9310f4b8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json
