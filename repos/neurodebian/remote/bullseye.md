## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:58a79d16e7a892c7a9b205ac6b6fc5cbaf75dd3abd45011c0495b6c36bb231b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:255fdb245facc56597ae9b5b225347c9299a146aadacd840189b2b52be189ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b449ad722cd075d476b244aed68df11ef85b5f61cac4ed6190ac5fa6e850df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a21ad05e392fee8d676440be99dd209ac18de59baa992f707e67b7521df0b6f`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 11.1 MB (11105054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a68e13233f02b4104031993a0684cc1d882e1ac9ede7c81ff542bba3753b5d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea73ea3f21ff7c2c3cd991b901ff12faf26526caf9d030ec0dc48c01494e35d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a580996243e3cc1edfeab84f80d57b91cfe0c769853ddc306ec0fa2d61b92ce`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 101.2 KB (101201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee411d1056c0875d426587f84fd261fa8611ad1c3896cfdd5e825889608a4094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235826dffcc85d41f141da43c90b3a0bdd7d9ace4a10e6d8736c35cb0d0e2b85`

```dockerfile
```

-	Layers:
	-	`sha256:b228de3db05de80fd3f25e54a24bc022f75c3fc059ea2b75832bdb6ab25f659b`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056a0eb241a620f5b51893b1c44746c7a38dd857e05ea98b9a9c29aa54d1da`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 13.7 KB (13693 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ad9866c68ff2e19c7299cdb0d9878887cad56c503d83edda51a6712b9f1957e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2001048eb7c80b6aeaa49269443f9792a9706f622822896abbe5a84d57c42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78070b166a3b33e5e36dba2e5c6120eb0be4da63e2fadac8989546e77ed84127`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 11.1 MB (11106135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6409cb1b4b20c21ebb839fc02573f587d35015a457c2a28f6ca099e3cb617b6`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1300d0acb93feafce5997490005d13990da5be84a9c0439e886cf3f9800e`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a370d124f43fbbdc6183d48f50d75083b3c2260f2deb41bd6be13b1408428247`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8829cd60b8151bb6843bc62acbca2f6215345cecb217996d00299d68001ed9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df58af517ef2c2b0c94f3bf5a81f4d4a8c2ff00b52e3f3cff3dd1164cc0ff7e5`

```dockerfile
```

-	Layers:
	-	`sha256:af2867479a8ea8851fc9af29c621493be023e1e07882b38427000321f7ef7c06`  
		Last Modified: Tue, 25 Feb 2025 11:26:47 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ffb769122edce0984f644047190e6eb18719120068faf3447665649c0b7e669`  
		Last Modified: Tue, 25 Feb 2025 11:26:46 GMT  
		Size: 13.8 KB (13817 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:b9b68a2c030f7816a446102efc01b832a31d88e8e1fca95e90b347113d66ebd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd3b7662aa6fa7dfbcdc31a0f3b16bf895d779ffa358418f30a1c362cbe7835`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee56fa4339347a5d9819313a3c54d7a27c7cb5b8d5cc000ffd621148a2d4bd`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 11.5 MB (11500400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623551ff0580ebfcd93cda07f359615669ed2b060f30806734fa12c97c1c2d5f`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d499538f85e1b885adb4a58422c8c4e7e67ae2ef1d8610a84f6768bca9ac071`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79821c0508cdb29d85e661e1a99e8f83683500bca6747943a84dd34dde2b1df0`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b61186c3d9e091e599ec9124821991256c93bac976bcae94a4daf4813c86c03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9a496f2a67b7d3857b9409a40da1a518023ffb63a34302a3c28bc774f065e6`

```dockerfile
```

-	Layers:
	-	`sha256:60dd1d2a40d86039f2e85dbab1797c9b022a0664a6e0d2b5b87ced8f62ca7ef9`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845bb2b878bc2a3e85eb925ee5bd62253faa04a947f6688ffce7309902fbc387`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json
