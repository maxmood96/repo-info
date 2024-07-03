## `sapmachine:lts-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:e6fb1e57199924287e252fb817249fa87259f913df4b1be7efd826dca46bd751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:0dadd3e7e0376e65fc0f1042838f4cce18514d52a57678d5c0650cead06b66fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244605096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ef7b1393b8e9d90cf08428b85338ca28f6c588fd17affa21016203fbfe3ef`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f015eaa0c4b57c8656d6a8e84010c13970aee4201c13af793ab1bb4e77dc6`  
		Last Modified: Tue, 02 Jul 2024 03:32:08 GMT  
		Size: 215.1 MB (215071041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7b939edae7ccc2b49fd8da14a362710f75e9b52eeb20c39c86a3f53a753e555e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659319105e0e7b6a17f31d46ef0674618b2568a47d5a8c02c9b33b734fc90b1`

```dockerfile
```

-	Layers:
	-	`sha256:69d32a38d71abb297dcd75c2ea346fd3209b16839c66628b38ba449d9997fa07`  
		Last Modified: Tue, 02 Jul 2024 03:32:04 GMT  
		Size: 2.4 MB (2444960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995ed7f9dc827e13d7860a911c54c61dec777b601cb801edcdf3d0958fc16c9a`  
		Last Modified: Tue, 02 Jul 2024 03:32:03 GMT  
		Size: 11.2 KB (11209 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d9d358ab336e4ead02db46ff625f148a5d8d5a267fee820a45d7fb57b15331a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240481994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed9ba7df37648061161b6b24a548529ce034799603f2ea873c3d3b281bde807`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a848d38bcbce76ab42f0c5becb6077fd33a5d8945e9cf84feafee03cd748fb`  
		Last Modified: Wed, 26 Jun 2024 00:06:52 GMT  
		Size: 213.1 MB (213120212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08093ea4bf1945574e99b57ef0a091a99195ba1aa177570f0b4b8b33745a0ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2293d0a454c7457f00e2fcaaee3a6193aa292554d6be26b4dea85804aaa673cb`

```dockerfile
```

-	Layers:
	-	`sha256:f381e8ca1307fc869ea4187d12f4f53e77fc6c3f041e8e20ea6b83edf6fae9dc`  
		Last Modified: Wed, 26 Jun 2024 00:06:48 GMT  
		Size: 2.4 MB (2444736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7d535ba6f5317e5900e491f76131dc29beae223ad8e435c98d078faff5dc53`  
		Last Modified: Wed, 26 Jun 2024 00:06:48 GMT  
		Size: 11.6 KB (11605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6530a2e9b47cefebb7da31ac03655c833a0627c9e25abc9300dfec6dd3a2ae4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250842410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a535548e76db3937c1a17833007ecce553c399eb8606800cca8f22231002b93c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae871d8c3573fd54949eea78a1cf5b7987e93d95d7db648528dd9c830980d13a`  
		Last Modified: Tue, 02 Jul 2024 21:25:33 GMT  
		Size: 216.4 MB (216381329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f6e36a8e7a097b531ef1bd1ebbbefb82e02e6a71b38e7309382a8955412bbf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08695e76981995de8ffdfbfb87cdc56f8c9d9e2f20c9818e28a77bb7d0ab44d4`

```dockerfile
```

-	Layers:
	-	`sha256:25561349abb8806001ec67d30c1b73c46c5974134e90fd5d88d08407d146f0e9`  
		Last Modified: Tue, 02 Jul 2024 21:25:26 GMT  
		Size: 2.4 MB (2447038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee62ce9fd20c82966c9c4a1fb2940d02c32a2f66051e5a4ed788c7955b5306c0`  
		Last Modified: Tue, 02 Jul 2024 21:25:26 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.in-toto+json
