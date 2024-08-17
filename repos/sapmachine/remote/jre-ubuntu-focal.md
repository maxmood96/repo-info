## `sapmachine:jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d2e399f65d362cd0fe1e605ded07dbdd00558baf2b5724830b9a5ebbd057a47a
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
$ docker pull sapmachine@sha256:9bf65ccd2f73b3d9b24e0c60d4006e18f4d2fa7dcdb95c78825354411ba6c09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86190040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0cbf1708838236063765d0d3141d75c0a2e4d7bd80d93a7380003ebee6de8d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa608482e9b49d069707f28904293cf55e7ff2c3db9e929445cfcc51ad2de3dd`  
		Last Modified: Sat, 17 Aug 2024 02:02:24 GMT  
		Size: 58.7 MB (58678271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a94f08fa3876fb7f614004a589bb6128c4f276dbd12df24aacc61b1ffddecf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f412974b14206f3358a4c37ba4fac88d5e207971c2135d79af645959217ca67e`

```dockerfile
```

-	Layers:
	-	`sha256:fe7dec9286c49c944a2f70f10f68ce515253008b740d901e686243a712db2f81`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 2.3 MB (2282819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d070e74565971993b85d5539e1ad8e84cb299375d3110023d122b5cf54a20769`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4c9e528b62620ec723f23341869895d332708fcc630b1bb5255833f4eac34550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83688039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90dd090d0a6fe7cd8b97d5c2d0bf3567ae761686987d5c79d0e89cf1daef6dd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2a1034fb1002bbfa247f1043bbdb90a4bb4e34dd71ac4f1e07361cb1ea07d`  
		Last Modified: Sat, 17 Aug 2024 04:14:08 GMT  
		Size: 57.7 MB (57713822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6a3987b952e93feebfcc3ea13f4e0f14841f6de24a9bf9e41667d6b186a7359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bcbf945df5be5bf19d395ed1f6ae989ebdd5b55098990e0a03f480a2f82650`

```dockerfile
```

-	Layers:
	-	`sha256:de3ca1c5dd82a054c7526606f9841b5769e46432ace0dcfd3be28409bfcea6de`  
		Last Modified: Sat, 17 Aug 2024 04:14:07 GMT  
		Size: 2.3 MB (2281848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33be3b28fa8c2d857b6a371edec372c85fc601120d53893e3f4498e3a02b921d`  
		Last Modified: Sat, 17 Aug 2024 04:14:06 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d897101fe5ebca7984d4da46623371794d9395a8dec7069be9aef521fd19bd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91811714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9359f84e580eb005bd0f4c2f3f499935863179e629e973ddf931bc5d766204`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd436b70515d0cbfc122f405654d3e7e4607a23f397fdbadc8706d157b3ff17b`  
		Last Modified: Sat, 17 Aug 2024 02:43:15 GMT  
		Size: 59.7 MB (59734574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c9dceefb6a244fff87d9a134d07e5a57842ab1847d3c08c98b50feacf0f729d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbb5b36de96a8d29e0e738bc633c1437fc58f8f15971b68fffded2a484c21b3`

```dockerfile
```

-	Layers:
	-	`sha256:499721077f23b845ec26d1bcce0fae95aaccae119c403c8dec48aa778cd9f5d0`  
		Last Modified: Sat, 17 Aug 2024 02:43:13 GMT  
		Size: 2.3 MB (2285965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbfaae848e02d449db86f60b18d93878071b15de41cbd267051209c9e6f5d76d`  
		Last Modified: Sat, 17 Aug 2024 02:43:13 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
