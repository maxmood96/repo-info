## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:a78a1c95462db7bf414f96ce328616fe968aac57b876af3362c3e4b47cdb81f1
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
$ docker pull neurodebian@sha256:dc2ee078717e5cd6782de72121bcc9936ef63cb0981ca8e921754737a77980e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94ef9a8ab87a336dec4a29f001d654de0e935525f16a071a00515579aff5be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7de7481f3bac1a3622e0eed2ca47e8f02312431429159b58502dfc6e1b23d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bcddfe5efc17cf322b5dd0859093bb6b3567c32ae516fe9b443b80a0541765`

```dockerfile
```

-	Layers:
	-	`sha256:70ad6f08346ad337d0f9e32f7ec11b22ad0d818d1df8a6aee0a4052c1cd75b1d`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:17fe10b8e293faa659d945422ff3aaf4c7e6e1f387d707d314802beb80b71a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d39b737a8ff196e533cfc0ffb9a1412e43594be8673e8c0da6c05751f91ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c77a0b2714832915027f323e1b1215a7ec8179d2324362662d8283e9cad88fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7509c00ee24dafaacefc91ed80721178d33398b768fb59515c8052afde5a23`

```dockerfile
```

-	Layers:
	-	`sha256:27c4680740117658f3a6d274e90c1bc193f9aed297af2e9c8658296f77a30654`  
		Last Modified: Tue, 03 Dec 2024 06:17:55 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:58259995e2bf23d42df018ba25ba3a67372a2422fdc7914cc5a132eee35433fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59686248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2739463941d7f2c81e9dcf2985fa548a020146336a6608a92ab4a327c6ebdf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Tue, 03 Dec 2024 02:28:32 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7260c43f0f9e6c3c34410fdfc970a0d4fcc49429c791e26905b3e6bfca89798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c94c1a91810b80643dc3cac6052e446072381fd31485d5f5196bd3ea6e0cb1`

```dockerfile
```

-	Layers:
	-	`sha256:deab7f2dbd81f35b295f26a1874c4c6ce9cea7f2c767ec20cdf21e9e17c46086`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
