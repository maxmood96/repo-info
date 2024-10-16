## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1ed149700fc3c9d9ff0faf643ea250594833d1d5b43865f30d0a9f21c499d1ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:50fea20ccabba9f59371cb5929d7e531bb4961ffc04d89e2034ecd5a61b96a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82055652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdebc048f92c16dc12ba29883e4af083c3682dbccffa98c26d005c0eb313fc2`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98c7f64b4497240d576e2b294066f654ed8c737eca3a4cf5705f106ea7275e2`  
		Last Modified: Wed, 16 Oct 2024 18:59:44 GMT  
		Size: 52.5 MB (52519964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9d6a9905640e129c73563559e1edf6fe1d80a3cebaec02ef4b22fc58135172a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6e8b7597448e9f58ad0e3939640dfc8a435bc1cd46e6b1750636d3c45e14d`

```dockerfile
```

-	Layers:
	-	`sha256:c4c9eaf827191c86c801d90c25ef3f1a05f259c5d5e70f151bf3a4a4fb5c1263`  
		Last Modified: Wed, 16 Oct 2024 18:59:43 GMT  
		Size: 2.2 MB (2151575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7ce336138e1dea1552cb31cd4473b62e0fd26bec7ce76400758234346c4681`  
		Last Modified: Wed, 16 Oct 2024 18:59:43 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:20b0361fe387febf4e8bfe7095280cbd05cae94b6edf493a75f28525de18cb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79257122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3531512fea6ca5e2192b155006d3fac0b97658df476ce05cdd2659c46cb02c54`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0b6e0db202208129308705d94f3ed18516fb337adbb8327c7673118aea03f`  
		Last Modified: Wed, 16 Oct 2024 19:36:16 GMT  
		Size: 51.9 MB (51898793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5d2a18723d544a7f274975127badfdc3bf3f3ee335a1aff3b980585e088b3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c943b8312102cfc7e215b47b29323c18f2a13f01670fc0a305190261358f9f`

```dockerfile
```

-	Layers:
	-	`sha256:b446a3a3a2bb144e5030ce8a6ec4f5952ff62b82106a465bb117ee63dd3bc605`  
		Last Modified: Wed, 16 Oct 2024 19:36:15 GMT  
		Size: 2.2 MB (2151245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83e46bfec5297c6be0ec8398d2cf439d3c543c41a449c5690285c7b078b8896`  
		Last Modified: Wed, 16 Oct 2024 19:36:14 GMT  
		Size: 8.8 KB (8811 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f784a8e079b5ce548bb6eb34c02c6ae0ae17ea6b0656518ea671507db25c4479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88249373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4226deb4439a88417de5008f85364116573ea38fa2ff2087b237300db657b1a4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ea24f0642d477a00618b8e0613fafb9a7454c785d81637e77fa4425eaf3fce`  
		Last Modified: Tue, 17 Sep 2024 02:56:04 GMT  
		Size: 53.8 MB (53801131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:62588e3deadd508fd8ff729a913fbecb995dc7b7e964c9c73e8b72d878e0cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7a14d80adbc1b3c00a8db0497e8b1ed6617b1d4904995b207e859b3ee719e`

```dockerfile
```

-	Layers:
	-	`sha256:178d488618e1d967e5bd11fa83e08be2656a24d9851203b71c95107d7b7863b5`  
		Last Modified: Tue, 17 Sep 2024 02:56:02 GMT  
		Size: 2.1 MB (2148825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4cc1c152a7ec94a6938cf17d530fcf42a2b1fdc6ae1552d5e8c89b50bc20c51`  
		Last Modified: Tue, 17 Sep 2024 02:56:01 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
