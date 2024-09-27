## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:ac61648e2563a3882383fad081f7de6996fe8f0fa8f9627a7e6bb0ba22288aa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b1f199d03815d48bab11ecaeeacd81e4b2ac39a65aec462dfe763fb7529d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2893f89434279438492df27d6533582a320166e62af2248cf9c6b82914766bad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b19379603d098a671eb23697522873f6e76947ab42375d6822c5b0a4b6e809`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 6.3 MB (6280319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0c24d6a8e14e4685405a8aaf43a7ab30aa29e0e1f283aa98a3d7449868222`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b7a35dec8f5dd32abe5be6043a56585b31eede2c1645904e76cc3a0482af1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57f109b0de41f938f7878759736faec767e84dac89736dbe1be92533a9acae`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 91.2 KB (91225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e14b1c01ac31d1c91fa43ae686e8efeb1145d926c79601a652e7726aae0434b`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15c88b06753416b8a2d15c8ec809ecbdb6754fdf950e7164e5fecc310c199b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92db2beeb0a5cd44fee711408904a5286a853e7f5a750d1ad67c91a5b7482a`

```dockerfile
```

-	Layers:
	-	`sha256:413a52dce277246c096155463956e28af6833eaec6061b111fe35a78cd5126dc`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 3.5 MB (3542893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b06258c0c750ae4d23c85317f3cf98f715296d195230122d9ca927b48c27b20`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de9deb09a9c4a574733d8bf0ee9a8435ca602569681432e0e590c0293bd56639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59972303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd450a6e5b8e10e76c6e84376a6dabc34200b6d18baa5cf78ed1fe5c5eb2ea4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcc1f5af84d08060d7baeab3587692d4e1469721eaf97086e62e8a08e46bffe`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c889b01f93a511698d8f75dec67873b2853e860e6b4fe77a705985d114ee6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75670270a37805095bebb659f19bb51c4a240cc626b2d8de23d774dac2059c63`

```dockerfile
```

-	Layers:
	-	`sha256:3d01e9874db9175f10aac3e72aa9bbdb68bc9c22142cafda74af046e7cc9999b`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 3.5 MB (3543935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11aab390c169d17bca4c29d127707bcd1072e69e4adf4beabeea95ad9335d9b6`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:610d5a9fef431c9ba267348b518a43342679baf184d01ae3eb14666c2fc7d82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93978382e36acf60763014fe3bc88c467988d32325425aa648e2f8ff7bc56eca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545000064ec8779f4364fc92c0c7f98105d8982df43953655f08d4136f0e059b`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 6.6 MB (6602251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b55a0ccc129180a73ace1423e5308abbb3f503a80e321fcdae582bcf6b65cd8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03864c9590de88a98994e47c33acbd627c63c0f22b16caa991fa0d1b5f19e0af`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66e8b891d253efd6cd929a90458ed0cd16376b0b3103ede91076cf1103e725`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 91.1 KB (91119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36db8fa03bfe1f6530a046c2ec1ac031c176b6bd18cb0c66c4fd002c6e47509d`  
		Last Modified: Fri, 27 Sep 2024 09:04:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2211dc7a785298dbf7d13565928c5611cd0a036d5582f40f6ce83bc822c5dd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5812a43efc0046dcba6e30c345df85cb1f3ff2eee19c2bab712b3796cef8d678`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c2998bceeff2c57dec6d686342a5fb51826e29f47d9118e161c0512cf2793`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 3.5 MB (3539984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c98fbc9db7ddf44a5051ac50bf1efac038624ab56321f3e8bb393c605105d8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
