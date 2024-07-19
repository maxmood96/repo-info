## `sapmachine:17-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:1c75cfc66abf70eae54a01b9081be789f8bbd7d770dab6b1a55a60f2d77c4249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:346da42a84a7f5a25dc14cc04184b35a7fe9bc7787dba9e33b3575ab4e5c20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230134900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50824a861e99603269fdc973d57db5c9885124630c444537acc84e3c712125ce`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c027fc52595e534c43532679a8ea4fc3b94b2e251ca581dd0e3e82c3ffd8003`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 200.4 MB (200429747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bdb69bde54aecbca4b3d670a09e2777426a097db876bbd646b1ad9df2a974c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e8da48f9e1a33f504fe1c077424b91211791915f87873f309231ddf1ff5534`

```dockerfile
```

-	Layers:
	-	`sha256:bf594421dcdbbdf056317c3601df6f283de18da9bd699a03be425546e757a94d`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 2.4 MB (2445162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44a9102536371cd38a129f65aa2af01480e40faa3f842cd5b4177696c485136`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 11.1 KB (11140 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:66fa71ad3f4083b85f615eb08f36fa44e5792d43aa4c03fefbb9444d45e43163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c553ab04d29ba95973f8f22fa71af492367d90a40ef63fed5f4b6193368427b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d0a14748c2231c2275e016585db28ee92592b045a28fbd4ced220e38cefecd`  
		Last Modified: Wed, 26 Jun 2024 00:14:55 GMT  
		Size: 198.9 MB (198938986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b1dea0c67ddcd37e5daa0dd8a35062a5563df2cc94343c3d0d09b339c96e2df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845e3d7345a033bd8a7282423b2b0faf169fc563443385e2924fc89dccf5d1a1`

```dockerfile
```

-	Layers:
	-	`sha256:836d882f1d1501eb7d291efdaddb953fc574d43211e1e82db4b46ea0c5f91551`  
		Last Modified: Wed, 26 Jun 2024 00:14:51 GMT  
		Size: 2.4 MB (2417013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd75d398153d878b584fcb1d5a6223c08d9280a5f15d48ee988797d16844de63`  
		Last Modified: Wed, 26 Jun 2024 00:14:51 GMT  
		Size: 11.6 KB (11555 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:59cba51c367f1373c4f1af3b4b0cc2de3a75b8458e556f917f02823fd155787d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236004405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ae808bcb7b7c1c897098470fc35f6103f1776c20c86615e3807746a66c66e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8333d5f5c97c563a6393613f47ed19183e8719dde97d5ae213be2cae721fde8`  
		Last Modified: Wed, 26 Jun 2024 00:47:22 GMT  
		Size: 201.5 MB (201498376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:165e2fae006e55091d6c8e9d6672a12098ad18cedc4e0d822585efad9b4ca88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc70d0d0890f846aff9497741c7e269dca2528b346d0e5a7b2fe385f01fb88e1`

```dockerfile
```

-	Layers:
	-	`sha256:2c9df0261694b5a94226908b5f5809519de83ef1713ae3d0a9c8802af87efac6`  
		Last Modified: Wed, 26 Jun 2024 00:47:17 GMT  
		Size: 2.4 MB (2418486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870ef5adb00d5ecaf47cd301faf1eb7a21f38c9c38dfb1057f7812ce0b9cfbd4`  
		Last Modified: Wed, 26 Jun 2024 00:47:17 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json
