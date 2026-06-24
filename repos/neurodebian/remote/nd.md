## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:cae54b6597e691d0bea0586b790e983a789af653e6850a7c3be61439ef6b40f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:e855acfc14258f5e0bfc1f3788879783ef4ecd36ea6e5ff1fe50a9e785808d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2c9a697c9c7bda1ef74e1ff9e53d02b402ef9f4c8546229ce3b0d9d10a0a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f562021cde277839fe5ca0c653ef4c5ef671b02aa5d24362582c01d2270996`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 11.5 MB (11461802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7be72cac78f9fab2e737c59dc780b7780871b6e29b62d1b92978fd80a032dd`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514595ce975e065a7ed83b4e9987d7718274066e17577300b8049c0f1276cbbd`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677003999fd2b129fe17b5835847a167d2c799422af38d35393c3dfb28fa7db`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 89.8 KB (89828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38b81ad9e50db435945b1954d30eaadcc73412acb74d99896963aacb35c543b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2965590cfc0691f40b54fc3d69d7afb8a06dc10771f0bd7ef9b67dd88c013a`

```dockerfile
```

-	Layers:
	-	`sha256:2a9729c7316703c3ae5a5f8fedb49eab3e156bcf2dfe5554741f6fdbf43af3a9`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 3.6 MB (3558319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb5aaf15ffae0d1701b3d0aa7ab956378977d64b1cdf869806409bb5cb04573`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b52d4611b34a2bc915f7402bf07b7c0ed611ac77167147a1fa579671e533f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e718cf8135c7a7dbaf28de21e4a599de708b5e737331e8374f470d67a4325`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f216cfca8681658c5c6a7a8b3653ba38754d80730e4760fa07c5af0c77dbafdc`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 11.1 MB (11093783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c245f33d403e20631db07d85c7949c38d447f59151983e6ccd177844c70b2da`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f20446e70687694e58be96b1e8dee8abbbffc8a86361dfef1e2c9933a7e172`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c777496248e833ab9ee2388720300b95430fe7f379a711f6d0d603d2bb9dced`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 90.0 KB (90032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af5bdee722473dfe53afb51c4052273ce01321dc38891ad423a777cd3eed1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e931479eeae972f6d3393eb1fc52d4600aaed088476de284ac64185006b8aaf7`

```dockerfile
```

-	Layers:
	-	`sha256:c667f4c018696b0a60c8e913790fd50a5b7b27861cbb09b150589add99b16396`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 3.6 MB (3566474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0311325e77f970962d6ac2bd4c71cc3ede59589e9266f3b563c2edb9fff8ae2`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:9818680b166763d4cba8100a46f14e9d58332f1fe82ec0a0732d82b7e0774d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61871687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b307c252def927240b96a69a452a0452145c179fa93fc6235617c9e727d0bec0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2283acadf304f3a69ec710b735a0744bce58269bca9c33a763c6a6817ebd5fb8`  
		Last Modified: Wed, 24 Jun 2026 01:45:58 GMT  
		Size: 11.7 MB (11697753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74779e8bd3a27443fc4cb66b65d67ebf43aee120fb4e2e8fc6c8f9684316f1f5`  
		Last Modified: Wed, 24 Jun 2026 01:45:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20da08ee4148d3d8b05f7e6f1ff4e1e029c8baae0a9de1d458e6bbd5e032361`  
		Last Modified: Wed, 24 Jun 2026 01:45:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d7ce12599aa6607c302cbeaa60e282efe5f6f71894b84d9b7d29c89ebc5716`  
		Last Modified: Wed, 24 Jun 2026 01:45:58 GMT  
		Size: 90.1 KB (90077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fba4e4fa4651d2069721d5ef3846887a6534e37da0d5d2dc5ac089d0272ff3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd131bab76d5a1fd235415f2fb8567c377333f15ab803522e2ad4bb99edf126`

```dockerfile
```

-	Layers:
	-	`sha256:b129c2c7b5e14ca7e264ee6ac01147d229136ae6e30f4f79963b279681076475`  
		Last Modified: Wed, 24 Jun 2026 01:45:58 GMT  
		Size: 3.6 MB (3556275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de8673fe5f1a69c7396d154a5350be92b978e6f5de36c6c95b80265c3478b31`  
		Last Modified: Wed, 24 Jun 2026 01:45:57 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
