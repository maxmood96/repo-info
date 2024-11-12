## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:81e8dd0a9e0b26661c24f769c2b9f490280388e12cd8b34a10892163f013c33c
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
$ docker pull neurodebian@sha256:fefe8fa828fed725f0862bb1e17640968cdbb6217136386f9afa4c217dcaba03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0886cde28c0abe347d5b9297675537483f8b89adfa3614f1f7b3b6d24b3b6362`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12105003f4e642f6b650661aac893181b1d5a223522c4ea9707f4c49c1c21146`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.3 MB (6309012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019d15d3ab6709e952717fee2030801d3a2e7b48627e0495968e6a3dddc82f7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5031ae0507f16d4327df45397b64a44524f00f43ce0a3c4b92d1841d4d4894`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb0be616ed4754fd8aaae15a80e494a5b232e34566aa75406ff523bfaa076b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.4 KB (91413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c93fc498acc8bd76e7c80e33b3fc67fe2b87d972f2a10e421cc3f9c28b1c75`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2777c05f8a9537fbd757ed82f1648ad91528d8a7b1d708eea6dea994aecc9129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a94faceb0ba666bfbb25c7f7d11c1da2069fb19c2835549905ecae4eee59b39`

```dockerfile
```

-	Layers:
	-	`sha256:c57d732a8ed4c5dbaadccf163569842c875c0401b711a18a1bc6cd10670536c3`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3568329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fbd41c2b70b3c5115f92fcb0c70f179193c0b3d101a2e9b6a17c436584ae60`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2124810c59c2070507d08e02b39e70ec6c559ef9db627160ac466ad8e024b528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60052919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4cf3027ffd02a3b90835d95098378de393c5f8c1f0fceed499f13fa28e7a9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23bf76a989ff5e6f76f330379b3e989793687ed133de3ac5410064a9c771a9`  
		Last Modified: Tue, 12 Nov 2024 13:33:25 GMT  
		Size: 6.3 MB (6288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120c2a86c21de9f38d4094726b8a00af5f3789a15c63dc031095f5280692244`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79269e860b98db1f347c42152747f764202ed57267f8615d3fce3fb871305cb9`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82a537cb0fa455330670123eb470dd2cc9577f0075c1e0248d0d011a21835`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 92.2 KB (92189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3fee26e316a8996c2e950f1ad5e0b6fe7c4021ecf5dd1d81ea3cbf9cf28ec`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e988c7c55ce2dec9c07a22613faae849c9174ff303d408c0da6e69dcb31b4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f11d4d0641ffbe565e4c011a9c392802ea9a92d0c210137a8730c01fc6ba4b`

```dockerfile
```

-	Layers:
	-	`sha256:4fa1271a0a18eebf089f507b19592bdb596a03efa9809236fd734eed8add7f39`  
		Last Modified: Tue, 12 Nov 2024 13:33:55 GMT  
		Size: 3.6 MB (3573847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784bc588fdda505cd76103136b7bb9470a0ddc64a3ea6d7b531cd79f5bea34fa`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:534dce1a3347a1871c4179745706a330c6b415fa9fd8eda2f32b41251d970ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60825149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a57bbdf189d2c4ec8efaa71b304424be58a2d1e58cd22074929fe6c196ca00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0ffbd19363ce5a9fc6e9f7187c63b2555049a39825812a94c390e6d270d52`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 6.6 MB (6635929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172f7e731b0de0a50742f1afcbacaebdf9c053a18fe4aa63b34f108143ce784f`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4148e81020142fc4c880700a5d8912a5ba1357a3e86a38dbfdf1421011cfa`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cebeba3a77966586091e95bab2b4a598231d8c300e6551fd937ddbd75a7d9b`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 91.7 KB (91650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80068347cef0c5223d5f71e7dc0d64b732ec48e36d6055338c7f363bc46f3a23`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50deb3e18194c5d466b1b6686d20d650631d5abb9211cc67f1275a9f18c945dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc10c3e19ac99eb4c385e5f1d514019783499f18773f359e61963a5cf47327`

```dockerfile
```

-	Layers:
	-	`sha256:5827057745618179658ddb32068a4bb10e525186aed20b21cd4ce612b5e0268e`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 3.6 MB (3565563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd822b3c8e11b3af5d8111e0582dee4147705a9e8c8e9f967578b5d00b5d286`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
