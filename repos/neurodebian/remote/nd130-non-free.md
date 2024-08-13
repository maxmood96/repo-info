## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:c2c162da43785442e6e6a09f487d01de7be7123b324562732db9aa30c2786799
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4599eb89d641c78f06330b5fc19e48023605af17a797465478d0b8be428f2ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59175044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d284eeb79e113b6e02d6ee672a6aa3520a83b5fa898a4bd2cb533ae8325e700`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
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
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce474f48ccd105d0617c09fe857f117a99e1e29a996b4320ba2b7de1979f59bb`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 6.2 MB (6240869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd3a110ef4119373f628e087c16dbbb4bd28f06220d7389a705093d2b18012`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61497ddf2d4bb6a7077bc1d8b6a1c5424cc821e644b2c69433d9ffcb21547f7a`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a97170d3249a59394f70016aa80f45c6862354794bf973c6d159f12d2287cd`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 90.6 KB (90571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0706b3fa22fc07de6182303c357248f9a97b3e27b5e9035a4589d29413bda884`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:19841391167fc5f99fa73a705a1dad677fb273bf4bc43c9b9e4e22ef270c747a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a4734cebb22caa416a176e19399fcd71abfb92b38d0fbfbf918d39076f45a7`

```dockerfile
```

-	Layers:
	-	`sha256:864026c809e53aff40d228261d22b559ec0c43cd4a4acf3bd4461dc7344333df`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 3.6 MB (3560361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82d259378640a9dbf9d00c545a02c4b92dc986e42188be54ef7e78503b091da`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 15.5 KB (15476 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e0fccdebbb4c3e1a4c51702d3bcfc7b8ef28c1fdba127fb501398b54b9d97be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078b3ce0bc1dd7b36af04ddc5cad250a918b6391f24707db77d6c92c9b0d3553`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
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
	-	`sha256:dab7094a272c5f55af989aed29e9331e322fde90bcc6e6310d1f9cecf4f1bcd3`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7bc75943597ccf63423e01147b4cd0be252e263339ae1466d4530d5bf245fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311ff9447377aa2faf72ae51c9a8a6cdba678c8bf81924249c2ca218cae908a4`

```dockerfile
```

-	Layers:
	-	`sha256:60ef82002dc4188c276c967733bf3f7dfe6ed10afb436761e28b05f01c47748d`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 3.6 MB (3561403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b732592ee34b5f02ad33eed797d157f745cb26004c31735bb1a7c10c88fb8e63`  
		Last Modified: Tue, 13 Aug 2024 07:41:47 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:549b82d1b0e5cd9c2ce9a9baf648b680a14c782c8f611235c31aca17cd419869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60436291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1bc6a4d38957fdfd69ea50f09f3ea43d9787658cdca31544d4d0141f6606cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
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
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09f0177e0d45ab1a69528ede56e30ac3e58bde63bf62f2c1bf78711aec1b92e`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 6.6 MB (6565895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a53b8f72283931b8920c07e7c2c39098475ff9658352fde012ed25e5ad75471`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a7d0317b5178d23dcf6d127c9d0af7c859e20d4bf21fb593b37a0621ab74a2`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.5 KB (90485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faf6db1b44baed2d5b9bb7695613c6daf5549c5f18f80473d873e346ffb47b7`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:969eb3d41b3528ee2d9433a5a63c75104060be0657ff8b63cacb1e505c8c89ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f8c1efe704d408b169c6fcfa592a13d6a9472f0e7b2e27b298560a24ff6281`

```dockerfile
```

-	Layers:
	-	`sha256:30e99b0a09798c571353fbc370f6f4dc9cec56ea7091480e8cad466438192439`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.6 MB (3557454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d0c3b412bb34261435220faf454f44ac6f6b3120cf906986b821f2d2229cb`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
