## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:150bf0efbc0cf3e71c4e917e1365f4ce12f068b52f78b4b3ad7edf35b51bac84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:2302018712146863aeb4690550a5b76df8b7df13e0d802be71a0c3c38149a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec708323e8e211beffa0a80ae7bba5f384b434ce88123b60733a0d195d8aa7b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e5a600b42af7e7249a38577cc844cd06b82d1f22fca446507bc4d97304e37`  
		Last Modified: Tue, 30 Dec 2025 00:03:22 GMT  
		Size: 11.6 MB (11625089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24bf27c0bb0ed449a81b5fa6ada1e384d2e5ab45f9922c801299bb91e5dab52`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e586810401da99692985a5491071e4faf2cbeba2c773b81a6c74603b1ef3e30d`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe4dcbbac465ccc98a30e7771909d8458a9f36baedec710f84603defa1dcba`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 90.4 KB (90408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f519e2e0c5660ae6c3b23a247879ae3da45a30261b90d6a9e855c44ab69afa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf20aec7ddfa5fede50a25e0ed3e08a788b1e122a1f045868785e829dd18b35`

```dockerfile
```

-	Layers:
	-	`sha256:5a0737d7a8f7467ed51fc907ab110086336b2a8248f44a46f1cf3e860d5b3651`  
		Last Modified: Tue, 30 Dec 2025 02:08:39 GMT  
		Size: 3.6 MB (3592069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3fc4fd325b4e974cb70b4248875c0c5cd5f6d01a0aa49b27aeda7b7ea9fa01`  
		Last Modified: Tue, 30 Dec 2025 02:08:40 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7cb33f542c2b2416b8360d80bf270f017394a8248f5547bd25b910d362907e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d523ae26b69c0e69f59c722a906ef5e749bc1b0072a349d4b47e66752980ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c77bf93408787969c8c3f6ff7213d99a7e697e69620cca332ac58446528bf`  
		Last Modified: Tue, 30 Dec 2025 00:03:43 GMT  
		Size: 11.3 MB (11283854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa76c7561f8431bcf2d9458d0b5122c83188cb1a0af66ba63739670f119ad8`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f90c9596551e2e36dca68165bdffea5d2e3885d8c814d8ec39b6430e18051a`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891a2507db7acd33db08d268da2d5cfe43517b88b3c5e4d64e7746d884a2120`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 91.1 KB (91115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:677e960c2528d3f9423b79824ad6bd592c57b82a587b2e13c10fe717f1ced255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec4e91d533b3762f44007169dfd298ae15029e6c51d8049c5674a2410e24c89`

```dockerfile
```

-	Layers:
	-	`sha256:bbd84bbc74533abe8bf8740104e0d06c186ae3cff091c08be59b46b536a3e3ec`  
		Last Modified: Tue, 30 Dec 2025 02:08:44 GMT  
		Size: 3.6 MB (3592945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39f6fcbfd1dc80794642dc576dfd48079c6de50372df3ff1ac44eef02c17cc3`  
		Last Modified: Tue, 30 Dec 2025 02:08:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:ed17bf7744b05e17a7f5a07512b499f7853d80ca2634d1b3091f724ec12704c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a7e442293c27bab1441b206d263cbbfda95db72021a246e34633483d87277`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cee8645950fcb2cac8e786ded94810e24e89ade2e4f5cc4099b37f01809d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:12 GMT  
		Size: 11.8 MB (11752135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16c5bf742f0f200c67b5041f2cf3e97f655ef571b984e5b607960988763c66`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec3e51522085c44202103858e4b4bc149caf3ac8be3196028e5327cc90b577e`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a58fde9f6b48ef00bb0ab006f68aaa17d9c356d37254ac44110fe0f3dadc452`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 90.9 KB (90913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ade3efb3c881d0f2aebde1a8dfd977b7cec6e59eadd851d32e96d5442cdd4c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31d7558920461a59e82693d3c70a6a3ec175dbf6017f477e182186218a2197`

```dockerfile
```

-	Layers:
	-	`sha256:16859a3d98038419a32fbc0eb7b4a65dfc2adab665a924d9bb3ff4e6dfb608c8`  
		Last Modified: Tue, 09 Dec 2025 02:08:11 GMT  
		Size: 3.6 MB (3583531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104b1ce751d490df8412608415756e6158e3a99cfc6d9d66a088c869af428201`  
		Last Modified: Tue, 09 Dec 2025 02:08:12 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
