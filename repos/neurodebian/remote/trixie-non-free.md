## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:aa04d182b44211caa6526f9e38414339cf44856e56c2f72981d4b74054e5b64f
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

### `neurodebian:trixie-non-free` - unknown; unknown

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

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae227e01cf2cf4676e0dad06a85f444edf7110c3308e37dca9ab2a8a0ef9b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59339204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66aec19c986d35008e382bc76893b6503d2a27ce5bbfda0ec9285be568b9e2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
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
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba27a9cd424832252c3bc77be2ceaf9ec1bfa8b7d89b6d274efafd9c44229fa`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a7a5d1d9aa5d38f7b816188f0bbb15d7b8afdddeb3c696a0cbd7475cb4fa9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c10ab083598a842ccbc3dcb4c849e36d85315aec9293da11de467620a3c21`

```dockerfile
```

-	Layers:
	-	`sha256:2f0eb7be74e008400584761b42470fbf19c4facfec49d94fab3b40dd02da6921`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 3.6 MB (3561620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad58bd9e9493475fe159f6f233256b3f58f8f9bea08a050d53f7ba19cb479e5a`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

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

### `neurodebian:trixie-non-free` - unknown; unknown

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
