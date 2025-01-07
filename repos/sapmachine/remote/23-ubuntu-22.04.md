## `sapmachine:23-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c8cb82101fbfd4d95b7e1f4da8017a2276c7322dac01525a656f5816baf04dba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8b09e2fb05f0f52ed44b2309d56bd212481ef788cd696038bf0de008a3a25703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251681165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c22a943b6936dd91394744dddaea17e55da1b8aaf6cae4b1ca5f6b6940cf50`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9218a0c2d867fff3f8c6b7d992564e41caa7c9660e020125cd2d5c3b44f0c4ca`  
		Last Modified: Wed, 16 Oct 2024 18:58:46 GMT  
		Size: 222.1 MB (222145477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:18c21b8daabbaf0bdce1ed45e43cedb7adf90154bb27dd9a389fe7b25a1ae24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70c190963cd60fa3a5958f8a5a803ce715839584fb76ab5cdf17a0c2a938ffe`

```dockerfile
```

-	Layers:
	-	`sha256:a638c49065f28bb04736e658b4485bdffae543927a76d333630c8d4c1b4455a3`  
		Last Modified: Wed, 16 Oct 2024 18:58:43 GMT  
		Size: 2.5 MB (2482967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2e21879bdbb529a717ea14b1951979249a99b307e65898cdffd96bcf6a39f8`  
		Last Modified: Wed, 16 Oct 2024 18:58:43 GMT  
		Size: 11.2 KB (11196 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:22bbebace39f2a521f738b024eba1fc3887cd7b9cdeed2801296ed53572be3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247435990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb896dacdfce481cfd85481f8485b797b09d1f791921164a440aff817c994c40`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745133c340c2df38a99e9dddf5411d318df0612ad0416c5433dd281cf755764`  
		Last Modified: Wed, 16 Oct 2024 19:04:03 GMT  
		Size: 220.1 MB (220077661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2af920e114aa145fdbe809864caddda4d1ed2acdced478602b23532ba68802ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2493503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dd5cb6385ddad2be5bcb578530e3c681610dcec231f9cf2d5419f070cca29a`

```dockerfile
```

-	Layers:
	-	`sha256:e93538fdef612d02b15b3454a98a09a70c6b7f8d25b32637430233a4b6c210d6`  
		Last Modified: Wed, 16 Oct 2024 19:03:59 GMT  
		Size: 2.5 MB (2482112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ab629a39e25fe5fe94873fece223e441f6d0e0706313cee2e67a1a2df95a37`  
		Last Modified: Wed, 16 Oct 2024 19:03:58 GMT  
		Size: 11.4 KB (11391 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d1069159c1b839568fb3225060c1fa896a280f480e717151f27aef7cd8d98f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257615458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8675fe54b712eaff60fb7697abe50c5cf5ad79612f2b95632af31f7c9c423b44`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd47a767d057fdb0977f5afc5777236bb758f8129b069f207e665472cf49abb`  
		Size: 223.2 MB (223167216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b46d2aeeb1a239b21093c86bb9a791ccece39646782f44578d3efcc67e0f49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92dfd6ee5698a4d6ccb92ccb5f4c8a5588ff1cc606ec5ab5bace5dc968a48b5`

```dockerfile
```

-	Layers:
	-	`sha256:93f99b49136006b7492f68ae248d25d1022e693400997c00574c2a26e2ed9668`  
		Last Modified: Wed, 16 Oct 2024 19:08:01 GMT  
		Size: 2.5 MB (2484426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f041d9faaaf82c40f11efb8d036d0680bdeadbbc067ae8c9528fd24bc75594dd`  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json
