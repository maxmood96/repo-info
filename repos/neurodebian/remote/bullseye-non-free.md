## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:11df13597ffbe35db169e2fac0a9bd031aa59645d797b6050e49ac01bf302013
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1db077bbc68cb8e74d68337502ca5c945f9c4f29e54222497225c9a11522b7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64980317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da8775502d1ecdd552831a705c1511e96376940077b10acc2bef3b6f254ec08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a2735bf9c1d4bc089df455dbeb212a85e9ff8f62dba795cac9e0cb71b25440`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 11.1 MB (11103381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2009f8c4e7990d64bda16e2a88a942f6ad7abc18d001232af0f0e4ac75d11785`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d973476ba736efb870298bff194f6ec7b1910fbfca24bd42ae9fc248e14b76d`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1269e6c05a31487846e97d3fbddbab8a598dda1cff5d64019231fb033d5dd18d`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 101.4 KB (101382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9b48026a9acf65c6b5593861cda173bbef66f37ca7acd2538c5c4db0378fbc`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bc63fbc70cecc62ff79f5101f38770d7c2d8da2de89c429f1741be8dcca4330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6120cf84591674a0e24db469c206468b73c1ce06886956406513d7722883b42`

```dockerfile
```

-	Layers:
	-	`sha256:a93a42cb76e96f599d0d5e3b798d78d20bda37146860c0320ee4e286a975a0dc`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 4.4 MB (4367954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2792f4b3c4a7656e05049f2af8b1a7f7783a1fcdbdc4d0d1818e9e445a2ba5`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7a636efaee6f21ebc76c6152ee8131206ff42801cf390de4c35d021b318d0e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63470935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe9b0400c0528d5e271b46d1468f575d2b78e60e209c31896f199e614505d14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:48:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:48:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:48:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e39bc6bc1ed41eb506aced6924d9d25ecf1a3e84e238e489d672651e99758f`  
		Last Modified: Wed, 24 Jun 2026 01:48:28 GMT  
		Size: 11.1 MB (11109917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4e87b399a6f38e8922bd55268f39d4624b38d7a87893932b9735adfa080f4`  
		Last Modified: Wed, 24 Jun 2026 01:48:27 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e239581ad7a245fc0ef7c5853326c75a8b67c911cd99d2301d0efc3e185a7`  
		Last Modified: Wed, 24 Jun 2026 01:48:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f72ce7a51d3a2d4d295d158afc8b8bd75071fddd0dc59210bf54ab7ae1e8e`  
		Last Modified: Wed, 24 Jun 2026 01:48:27 GMT  
		Size: 101.3 KB (101251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60756fd7175aa79a5bee9a36489e37055393bd362d903bd7de23b7257f7f57`  
		Last Modified: Wed, 24 Jun 2026 01:48:28 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b5c9b3c82a84c1a1dc6ff55123a42c82e1cf63d65e25397bff3ea0df61f1d40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e284f5c9621e66c31f20599a0f25ef384b39e1c39726d57fc4fd502aab47040f`

```dockerfile
```

-	Layers:
	-	`sha256:d14f341c977a733e9ba62f54755a75bc9d0befc983f2d207186e790c6854d433`  
		Last Modified: Wed, 24 Jun 2026 01:48:28 GMT  
		Size: 4.4 MB (4367561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da97c88180394054a2a94f92c089ad6bc62f9e532d4c8fc4a8b26407f0c80c6c`  
		Last Modified: Wed, 24 Jun 2026 01:48:27 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:59276fdf68cdf6c39f9f2b48adea89d87a69b799a451e0654695a04f8cc2d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66319059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f05541b2fe796f61d1f458804828998fab7f060d538af08930063aa5f789798`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:508ffc251196056212d40e318af0b7425af79fd3069a3f9ab15fd6220917ec75`  
		Last Modified: Wed, 24 Jun 2026 00:28:09 GMT  
		Size: 54.7 MB (54712884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1003e73ff718fdd0ac720e6b2b133d9905cba574dc287b25be82e4ff3db864b2`  
		Last Modified: Wed, 24 Jun 2026 01:45:00 GMT  
		Size: 11.5 MB (11502355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b007ad9eb044b5b1ec8d7f05615b58da2a62b453fd9cf797bb64b34839edadc9`  
		Last Modified: Wed, 24 Jun 2026 01:45:00 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89546f6290ccf1e1f417f74f6c9355b14df28e67c1357fe5ade3f8a14355070`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb4c67ad93bdabd1ab0abcb0c7f29461c23f753e1c83e7e190845bfd5b7a68f`  
		Last Modified: Wed, 24 Jun 2026 01:45:00 GMT  
		Size: 101.3 KB (101275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f4c5d6b97b2aec70163c3b8b6c8655e50de53e907aee92fad6126127cac3fe`  
		Last Modified: Wed, 24 Jun 2026 01:45:01 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5d0b50f8fbb42f876d06f7b914bbeaf551f110de946b00c9ab62be1e135634d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24869a05642126e1fd113e8a49c7c57b02a8779b4e52cc1df48985260eb767e`

```dockerfile
```

-	Layers:
	-	`sha256:d1980be7a551dc07a55478fd74893111004bf34dd26ef817a9137a20bc292842`  
		Last Modified: Wed, 24 Jun 2026 01:45:00 GMT  
		Size: 4.4 MB (4364473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65207eb267d41599bbb9cacee1d8500e39c1952990aa0c30ca9ae57a275db454`  
		Last Modified: Wed, 24 Jun 2026 01:45:00 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
