## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:0563d2536caf4900b584a6744950b5933b836feca88b18f1193dff60f6db5f58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f65ab94de2b8eeb7ce8e3ca843ba825e9c7fe90ed9b6634fbaf551a4d61fbe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce894af6d2b00fbd05af4826250646684dcbb657ac827263cc9e0f14b863a70b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4394bdcefc6fa3b661b40e6eb591c5f4d4a4948bb9f94efc8cfb2cca63ab0`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 3.6 MB (3624440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe5dd49d306503d46bfd8860d908db1bd43054f51630df3cae246cda80ab538`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8033217859346bf8a7b9a474edfbb809fbeb1a627bad48117b921acadae46`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466de1c292093141aee6e0b2e28cdb5dead9eaa5b899e28405a08326e0afbcda`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 111.0 KB (111028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816e7a377a6dd0ca7d84582d786a62e2eae934a80a7d10a4968032c0c09c847`  
		Last Modified: Tue, 17 Mar 2026 01:43:52 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3327cf1ff11761f7d3fd4c86c31125e43e1d212147fdd91197fb422bd6610d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42da9986bb0da24b6b98d1bcf5be809650d9e940fa3ccf81026bdeb9108e866a`

```dockerfile
```

-	Layers:
	-	`sha256:044f0f60135fd32871cae06a72337f371a8c9006584356dc984cdd534d47b695`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e31bbe852e2d1e841c91b37d8c7c1547bbaf7a57650644745cdf4181ae15a`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6a1324ed061523ef22e532caf02b5d13a7d342ae3c0581bb98378dbf5998b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31107206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d789266f761ee042462b64fd62015f0592608f8911a98f067d7c67233c491064`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202f320aee81dfa65dd047461f0166a121168590d3e51b1929d1b5dfc59f4dfa`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 3.6 MB (3604661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7beae3843cfbb7d29beda7d948635e8eaa8697817f1d97af9b26e6201268a8c`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edf385ead3b8fb2f0dd3dc7542928119f98160e2be31611ce29c87fdce3b147`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549bcc2860f4774039377e1639794661a450d3832d5477a77df95a05dc4a6d`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 111.1 KB (111056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99cd67958630ecee727aa5ffdc70e69afae561b6c827d318cec4a3933ae0e21`  
		Last Modified: Tue, 17 Mar 2026 01:45:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3e1cfe4c58bd5d2c1a8f4abb414817152200d5bcb6fb06b31541ee24a67d5391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de9d011d760b10371e31fcceb88b7b5a15bd2720da1c846601075f89823426`

```dockerfile
```

-	Layers:
	-	`sha256:a53b614a54e6d4ffea23c6091c74a19b7dfe81b57afd8f6f1332b06b974fcce4`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c823c9828410b7a964ea17197da7b784782378fc7dfd14a237daf78286372be`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
