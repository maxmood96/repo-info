## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:e1f82331fed085ae65759722772d310e652df3d2580df3961a0fb4ed72b242c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:44b94bce3070df694aa69360e5f4d25dd331ac925b63c7b12d722ea917b73199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f75ce278b18fae6ca6db2466f215ac469aad802640996a9583a48ffd6083f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575cc642df1608aa3a7dd13a5d11d9c1b0e947da30b140327dcbbb42486acd20`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 3.6 MB (3564688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfdb56313bdee74c9035c64d8f0955f4f96eaf39216dfcc07f1563f915807cb`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4058043e8913014bbef8314241b526aff31cc1dafc3fe31d6687bfadd45c15cf`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0f244aa413cafe9503aa54e962810e25eeb5575cf14dabf003e18e01e6b79d`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 104.6 KB (104579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f9c2a95be017c7cb55d088b520781d84106ced3f5371b3ffcd3c572905a83ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4796c51c23cf5e13016c160f0e99e73711f2d6f598b258ed86fde96380d02044`

```dockerfile
```

-	Layers:
	-	`sha256:d93371c9d6ece2f6cf45976a5c5c15c04a332fa920dda65d6cd64bb5a887d710`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.1 MB (2120907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664b66c569f16540a51491a7c6e5b3ac4abc94ba3e9c470acf20345c740c7dbd`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d68642710aae078b8e89996ac5eafecc634ceb8ae7b59ff56b83785d4973e3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c0d4766cf8a7b23c701e4dba960d86ebe34269987eac6c889ba6f61e561f29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:20:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ce85d6a4f7e55f753210ea58a2069bb210b5773b1f90667ae1b96ad6c58f0`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 3.6 MB (3561778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3586010e44c2321adbb1a013c27b75c2594d069fe8a8b923886da05572f2ca1`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9985cfd214b77dd7244a723023eab3d0f045e3a08ae09793263854ad201e1b`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c81b86547b2f4045feaa349c342c702bc693662e5f588034446b0903797d34`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 105.2 KB (105224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e97b1e00c6b966efd15366c8bd5b64ad7ec88e5f191bf039b92fa49a699b8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699c75ebf1dd1c4225e9322be2587cac789c7c39450ae78578895be5060be76a`

```dockerfile
```

-	Layers:
	-	`sha256:38310a16f1f7da0df5b8da8dd8407e79ff7ca8e4a04591a8f57b7cd2b3ab0c54`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 2.1 MB (2121952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6a03093006d13698c10c2e93a860dca32148404ed133224a10bcf8a4231d85`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
