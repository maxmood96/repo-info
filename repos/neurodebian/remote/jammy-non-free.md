## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:8aed8de3f1160326e3957e3cbaa386a9ad82eeace52d585f8cc758faf39ec1f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2fa15741085a7b9a111304f94de710a342d4003de42f96d7188ae76614ee49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f3a6a8f1c8ad9cece02d2fe19baf080213cf7ed68cdb0ad98152ada06cb1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d350e6c4b05f6944ae006b8aab5488c91516ffd162cfaba7f84ac273d473b`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 3.6 MB (3625625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e43a114a27e26541cb1e85f4e91c965938ba1a97cae143d255897aff2129a`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9ace5a9e24d09a5d74cfbef2b3423c8652f27e8f966bd9bc62e9113363ce`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32399516aec62d325145feb3435edfb7a8ae0199ff2cb6bbd66c90cccb4d2e3`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 110.6 KB (110617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7cb48d532455ee1f3cb8304abe4242d944151fed04590177b16c700f70b807`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c57cc66c296caefe8491e689ab76b85cfa5a28354db8fcaf6d4e285820860324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607be7f30cc779a1e17202a6d6c14b2ac08edabd49cd5703daef1c66963a2b95`

```dockerfile
```

-	Layers:
	-	`sha256:28344ea9cda64308e3f2beaec2b0f1ecf33f042627051ad839a05fbb550e8d2e`  
		Last Modified: Tue, 02 Sep 2025 01:07:24 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32e711bd76c0a3933a65639adf42f2367cc2f94d3e8d671098de1fec9256e73`  
		Last Modified: Tue, 02 Sep 2025 01:07:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3477c05d1c44a95df25451442a0582adc59b19a1fa02d71ac9defd2e99dea2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe9716177d8f8c156f3750861d90f455ba6b3aed16e8bb8c0463bc4fd51b33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f860954b7aec09e8e634d06f465a2fee9f5efc8618a451be9ca3999110a04e0`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 3.6 MB (3598078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80240768d635dabbcefc8ff489dd31b390e710ec1a57a20717f266cbb43f3a12`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b19e7977bcb10026b60e7b92462d7e2992d0969dcbd487e6c1716a80bc89c`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a31027b0f91a269a073a36622efb6855af47112b4c53f9b2bdb4ffc8b6caaa`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 110.5 KB (110527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56be4a06905892f6b37985a75ee287ae36160af8de2c3299e76657303232f5`  
		Last Modified: Thu, 02 Oct 2025 01:27:26 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d027eaa6f6342192209425d6ecebaa9137e2db5ac730d34139eff64a9ba7f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f4d6e154722074fc244a1c8c4b58453a017f4c753a2047c43d2a7e1d1ca1e0`

```dockerfile
```

-	Layers:
	-	`sha256:3446b6bd4ea75dde0ade5bf1621b0940160475b92f8445fadf17a1f4e63dfae7`  
		Last Modified: Thu, 02 Oct 2025 04:07:33 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d889bfde4fce06c5ea57e1f1822e2efe7d3b957970ea5f2f890dc14ec4116c`  
		Last Modified: Thu, 02 Oct 2025 04:07:35 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json
