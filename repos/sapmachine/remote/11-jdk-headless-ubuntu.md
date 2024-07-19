## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:5da1a89e7e27f9dd65e6d76cbb217389d052d407bed4a0b042001492ea08519e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:cb82f9a3a01569cdc09c6e1b01c27acf6148e58c94e424bcf78c034803e3bdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229631815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9c50ca3c2cebef3d39510fe82f72809c9e79fbddd2a59d4273d2dec5f9012c`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e9a650c69d27d7b2bae8a605c0cfe381c17402736f78797be2fa9f736276d05a`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 199.9 MB (199926662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c120904a07933e1bfc42f4470836f73fb7ebc0311ab8812fd0f60f8304238a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2234445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e89cb6252316fccaeb886689927c3ceb8599bd845e98fb9e55c461a9f4ad3f3`

```dockerfile
```

-	Layers:
	-	`sha256:d3aba3f0ddf93887cb299f722aa1aa60c8ba4e08e48d8b2839beceedf538f923`  
		Last Modified: Fri, 19 Jul 2024 18:00:34 GMT  
		Size: 2.2 MB (2225080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6407bbaac27628a541135c3683f29b813397ef1f4519040eba34927ae7c93f6e`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f39f8c5f44058262de6a2998bb93bb71ded5688eb87f101bee007486c018f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227242380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653474ea0f1048ba8aab9ff5ffecad77d412fb5d57c50835c716918ee4ea19f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054a9f1449a348f95f606692443fa8da5e797bf978a468860e317c369a42124f`  
		Last Modified: Wed, 26 Jun 2024 00:28:44 GMT  
		Size: 198.4 MB (198399337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:201852951f8eb076f58b8ad6a0e541aa286777ca8cfcb7d09daaf7c171609292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e98fb0e563b6a86e12c69dd676838855a0814a8de086835cb8a5aea4698603b`

```dockerfile
```

-	Layers:
	-	`sha256:e7f5295e0c46a554740c973c5e481228d6a70470e59ab28e9b4e06eb04bf60e8`  
		Last Modified: Wed, 26 Jun 2024 00:28:40 GMT  
		Size: 2.2 MB (2203015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc034c30f2b4e1285c4a3aae9e7c9b1384b35c3b8de24c6ac481c6e445913f4d`  
		Last Modified: Wed, 26 Jun 2024 00:28:40 GMT  
		Size: 9.7 KB (9708 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8580ce2b72fb2d4d501f8abda02b93f9b6f0c1410ac656743028b13f1d35940f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220987425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4538f5f2ac23d4422e99b34c94c68f2449972acc380c367fa3974ca273fa205`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9c18452e22640b2c1ffecbf1935fcb3c7abbdee16cd44d7af404fbadb7ffa`  
		Last Modified: Wed, 26 Jun 2024 01:09:46 GMT  
		Size: 186.5 MB (186481396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:98e05110ce4fa66d7972d3a9026557ec142cea3c2678021984eb8d7d42504f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfe7939c20a6714207e1e2ef997886fe8fd84f1cf768d0120122053e29a8f0b`

```dockerfile
```

-	Layers:
	-	`sha256:c588b5d02274cf6bdc0c9b8a527f3f84964496670658843b4e20c0ac226469ce`  
		Last Modified: Wed, 26 Jun 2024 01:09:41 GMT  
		Size: 2.2 MB (2203217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19bbca9c2be68c618dfbf96a2ffb679a720c8a26c6977dcc8370057309d91744`  
		Last Modified: Wed, 26 Jun 2024 01:09:41 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json
