## `sapmachine:11-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:83bbfb05edc0c6fd0f752f1dbdeeef69cf234c38a371e69a58bccabbacd20e8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:28006515858b55e965e28fc817f1cb70b2fe217a893df906d6b9658c2dc44c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77013603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be52eb7bfda26482f9e0fb45f6ec244c8cea1c60aea99434095705159a244f98`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa7cf78dccff63f694f32b8c64deef782e1a165640d67a6aca07e237c814e2d`  
		Last Modified: Wed, 02 Oct 2024 02:00:13 GMT  
		Size: 49.5 MB (49502551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:460e8fd1a4d0073a6c97c3713fa879cc80d4e9a672476a3d227e7f465fc600b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1c75fc500b75dcc5a5ac0c7d464961b6ff36449925cd7a19efab7da0ef84b2`

```dockerfile
```

-	Layers:
	-	`sha256:e6978112164df1d45ab943f8d4ebf751959f4b1f047e1462d85821723a187336`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 2.3 MB (2291720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a8847e5b3bd113c7f87973c4ef898bd056fd998c0b2b1585fbda337b3fe7ae`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dc431abf863a4109465745f23564954b2097d43af4066d6a60e7b2b56125ff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b53f4477bc4c80c3a58bfe1a391715904f378c3d6ee888b55636a30766775`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe92357d250ed68e5f1c160bb94fb845f903609506b8f292722fc4bf1bff8e52`  
		Last Modified: Wed, 16 Oct 2024 04:53:43 GMT  
		Size: 48.8 MB (48817435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c356248ddc3c53aa50a9662cd26fed7e48cb7447ab4dcd770360a294a918a081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1078101a3be976a5f9762d6485c72719db5169228d39595194f8f32dbf2f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:2b7ef52c2e994438719ba3de2b4a6007399c3053f3aeb101390ab2c7451122e9`  
		Last Modified: Wed, 16 Oct 2024 04:53:42 GMT  
		Size: 2.3 MB (2291984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c78552edbae7b12e90305b0b91924537b13f795f58896692c99fbddfd49520b`  
		Last Modified: Wed, 16 Oct 2024 04:53:41 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:87c7cf2416dddb42f085743cfddc93439972a2ec9da0b16204f3e51b00b49727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79822287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a91f7a1c8afdf0dfece02980c773b4d17cc2ed61082a448a28852e83bdbe5b0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3c1857af0e4f94b33431b7869903688788599c86a75eb04120368fc9d5c9c`  
		Last Modified: Wed, 16 Oct 2024 06:18:47 GMT  
		Size: 47.7 MB (47745781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d5ae1046235d9090df1059829a22ce06482f85cf451089606d49c839f96ea75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a51b0f096fd0c5e7112913e8954b6ab40adf4b71ac13fbe69779889c45a633b`

```dockerfile
```

-	Layers:
	-	`sha256:c0d77733d7f7156cfd2f7788a2c8587afbf0b62dd92a4c841d63a27e3c2daaf5`  
		Last Modified: Wed, 16 Oct 2024 06:18:46 GMT  
		Size: 2.3 MB (2295491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d836ab09d219baa22fcbfe05ecb7ce647d35650a19cd293a9c71b9bdfddb0695`  
		Last Modified: Wed, 16 Oct 2024 06:18:45 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
