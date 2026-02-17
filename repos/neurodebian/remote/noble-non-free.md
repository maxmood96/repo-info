## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:a7144487a6b26292cb693d313f5fe6008a0ec8af1175afd7a8a0ee3722258e06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0cd7e0a336536969469e437390206e20cc0e2e6e715f36bb2310d39d710b902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33399972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace43c4c113a98607283bf2b3471e9cec1f264a00823e2a8092141bc3ff0b16a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Feb 2026 20:29:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515f56a0136ac890c5579505bb7cca7e597ccc62957a7b8cd526b2c44e6c892`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 3.6 MB (3564572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85bbbcb490789536abf66cade91a9a49cc57d9fd42d69b55cbe196f76ef8b2c`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05953ad0cb03708a19c986de26b25997e81b9e8276f474d36afa35b8a6c49e34`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b1424db1c457f269e53e6133158e975349e7a768bd161474c8125ee06d2073`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 104.4 KB (104448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a64dae047acd904d962e7da565cade24054d33a4a95d7f745f74a2dbd7f44cb`  
		Last Modified: Tue, 17 Feb 2026 20:29:30 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:572450c0be614c10fe35dda4d911bac23e51474fd6be82cfb94e2bd6c9182025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b3b16dcc8f9d40a1b3f09f0bcf0541195b32d503cd0ab03bba6ee6d3827c6b`

```dockerfile
```

-	Layers:
	-	`sha256:f0be2d2e05f9c016616ff823854da1b3bc8b9837e01ef128bdb6e153f9cc825f`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 2.1 MB (2120909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f33dc2cb3bffa77aced26a5f390fdab76af7be7dec35c0b235bbdfe7e44a47`  
		Last Modified: Tue, 17 Feb 2026 20:29:29 GMT  
		Size: 16.2 KB (16161 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fff0ec4362adc573770ebe8da091b593449eeabee79d62b783fa374714cda5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32535540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd10561082b49f6364e3736ed043f5ba55c83e97529c75e88a4d8c1359f08f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Feb 2026 20:28:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e62ad865addda2f739b0ffdcf84f97db33cfa07d0f6bccf57a4709e6b2dc616`  
		Last Modified: Tue, 17 Feb 2026 20:28:24 GMT  
		Size: 3.6 MB (3561758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7f6d16f7c383c42faa43a7dd80ff0d07d964b806153b68c29008616d47a6fd`  
		Last Modified: Tue, 17 Feb 2026 20:28:23 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7103b9471b3198490e4b6c711827166766069b946c8b0a28fe2b0680b1366fdd`  
		Last Modified: Tue, 17 Feb 2026 20:28:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e7cd1e8b51fbe51a65bd9b3a4952272f93ebaeb4e4974e3edac99db25dcd73`  
		Last Modified: Tue, 17 Feb 2026 20:28:23 GMT  
		Size: 105.3 KB (105319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135662aa05d2be98edc7d73e54a3bf0010f6dae38d9a9fb5bcfd77143afe06e`  
		Last Modified: Tue, 17 Feb 2026 20:28:24 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:511bc4fb5a53c02590caef1c31dc296b276fc27a9947bee75639cd31e1a3d720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be806025f4c0cf44bd353146baeb8c7f2ef4be48d9b853e7e2ad8497ad3dc465`

```dockerfile
```

-	Layers:
	-	`sha256:bfeaa1ab09f56fce26562de564ae66d0c4a948a3236e94000b242a0cbe9d5d0c`  
		Last Modified: Tue, 17 Feb 2026 20:28:23 GMT  
		Size: 2.1 MB (2121954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5400076b7d800dd8fb1ce16ec992b876f1c2ebbeb2cb6a6d8c11bf11211c27c7`  
		Last Modified: Tue, 17 Feb 2026 20:28:23 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
