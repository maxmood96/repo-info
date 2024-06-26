## `sapmachine:11-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:513e487824094a6e6fbf19350241a203ff2e4596297c0175261f685efeee8de1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:90be90e8df13fca69d5aaa9857a77307c59668db2bbed82c361e9bef9c86827d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229600612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966a848405ebcb00679d9248ae5082b8dcad558930f04115876e061624e11125`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c5c1a968523c18f120b2f504f269a276e72069109cfa926e9ae0395c95a0a`  
		Last Modified: Tue, 25 Jun 2024 22:58:56 GMT  
		Size: 199.9 MB (199895459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:16b398645163113c99f4f282bda1335dd0f3587ba9e6fbaf3d8cf735f1266e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25190040c6011b48dfc29a54df2517836a2e2bd6d7552e007c33f81ef2793e41`

```dockerfile
```

-	Layers:
	-	`sha256:e4c209b7614b940a54cca055e2db56b9b8f0afafb2804404af1b6dbc84b05a49`  
		Last Modified: Tue, 25 Jun 2024 22:58:53 GMT  
		Size: 2.2 MB (2201905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178b856a024b0fbb0785f619abef66d44cc49c1117fd5828c9e080c2c414e283`  
		Last Modified: Tue, 25 Jun 2024 22:58:53 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

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
