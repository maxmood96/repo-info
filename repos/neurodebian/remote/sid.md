## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:396c89536fe6db1bc27165b5b3b01c1c141024b20e94ed056ca001ee7d489199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:11f1d8a2c1ba5807309a84fe53239c15644decd7e0f952223fcfe8e28b9d40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d931e73790091e29816ecd8a3b3bd13e50c1b635e8ec66b670304f41e9377f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 91.4 KB (91417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:813cab0e7d8d6a6d32eb156bb2a98ba13135a9efdefa45445c299cff634bb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eddb8c244b0b5047058b014b003d153a1b272ae2e55f50361d6707a657d0ca`

```dockerfile
```

-	Layers:
	-	`sha256:c07968d16a78367e1d48530eb27283dfe91c39751a8b135ec9af329cb9dda337`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f70ccf1c4f8e34348cbd6dbdfdf30069e43ae372c6d6ae4183ee57c6cf6e7f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe90355c453a718b5f375561fdd4ffe5ee6d55f7254cf1b2b706984bfcd91d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37cfe9a0d72ee56ff9cfbd3d6f54367b57a516bedd5b30b0d1a598123957ab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3355433a01c656d9187644992eb02f399b926fd6998309ff3152bdd174664e0`

```dockerfile
```

-	Layers:
	-	`sha256:f01a69ba873a649d16109246e36645e9293f212711280454988268bed4add197`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:a6e34b9b3ef10febb3e68cb59e5d43a9cd4518aaaec42c9fb0eb764661ebac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356823f088987741ec801961eaf46491d407c63f5df550066164acb83a595dcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 91.7 KB (91657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a39472daab1f7ad10eddf0cd67f8453f4675bbd31ed229cb77f9a601729e442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5077173fa2b440d42065a12b5c4ecbf78be9444e400aa418924ffe9cdeb599`

```dockerfile
```

-	Layers:
	-	`sha256:b9520b672b857555a8f6a7d165f2b5323247148278f458a7278373f979f2088f`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json
