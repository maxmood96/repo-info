## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:e83bb62e6895a9ce374b63e4ef3a0f74339025e8869f9a3165ec35ef951f2a3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:53d864d13ad3a6c221aff04bed3280647718cb5f7bdd41533f927e4c2ffb6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228767728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0a41364f570a57333079e1990c56b36961cc4317b55cd097257ff3c4fc822a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:12 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:12 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5940c1d353ebac53493d4a83aba85816203a8ccf7da96bf658b93c6020fc121`  
		Last Modified: Tue, 03 Dec 2024 02:36:27 GMT  
		Size: 199.0 MB (199015760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4033b59b36bf7c4aa3d13354437f6822d0bccc7eeebd4d4d8415c475c495ea1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30b8e43f513ebecf01691ddc2e6ec118fb6288d2ee96aa42887279274626d9`

```dockerfile
```

-	Layers:
	-	`sha256:de4801f67a30a099328ea59c821faca4a4722535917883e3c8f479927a13e262`  
		Last Modified: Tue, 03 Dec 2024 02:36:24 GMT  
		Size: 2.2 MB (2230796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4ba68b4212767c0204c010f3e650c6cf5281659d59de5b948fa2116423d5e5`  
		Last Modified: Tue, 03 Dec 2024 02:36:24 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d4906d61296d2e04bcfaf0f4b419afe8831e593cef958519631583950b56389e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226623630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f49734cb2aecfcfeb2a69a2acc8fb25c8b1b4d501da433fefd43f463df1deea`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354e0baefba444abe0a2b7f52018c57857bf812f121ebf39a555a0f84c30088`  
		Last Modified: Sat, 16 Nov 2024 03:52:05 GMT  
		Size: 197.7 MB (197731205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26db2cddffadb2199580f2d66549eb1153985f1786689779908fc44dacb10a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9420c7e9d1bc131b6fec6197fc485f92d4aa72ec491ff1bb0bdfa19e63a503ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f19184097a4a97466cfddafb0b7122ee56431a649f0f4737f39a8cb946cd846`  
		Last Modified: Sat, 16 Nov 2024 03:52:01 GMT  
		Size: 2.2 MB (2231258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5537815de57baa669e32c7c9119079f62f5335aab76e4702d26d4a0350518c77`  
		Last Modified: Sat, 16 Nov 2024 03:52:01 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:43da442b7412c6ee5c84840eb920378603be7bb67dd07e5686c7b419740b82a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234423831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9932925bb2992cb50a4fed56fdd5c62fe24832fe98318ce0213d174d7efe9147`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:12 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:12 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37520cb7ef039c969a64015989e8d755ce908ade6f0aa86abbdba0accfbfc45`  
		Last Modified: Tue, 03 Dec 2024 08:40:46 GMT  
		Size: 200.0 MB (200035011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c4a1b287662c2859b67af128cbc8e42132a3919969ca4701621eaf04ea8f1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a879d9081e27413650fc07f5ef4b50f1fa79a753a8de3e1e13df58a50e91be`

```dockerfile
```

-	Layers:
	-	`sha256:d9b46c8bc33f5c598ff287d12203bca180ea89428f79de68562a52a1edac89ea`  
		Last Modified: Tue, 03 Dec 2024 08:40:41 GMT  
		Size: 2.2 MB (2232733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86775467e5aa2e8ff0c4deec5b29975218aa215bafa4f50818bc81bf6dce2548`  
		Last Modified: Tue, 03 Dec 2024 08:40:41 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
