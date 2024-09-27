## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:e5c3a6f1dee07add5b53008fa63555b3e87c50ef0cbcabfb8fe7e811a184c19f
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
$ docker pull neurodebian@sha256:8a704ab2a66bedd6d545216d003cd9c9ecf32438627d95f7c047de9514cc09ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec7d8e42f5d698d453c52c0e3c5b95182ebe92ce4f3ff0d418bc8ee51cd21e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
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
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f4127dbb6bd4852281e126959ee094bd68ff8be42d017e6a181f73ead3bb`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 6.2 MB (6241747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955f83e1df90f8ef2d13b780bebc31587035c53b36c3b3725fdf8080c96a672`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab66138a8cc3cda808f2ce60f4397ab57039ee7ec2d135069398bd4cb72b73c`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3975fb056504c89c026f526d8570509d6e32ba72d8a4328e7357324341d27d`  
		Last Modified: Thu, 05 Sep 2024 12:37:06 GMT  
		Size: 91.7 KB (91726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6a231b4ae5e9400a3674313b29fa6bb199e56c37c44a7604322ec1dba65dc`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e548e1427eb6fc2d9a7a8feee437a55ff3ead5c3e8380688294479911ddce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05445c5a5d254af676048b62bd4c259bac7cf7ee009c6a869ecd4663da883c6`

```dockerfile
```

-	Layers:
	-	`sha256:97b0afd3517a47d8760e79a48c134bbf27216a34c50cfdcf9f69ca816e61b898`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 3.5 MB (3534362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586a8f30275c37115efb6b53ccb770a331afdf2710b998e8c032b26fb202355`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 15.8 KB (15754 bytes)  
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
