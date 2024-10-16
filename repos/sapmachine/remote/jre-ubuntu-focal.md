## `sapmachine:jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:42a52f9d5884a6ca75dda6c184d5ddd289b7ef961ce87811f509d918d11228dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf44f4a636f3062e530f580b9ca2b9e3a78c74d0af2a3dde88fd6e712412faac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86427636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a1b94ffb2565a7615947f798caba0a814bb1723de3eb0cd907249e83cdbaee`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5569aa27de0ecea51c65eda59b86b6ca1fdbd384517fa1e319131f6c6ea50734`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 58.9 MB (58916576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb83c4f188a1ff9e7e4c654e96c30f49d0a8bfee15dcaa3e6e0e9d421c75cae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275bc75ab06d5bcee215c7577faeb0e696ee2d0068d76a4dc9d2230dbb738631`

```dockerfile
```

-	Layers:
	-	`sha256:22038438614b18f5ac9cd8fc8ec13f3468f05aa60272043f261b4fba85f23d41`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 2.3 MB (2282785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbe274496cd375218df82979716df2ac36555eb911e910934e0c607185b2ee5`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 8.6 KB (8558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:de62cff0635e011eeba79d0ddcb58ac2b8825c81b748cc68d4076abe0737b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83922237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34741e2970cd5d0b2711d4eff8eb7e14faf2a2c035eaec3c299c2caee3d1f77f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d59e06a55dffb9212527c261b0f3211a32f289cfb7a4b18ae93e5ccaddb1514`  
		Last Modified: Wed, 16 Oct 2024 04:26:30 GMT  
		Size: 57.9 MB (57948409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38bc26194b70a678c8b4f6db5d4d951f11d2b8636458ddc5a8f834688bf5e48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12107d9f2829486b22c6aa6e773802b5f50ff0cd62e5d38722dd24f9104f545`

```dockerfile
```

-	Layers:
	-	`sha256:8ff95d8d3f430a3bf741a5ba242421fbd916e979968cf11a75ace281618a8fc1`  
		Last Modified: Wed, 16 Oct 2024 04:26:29 GMT  
		Size: 2.3 MB (2281790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d5a08daf41b88aba46756122b710727fd682bf7c58c072d56262b9279a13df`  
		Last Modified: Wed, 16 Oct 2024 04:26:29 GMT  
		Size: 8.7 KB (8658 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9773d6c4bf95f2b2b35344a9ae139664145b94406959abd880e08a430f844c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafb46af27b50a41f4e52eca27ee86af75505b6d1ee5023c2c8c0ad317451b6e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25606175b5e5d0bc0b8f5439a9adbff7ffa4a10d62cf690e72708416db2dce30`  
		Last Modified: Wed, 16 Oct 2024 02:42:27 GMT  
		Size: 59.9 MB (59935155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb94b63c1c1c1b0177d4ee4b7fca2b24240d8a83c783015afcb9067500ed3e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a2b33be6fa512bba1600cba9d6a966930bf71da6fe34267812bbd74838204e`

```dockerfile
```

-	Layers:
	-	`sha256:03969e2e46b1bebb0f42783447ccaf83a2dec4e29c88b2beb507c506fe47bf52`  
		Last Modified: Wed, 16 Oct 2024 02:42:25 GMT  
		Size: 2.3 MB (2285919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35bee08846e184628488f646edc1b2bb8d3b9b4f6072a8b5ff9d0e48ce2f46cd`  
		Last Modified: Wed, 16 Oct 2024 02:42:25 GMT  
		Size: 8.6 KB (8598 bytes)  
		MIME: application/vnd.in-toto+json
