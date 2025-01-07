## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c01bc07063701cdc7ff657f1185824d0d49b9a96292bc2c82afa46751931059d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:0800a1f7258787596bfd66b6aec24a10c308a521fa11435a90fcb5ac1fe5a1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242878840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d24ad7266e9847b422aeaac364f3c3a8a32079d529262c78d6f38573c097574`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70925c66e7c5f33faf6f010b443ecee4c730d134baedb9e10fa8da717e80c140`  
		Size: 213.3 MB (213343152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38ad9e78c7b3bcf421083fb504c7d0b67fa4f54635785903889d47dde763e770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05caabf49c109fcb76dca1be65c46086f7a79e5946548700a266ed1b6c486dd5`

```dockerfile
```

-	Layers:
	-	`sha256:b1dd838be4e211350ace4001962929bdfb210aa6d136d0cb6ccac039bc91a86a`  
		Size: 2.2 MB (2237184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4148c7940baf7140897dc2b3900352747c99ab0266d7b001e9ee4007a170a889`  
		Last Modified: Wed, 16 Oct 2024 18:59:07 GMT  
		Size: 9.4 KB (9412 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:32eb8345db215a8f1c46dec9ad56b56590b2c3bb1b0a6ddecfc6d9cfb52008ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238848150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d7af8477dbc082bd77be6f7bbbf1040dbfae646fe431ba1eb3f64c50ef41bf`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30162572c69819d24ed3a26c2b76b7c359e53b8e50e831198666e8ed2237f4f`  
		Last Modified: Wed, 16 Oct 2024 19:19:15 GMT  
		Size: 211.5 MB (211489821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e57f31debcb9a2931f7825c61ec4ba207d81948601abc0b5f499c536ee7480c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82300c9bcdb0e72555954d36eabcbcbe936e98d8eb25a7fcdf88b1eaad29909e`

```dockerfile
```

-	Layers:
	-	`sha256:f5e1387cf389bf89bb408d050ca81451a87daec3a73d0b1e9ab230aad112a842`  
		Last Modified: Wed, 16 Oct 2024 19:19:10 GMT  
		Size: 2.2 MB (2236878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d588cee214956ee36b5ce75876da21a9d6103989f35f993efe517d9c1126c972`  
		Last Modified: Wed, 16 Oct 2024 19:19:10 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f9c443d954f40da36b81bc283e5274437f010be824d1d4d719c33bcbea463da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248943519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebcb9a16a09af8410e0f04604b31c4082ddb590fccb4ee6641ef6805b89af41`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fadc43746b2ed986c4dc1a7af65ff47c0ef6e9cb86eb9f7abce83f9e0326b4`  
		Last Modified: Wed, 16 Oct 2024 19:35:26 GMT  
		Size: 214.5 MB (214495277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:810bcd2925cf6f31b18345b2800fe9b404f857515ad388e9c0ce34c02dbabd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2248618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96783084ab4f4a2d1acf9eadec1d885c42820b1594a6d03b50cadbb8f3d40bd6`

```dockerfile
```

-	Layers:
	-	`sha256:e36bf881e1e5f9242cf83cfd70562d464c558dd6803654c5e1ba52b9330acff2`  
		Last Modified: Wed, 16 Oct 2024 19:35:21 GMT  
		Size: 2.2 MB (2239156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81fa1d66691dfd5c5e38eb45039e4a321399cc9ba073f8d877cefdc5b328a89`  
		Last Modified: Wed, 16 Oct 2024 19:35:20 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
