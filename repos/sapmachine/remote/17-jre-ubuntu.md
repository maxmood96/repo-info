## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:0286caf89929e8898e779ccc642aa7fb5976673b073c8eb5c6183026a1d3aa52
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
$ docker pull sapmachine@sha256:14974df998262eab85ce1c6fa9cf1ae67634728e23cbc0e3a8bb137662da3e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84051734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783acd573b9e91c3f32054aa4b91d2916d2ec0cd67fe1503dbac8442f7d9c3ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c252b9a0588232307ad7bd37b60129717c337cade298f1b0e33bd77d202ea7`  
		Last Modified: Wed, 22 Oct 2025 06:30:57 GMT  
		Size: 54.3 MB (54328587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b3069793756606a698f7c11d3ff5f2512e9717a4ed98fc7efd0881d2b22ddb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cbfe92efab8906b501e23df3686f72ff2bb659019ff32206cc6a11a3a58f1e`

```dockerfile
```

-	Layers:
	-	`sha256:15115500be4f79a55824c26d4846fe0cd8598c9bd32925bee208a482dafac299`  
		Last Modified: Wed, 22 Oct 2025 06:07:14 GMT  
		Size: 2.5 MB (2517386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5314dc956a0d498bdd615eee2878195394c295d43a3e706a048fe67646fb890`  
		Last Modified: Wed, 22 Oct 2025 06:07:15 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ac6688a5722734dad837bab807ae435815f8adbd8d334f11b0602e8e62b4fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82613915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba0b899166773f77fcdda7bbd21682f45ee6b409962e13042b15876fb9002c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d959f781f10824b759c75f1511117016240a20421a092e598becba437b62dfcd`  
		Last Modified: Wed, 22 Oct 2025 00:06:32 GMT  
		Size: 53.8 MB (53752203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5afc66ccabb2e88f04906a4fdfc77dffda9e14c5f724fcef5b7df0f4e06c405b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f896d435de878c311b4e3c26e285ca0edacb041cae0e1851bebd1757f3cc1d99`

```dockerfile
```

-	Layers:
	-	`sha256:837c159fdf8cebab06d643976010f065ee191bd902fe220c20d951632918474f`  
		Last Modified: Wed, 22 Oct 2025 03:05:16 GMT  
		Size: 2.5 MB (2517902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263ba7dc08cee7e491e1af893f9e0355673f43a32806395c9b0a226b7a93eb07`  
		Last Modified: Wed, 22 Oct 2025 03:05:17 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:50cfcef9a7d7f16e4ec3d770eac7ebc07c437b95de128a614adcc4d751eb528f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89827538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05420d9b74985a5e90649b2a246db66409b5a8a0c80c9377c6318e428d554562`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c31e892056db5c7f73e93319c77cca109b1d17fdb9f129ac1761d3ab894ba`  
		Last Modified: Wed, 22 Oct 2025 12:07:28 GMT  
		Size: 55.5 MB (55524013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c979a05f7d17f2d8ef8675ca3e0eb107800df500f5fb24fdacc3bbf747c2c8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836c13af90a29363112c7fda308694fedf60f4957f83ac8c2f498b6ddf4da8c`

```dockerfile
```

-	Layers:
	-	`sha256:dd65dc93f78f84f34958fed07ae7746d3fa6ee4cd54fc6d598fa2682eaf76811`  
		Last Modified: Wed, 22 Oct 2025 15:05:20 GMT  
		Size: 2.5 MB (2515467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b98cad491585d6432895327dd76710b2c32bd5f068c691445ebde76d5e7e652`  
		Last Modified: Wed, 22 Oct 2025 15:05:21 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json
