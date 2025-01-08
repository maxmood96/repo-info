## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:8c645958f1041cf16751ed05c02cd3f1c4c972d617d3e54b2dc0fdcabe8406c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:10793d833eadea4c7532122950632f646c90f590c90b95d05410d9781c909e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250473596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fa9ef38a75007ccff571377c0b26fdd3fd65bc9edede43c4e0e19bfdef90dd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486cc8c4b818a960df6c0831eab58115134563bc30bcba0b1c47cbed661981d5`  
		Size: 220.9 MB (220937908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2b75a8ddfc9acae3bede2348c6dbea877aa7ff5d06dc5f8a09cd5ab1a5b9157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2248505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8fa966c66498498138d8a7c8325baffa5274009f5c1fe992830954037febb2`

```dockerfile
```

-	Layers:
	-	`sha256:25cae9e1d2249703b11629f6679800b6ea6fa290cce1500cfebd876608114e47`  
		Size: 2.2 MB (2239109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9bdfcd794ed945b4df670e35d693fa357a76bd0660c8bd2116c247728e1e6d`  
		Last Modified: Wed, 16 Oct 2024 18:58:49 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b22a75395384707c85658abb455231f7ae5e1e3d5dae3ca46d2fb0eb8445e564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246221274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18942caf15bde31c8d5d99d56400c7c668e14794cb8a77970ce37937aecef620`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd2a4a384f02d984224d51818d3a625f06fcae04f51c1e386c68ab8a9edec3`  
		Last Modified: Wed, 16 Oct 2024 19:05:30 GMT  
		Size: 218.9 MB (218862945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c5c7649fb32b2a9fc07f742bdd651f176edc9860170c85e790c42d9dba494cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ced6100902bd6ce4aba6f48589fd20c3447845c4cb9da83b0cc62fa035e2cee`

```dockerfile
```

-	Layers:
	-	`sha256:2a65102a28b31c6515e94c146d46e45e9349abed355d80e7b2e58c147b05ad4b`  
		Last Modified: Wed, 16 Oct 2024 19:05:25 GMT  
		Size: 2.2 MB (2238172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097b5afc3fa43e1c73d538a4eab2172571ba3f198eaf67777050206acd19b0a0`  
		Last Modified: Wed, 16 Oct 2024 19:05:24 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7cfe20e1f8f626aab201a8f1cc87f97060f3a3fa9d9ec098147f0bb54b491b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256232977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65ca96bde63b5ffd6f47ec667b1a2738ab67843eb8836cb41a68f159e809dbc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea67b462c28e9224d3bc940e2e9b56e73095cddad1c8195baeb337cca494be1`  
		Last Modified: Wed, 16 Oct 2024 19:10:13 GMT  
		Size: 221.8 MB (221784735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b92aee4df008456114e1ffdc46ef11a635d4df99c8404d5e88508556d9ac4320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7177ea3fda56cad7543b9854c768a77671fe9dceef126f467cbff6e3d39be838`

```dockerfile
```

-	Layers:
	-	`sha256:f51b42068655b05d87d48278fea1bc96151f63f38fb7799e30cd737ffeeb413f`  
		Last Modified: Wed, 16 Oct 2024 19:10:06 GMT  
		Size: 2.2 MB (2240462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b840169ac9ddde96e4099acf7c4c69c25c70a76bae061d49362481c1398778`  
		Last Modified: Wed, 16 Oct 2024 19:10:05 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.in-toto+json
