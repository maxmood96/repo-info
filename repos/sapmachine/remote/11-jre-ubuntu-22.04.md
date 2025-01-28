## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c7dbc59810667a1a14893017a0aa27f44f302576e2f2de2275c5b265208ce440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:567ab704109ca9714af0dad1d5504aa22c15ff6f6917145393e096a95f43fd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79518955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309021d43feee7b632ee356e159d056bf44ad95599291972a6172719e331c65`
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
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f125e72f863c6c0392fae7689ceb6ca4e5b80ec9fe9f37a44b66e2c0f05dac99`  
		Last Modified: Tue, 28 Jan 2025 01:29:08 GMT  
		Size: 50.0 MB (49983267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a43d323908a3e9ace83036ff06da4787e9944fbd9c678a742866c9eaa9731604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532e562e11d1f8058433f295fb8377fd6e8bfdfb0f2a4d1aed188e89bed3a8ae`

```dockerfile
```

-	Layers:
	-	`sha256:c43895d3d08696da2d376066bf37b4f3ac6ea23235f296a4253644e13fbecdd5`  
		Last Modified: Tue, 28 Jan 2025 01:29:07 GMT  
		Size: 2.4 MB (2413354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72dbfffd247bc04b15bd6a5601adcba0d223a2c995efeb23f65e863f802af059`  
		Last Modified: Tue, 28 Jan 2025 01:29:07 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1285c90858d95adf7b3c5e9ec1d26dd78b596e41ffdbb4addffbaa7f4b47895f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76631169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fa609eeacaf738e1cb9fcd0eb640fb8d256fdee8c71c267726f4c0198773a4`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a09d4d28cee43da3fd4e73788702a289288266433684e3b888210585845d`  
		Last Modified: Wed, 16 Oct 2024 19:48:52 GMT  
		Size: 49.3 MB (49272840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7270967663217ca47a4507cf70ef03b685f7538c986003296c6ad4119d214209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a79fdb05ee89733027fbe473c68ffeeccdbfd7244d89fc5e6cb8b339457c2ff`

```dockerfile
```

-	Layers:
	-	`sha256:04514e14dd439194c41852ef9080a30b8c2144059faae4aef8c10823975227a0`  
		Last Modified: Wed, 16 Oct 2024 19:48:50 GMT  
		Size: 2.4 MB (2399883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a7446c95a7409a7186b1047d3608f440a753031615c5f63aaa23ab9a5d796c`  
		Last Modified: Wed, 16 Oct 2024 19:48:50 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:95a687d84d8c0bddb25b6c740db70053211bdaff6986760753efc79d8ddc847c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83073384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a056cb468dc343e11082fe5ce67ed2a5539d69be9489291180ffdb7e9de870bd`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e7672e573cb87deb788ce9c604a40e17e00fb8483c5017b321bfadced6360`  
		Last Modified: Wed, 16 Oct 2024 20:24:58 GMT  
		Size: 48.6 MB (48625142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce7f7807ede1e69e71c480038226c954995d4987018d46fd73bd763b4577a3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00804117b41769d36f35491d9b618a8db9f4d6118126fef9cccbccff6cff381a`

```dockerfile
```

-	Layers:
	-	`sha256:3a16aa52083d589f35dbec7a27bf55023239cbb2a8a88cac09076a3d672ca28c`  
		Last Modified: Wed, 16 Oct 2024 20:24:57 GMT  
		Size: 2.4 MB (2403560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82691aa17144d8bf4713c9b95206ceb8341b8f9db911503dc1773d08f791ac9b`  
		Last Modified: Wed, 16 Oct 2024 20:24:57 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
