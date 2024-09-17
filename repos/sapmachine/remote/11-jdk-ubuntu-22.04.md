## `sapmachine:11-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b43d77750329a3f8f5ac19472b83e2f0902be87fc4c790753b632c0cc58605f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf88797915dbc4832aa5818ce5b46fc1315ecfaaa190dd43a730ab6732d34e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230270901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb221bb1c6123239ab03777916195ef313aee77f9f6a1575750721f6a2542de`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af43ed6fb4deb7b0800847382a4cdae401a2d36d8a96726445207b37e46df74e`  
		Last Modified: Tue, 17 Sep 2024 01:01:19 GMT  
		Size: 200.7 MB (200735213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1be80ea3b944b3a861897b6759e2fce55ba55a203344af3f10b26c8595298d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62efadf00985fe08876e5988dcf098719551f6f40feed9512d7a397226d598ac`

```dockerfile
```

-	Layers:
	-	`sha256:02183fe0b9944731047c8d46cbbd7a833665a1e0179c47e8377e56be52c51a5a`  
		Last Modified: Tue, 17 Sep 2024 01:01:14 GMT  
		Size: 2.5 MB (2489152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4038074caab7b56cb60b8771df04e6d1ae11aebd356cd3ea44d4c89e5adffff`  
		Last Modified: Tue, 17 Sep 2024 01:01:14 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:db831ea86d25791dee8ed8f20f5265d6e7cb9bf82cbc524fa6614b9def2e042a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226551159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ada204e22c2373abc06ece784c1d7ee4e63db424b4165218051b8df803d67d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c6b5fc9ded1562eda8353fe656ada8b14215502678ef93de1d56c8ee7aa64`  
		Last Modified: Sat, 17 Aug 2024 04:45:34 GMT  
		Size: 199.2 MB (199192476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a142d099aa0aff7f7fe0117ac14da52c26a60d8e40e601013d8cd04e70cb9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fde960efd270fb8f6fd5376cc707e1069aa47238f43a14a768232cf0df684a0`

```dockerfile
```

-	Layers:
	-	`sha256:71af787178068853af8f1a3971c25dd19320180ba58975b0fe4bfe63a9f13923`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 2.5 MB (2489508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9926fba49eb7a38332c5e77997fde16ce0861e9d822a46d760c25831c9cd7981`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:84429111bfac982ff6a3e0ef5dae7fcc51e369eaedd108c9c7f5279aa1413e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221830298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae483d05f675f6b329765e93814b299fee3f6bf07740b2dbda88e1b034cce2fc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c099e9d5aab32add2cce10bb3ce1030e24db3f71ecc11a57902148c526172`  
		Last Modified: Tue, 17 Sep 2024 03:05:48 GMT  
		Size: 187.4 MB (187382056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca523fbe1355fca01aa2a4228a88c4656b89ba9c76733b949f31381ab52de9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164c8448bfef4b4354c241b416d04b0e3d6d8ca01111d8df63e744474d63834a`

```dockerfile
```

-	Layers:
	-	`sha256:3e5da59148ad02fe7ea4973278f06858b70836669773af07e63608cfda73991e`  
		Last Modified: Tue, 17 Sep 2024 03:05:43 GMT  
		Size: 2.5 MB (2490581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48c30a90982bddb12c157aa509f1d8b5b3e0820d8561d89b11ea82f9456e860`  
		Last Modified: Tue, 17 Sep 2024 03:05:43 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
