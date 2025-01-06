## `sapmachine:11-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:975bab8e46902a228b5e1969ba788d0a0702376266693d36fb2fb5a4eab8b87f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2d3fd70e642f8e19157700393779bb0c627f3ac187500c97b66be527104fec5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230989826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5d05ffe0b3b327da4e6995a9e72c082d4037f117ea009ceffab2496a7cd893`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef724932d71ea48dc040303276ee799bafb5f05bf9326603847899207fd470d`  
		Last Modified: Tue, 03 Dec 2024 02:37:07 GMT  
		Size: 201.2 MB (201237858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a55a3289e281353bae990a46db5874e0493fc857a84ebb107332f8ee782ed163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb21a32d694f94da91576712dd77cb1a70a3a2061cd3cfedeca55eb35f885d`

```dockerfile
```

-	Layers:
	-	`sha256:320fa2b8b0fecbdb5d9138f1003cc8fb3c135cef942304314f59efb934628e80`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 2.5 MB (2482642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e7d3b9cec1d9a299e0fe2f7b918176c4df418cb0bfd6d6adbb7c192b3c681e`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d7a32c7eb5215040907aaac50db1fd772786a84cead8a4069357062d28d4fb93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228632730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6071ea41afe0270c8949de235fd9e64b2e63d07d3c816892e638382e856219d6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c1e225a913ec2eeb1f563db61d2e8f6c905a25f48821442ea495e8b67dc6a`  
		Last Modified: Tue, 03 Dec 2024 10:55:27 GMT  
		Size: 199.7 MB (199740059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68cd790951c9dc403421cc2c4b1dc07bb315961a669dc7df162f631c36163ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ae0f54ced627643ecc81def9482b0705c154b982bd91e36aef0edb6dfc23b`

```dockerfile
```

-	Layers:
	-	`sha256:4b62e3b781b1551537a26a397a8117f15822a6003ae63f4a7e0d4d7afd4f0db6`  
		Last Modified: Tue, 03 Dec 2024 10:55:23 GMT  
		Size: 2.5 MB (2483833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b42dafe1bd8cadcca48f9315929c6d24cb4390a63c06a667e3885a0d81c493`  
		Last Modified: Tue, 03 Dec 2024 10:55:22 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:78739e5398360ed040c9751a897b8370bc3e1cbb5bb41756ddb30a01025dd10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222412804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3f1653114973468cc0a6a338b382c7faa367071471906aa6e74cd0199d908f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0054bdc255dc1b06b8b1161447179fa9c23f8df02f78bc2fe0b702ac092d803e`  
		Size: 188.0 MB (188023984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:535faf7508ba64b639a5342cc19806437a53014408a96efedc57ff8b48a078e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe9921119a1943f940e3637b3b5cea85e1e61a2ed86619c50070965d4df929`

```dockerfile
```

-	Layers:
	-	`sha256:efda7aabff8f0e2bc23e91706f2e11e922b8e0d97ca09f6b6d9bc3df5c0d3027`  
		Last Modified: Tue, 03 Dec 2024 08:45:37 GMT  
		Size: 2.5 MB (2484053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9a75ab5b49a3c9e34a4cd6cd9f2f04bea3bc96e42fa8f4262086cd2fbf472f`  
		Last Modified: Tue, 03 Dec 2024 08:45:37 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json
