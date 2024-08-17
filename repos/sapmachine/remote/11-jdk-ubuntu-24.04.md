## `sapmachine:11-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e9131f0a2fdd171dda056157aebbf5ecb072f604ab227a7d8d053a06260aa9b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bd4360227c0ae82675cd886c2142fb33741769b93fef72db731e202c0ee5d017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230823676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad36a13705f2653e4cdc2679d85c4faeee5aadc0642283293062362e7b9a2b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15394dc155969a70dad5e8d723729787d6852b2618ff7fb938880de7f91f7a48`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 201.1 MB (201118523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5af64ddb8d120bea04a601c5d94f731429ffc79f270cfe8ba733857a5b062722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f762608afea6f4e07b56d5634c7b1f7c4b9d76d51cc1d9d3365337b1fd56e9`

```dockerfile
```

-	Layers:
	-	`sha256:13c6720c555c00bdde2a2f64178e18b5de021b81b19cd5909dc302a9f45dd0fb`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 2.5 MB (2463097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648ee194b973c91e403d75e3028a1ffbd1cae6bb00330583653263f61cee086e`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5906dc40d06830c3a62767ad51c81aa3b9f40e866c2538aeae5de5c14cbdc63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228477065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3f87e9fb391150775be63607310126585d1926fc826af8e7425e19307415e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02e890f0fd1326e4b918f09a6c4c2a4fe656fa945bdcb8f6f480bef7476b4f9`  
		Last Modified: Sat, 17 Aug 2024 04:41:49 GMT  
		Size: 199.6 MB (199633379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe6eb38c6b0fb3cb434416e0821adc3ad008b11d09dafad1739a54448edee36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20f672bac2781f8112f932936aea02f34295656da97d5823d06c3eb00810ebe`

```dockerfile
```

-	Layers:
	-	`sha256:9004bfbd53d34d2e9ba4cbc44c3eb15aafe2c46d8220f06e6cbd6e73b9cd90c2`  
		Last Modified: Sat, 17 Aug 2024 04:41:45 GMT  
		Size: 2.5 MB (2464288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a45245a130372ef2d52dc8a83246fcc66e2016408a292fd494cf539cea39a2a`  
		Last Modified: Sat, 17 Aug 2024 04:41:45 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3db38fe94e144abe0b2a617cbfa57c775cefecf4e8d4b07db87ff5bd74167356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222410374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce123e1d1a694007b50cdd4265c13f390eea1f78e4c725a37f6970a3463d279`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
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
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6269c65182f2d03a0e18d6c24919636d1d9b1868e06404fabcfd613f878677e`  
		Last Modified: Sat, 17 Aug 2024 03:27:50 GMT  
		Size: 187.9 MB (187902802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05cce6ed22ddb09ca33f9208beba0755f74544f54c8ed58a5b7fba1c33a9441d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3418c82b5ae34227d05f661f6ddb7d413a36964d9b7a606649355f87272d3`

```dockerfile
```

-	Layers:
	-	`sha256:e4baad5864574f18f2f6d34071ddb00597d59d670efd4cf5d5a595a5db781b55`  
		Last Modified: Sat, 17 Aug 2024 03:27:46 GMT  
		Size: 2.5 MB (2464508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fe1b0d819fdb9dcbe4e026760900792c24e415e39fee7239a3d35ce2754780`  
		Last Modified: Sat, 17 Aug 2024 03:27:45 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json
