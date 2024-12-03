## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:2a28499c1e34f40c420aad409898c2c9eac8df8b9fa4c50311a42b06272538a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:44319b8e4e47452c666c44a6d7ea5f78e58daa00d3f5f5c3ca452263f1362262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83883478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad82c0929539da9ef3aabb3d13852fe088ecb8bd017c7afe10c29923d2077b6d`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:92dd2768bf53a3c92c48954700e8dffd19a64a8a607b6ce7a3fbf44a4196d462`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 54.1 MB (54131510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c5ee8cc6bcdfd06974eeb693a380ce919e51a37613139df547f4a60c906c2a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1ea1600907610eaf6970746aee8474a49054aad16811bf00235e9552bdfce6`

```dockerfile
```

-	Layers:
	-	`sha256:cd9dfa9009620eb7284b44fccb0e74643d7692af1807dd052511edcb42a229e9`  
		Last Modified: Tue, 03 Dec 2024 02:36:41 GMT  
		Size: 2.4 MB (2385124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129243b54f6f74091c15a087ca478b5d7e856a388637b8f54f00de7c5fca24a4`  
		Last Modified: Tue, 03 Dec 2024 02:36:41 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4fa57c7049a245aa940ae5bcaec51d290a0bffccd114fa42f95dd16a7715f844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82451315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d3cf6a4b80cd04c8d4b4e3bbd7c41b021c0fe5aeaf8fbcdac3dec03c542d3e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:323a99a6527227fb5923ac6f538b26e97509813fc36c7aefddd2ac3124d7c3c6`  
		Last Modified: Sat, 16 Nov 2024 03:52:50 GMT  
		Size: 53.6 MB (53558890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78d504eea2a8f83916ee1653277189b83f98ff89b5e7b841c0f3d01019ec7652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01522a71a414e58c81f33edbc21fb810a4d513051640c7a87cde65a45800e54d`

```dockerfile
```

-	Layers:
	-	`sha256:9c84598b217ad06009d5cf7072d34c82feb887f1abeaef4177ba32f73d915a6d`  
		Last Modified: Sat, 16 Nov 2024 03:52:49 GMT  
		Size: 2.4 MB (2385595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e23fb91a72b598f335ffc92ef1a957fa0cfcff57017d045b757643ee322e6c`  
		Last Modified: Sat, 16 Nov 2024 03:52:48 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5c63dff8f750eb1c9a7c0f38f4731106daa7b042148680feb97090e95f3a520c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90155022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585a8d5e0ab9d437c4c86b20d937c571af66747d3e0a774c2f11c4290ea33770`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:324913f712415863a7581ba064fbc63acd916392030131f4d0f71911aaddff69`  
		Last Modified: Tue, 03 Dec 2024 08:42:22 GMT  
		Size: 55.8 MB (55766202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1ca19f7e5e37c94087bc1cfe66a29b01e10e7f32239e004e76592e7f35945a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba413c4bfbb0652a540a256a87c50a2f71f07b3ff2ebf1537090f3f28151444`

```dockerfile
```

-	Layers:
	-	`sha256:ed58fd613c48d8c8845bf81e2cd50824155a5f9965b246fdd0ab49b36b80c464`  
		Last Modified: Tue, 03 Dec 2024 08:42:20 GMT  
		Size: 2.4 MB (2389073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7024c2c73c62ab3e878ef2db6604f0fea9199c4bf8e99669fdad6f5532c389f4`  
		Last Modified: Tue, 03 Dec 2024 08:42:20 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
