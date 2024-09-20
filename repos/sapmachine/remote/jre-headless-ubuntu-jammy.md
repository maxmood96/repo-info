## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ab2b053463e99ea4d0788280abf2dada461928ccfd61c44100c435f362fa223b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b95883194b2ed19de13defc11969afd32e6fa1122fb3dce6a7e903700d2047da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87688847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2e7f7cda065a1024487b1a76d5519d64bc2ac222068f93c5f2784d1fd27836`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfabcda7f2f85769521b31c3b3bd97b09f36aa195c670c4216e12d95513c30a`  
		Last Modified: Fri, 20 Sep 2024 16:57:44 GMT  
		Size: 58.2 MB (58153159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a68843acd666ec39102f01e753f2f294febe0741977ebb25bf5c3b5ce1efdd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e42e78a1624ddf931d6bece80c0714a1df231ecc517e4750cfd411a345b4142`

```dockerfile
```

-	Layers:
	-	`sha256:631cd4e7522fe9757200eae312fa1f9521238354ff44583c2fdca5cab0d05b94`  
		Last Modified: Fri, 20 Sep 2024 16:57:43 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434b1b2fd667aa76b42b78ca3800954ca5a885675caad78f743b16633f4bbc33`  
		Last Modified: Fri, 20 Sep 2024 16:57:43 GMT  
		Size: 8.6 KB (8632 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e3188686569248faccef98d6e28f1c331769e0a0d3607a07594aecca550971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84512085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f53e61387567074b44b5b521a60421888ce3546b4fad120fb0c92b0c8f5d4d1`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde0c457134ca42a5fffba719db2f7000d5cb3e3e933e2244db0b9f5f8c9c70`  
		Last Modified: Fri, 20 Sep 2024 17:09:26 GMT  
		Size: 57.2 MB (57153756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73ab9b2df6dc064f32ebe50f3088c4006afcb487db1929775a6c129e5bd10367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c98c737100773b43a1368c05f4b5cff2c7bdd1bf3edcd1b5e84b746ccfd332`

```dockerfile
```

-	Layers:
	-	`sha256:917ec2822ef020cd3bb134c737b58c8b22ee604276f06ba9c398c3d700829faa`  
		Last Modified: Fri, 20 Sep 2024 17:09:25 GMT  
		Size: 2.1 MB (2147086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93303a58f0389bd98f1f0b4347414cd36ec9d53d30fd7292779469b410c6d01d`  
		Last Modified: Fri, 20 Sep 2024 17:09:24 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ecb4be3dcca20f7585997fb30c72d09021ec5ca6d4fb71d5bac2dd54aebf8384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93809009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8199a7d09735cb7615fa888a7ead6ef6e3e85d1ce18cd60c30777151efdbef`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781872cf291d08e501ca64c70de4383618ac845d2d5abac045685de0926994e5`  
		Last Modified: Fri, 20 Sep 2024 17:12:34 GMT  
		Size: 59.4 MB (59360767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8056233e5006d002043ed02ac2b0aab2334139f5f23186ec68eac421c6a3c99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2159996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c918ba6a24c2971a6d3dbf9eb51dc6379997e6003d86155b0edb9ac6c7c11f29`

```dockerfile
```

-	Layers:
	-	`sha256:dd49027485e82ead564456016a43f6b83af3833fc56667a2daf2beb93ce317f8`  
		Last Modified: Fri, 20 Sep 2024 17:12:32 GMT  
		Size: 2.2 MB (2151325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a73ed904ba19ad19eb224a3983aa085a7ba65198a770b4e0a1288b9965287b`  
		Last Modified: Fri, 20 Sep 2024 17:12:31 GMT  
		Size: 8.7 KB (8671 bytes)  
		MIME: application/vnd.in-toto+json
