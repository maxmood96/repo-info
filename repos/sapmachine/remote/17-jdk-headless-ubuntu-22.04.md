## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:818f837ec983ed0c0851c1cd678091353763746ce4959a3b23419dcd2df204fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:49cf7708f48cc2ee744a979ff7caac5f95cc84dfc059c9a5d47a6484b65c296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228360351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda3f0d0ea9f0222484b5b424e710dc04748dcced1cde0a02a07403db84b4526`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8004e5a9d5e0a972410f599e574e80008644edc080a9c46b8498b33dbd64b1e6`  
		Last Modified: Fri, 19 Jul 2024 18:00:27 GMT  
		Size: 198.8 MB (198826296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d72e76e68962d77a6869ab742339a4084c06d251c2f1cf591309ff2f04b4dd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ec0ce83270f4583742edac086b62da347a21352dd6c19dfa50db746ccd610`

```dockerfile
```

-	Layers:
	-	`sha256:19fc463f17ed9373e3b94f08d768633419dc55bf8e5e520f618807111f1b9744`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 2.2 MB (2227955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984c1123a4ee195aa211db4eb6b6c5a10363b32de0be4ad686ff3b7788d32d`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c90b281ca29a11877c4eba770e86a3fee59e61e4596ee445df0ae7beaa8818ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224784364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8040fa5f082ea515e4958ebf2784d43e4a14780d8dfbd9eb24b0c9391019ac`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e443c8b501be9223fdade1be877cfe86701185e2a77a0ec894b2b790e92e4`  
		Last Modified: Sat, 17 Aug 2024 04:35:12 GMT  
		Size: 197.4 MB (197425681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bab68122ef70c15b53a9c350b9fb0cf65437b49260d44db9f11dad1602543379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2232ba2498abc5d4e9677c5f3b0b7e2b3a56f3526c17c0c4824e12c1ab7d37`

```dockerfile
```

-	Layers:
	-	`sha256:99e6599a38fcf9f2d667ba57e5d59aa57d9e1dab58c95009c043a8466ab8736d`  
		Last Modified: Sat, 17 Aug 2024 04:35:08 GMT  
		Size: 2.2 MB (2227625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e79c529dfa5debd1b05763444aaba1315ce57ad69b39c0a6685dcd9cb31fb3`  
		Last Modified: Sat, 17 Aug 2024 04:35:07 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f63b8aaecd921fefbbc9975ac8544a1febd0aea2805613a288ea8a6232329d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234198349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d327e78391bf5c4434840167b01a7a780434c988eb4fa9be59bae74d499eb48f`
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
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a208ade4832b92e62af8529d920df794d6a75dba02564f50c6a1f6a9f56625`  
		Last Modified: Sat, 17 Aug 2024 03:16:39 GMT  
		Size: 199.7 MB (199734171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d52c2253adf84b42b06ef7bd959b69b556e048ed5877b940f5d60362f84c905a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067458ec1163e5f33689a0d768755900f7e9b5fdf59b29fa7c55f839ca15fdf4`

```dockerfile
```

-	Layers:
	-	`sha256:e574b3ed8e9e06e8ad732859f9166062421f2318b74235747d8eba355bb14489`  
		Last Modified: Sat, 17 Aug 2024 03:16:35 GMT  
		Size: 2.2 MB (2229915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b3449802d2f41874b6e9ffe6f98daead3c4ebf032cb9b5fcca2f7aa0774e40`  
		Last Modified: Sat, 17 Aug 2024 03:16:34 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
