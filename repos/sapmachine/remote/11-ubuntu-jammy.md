## `sapmachine:11-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:5e57e5acce16dec59f663cd488197e68d0aa40476e8d918698b72fb5389c7bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4d32cff00fd4d48a6501c679367c804275922a2a3c7849ff4b7d5a837069a1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230377662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dada30895bae73961397d95252afeceffb7cc16d193f1fdd8431dfb01ea93429`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2651a3719d0900475970e0e12a1e9f906b8549e1736a2ed826bb758023cacfcf`  
		Last Modified: Wed, 16 Oct 2024 19:00:24 GMT  
		Size: 200.8 MB (200841974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:164b4f710bfc8b20563aa302db6b80021b27e0f236507e2377c3ac94b67e7665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355a2289a905fa5c758c730827d28596a828da5ca8a46de6ea99bb455c4b6b0b`

```dockerfile
```

-	Layers:
	-	`sha256:d45b6b242b10928d9e7a377f73d3f5e37531a0ddf10d995421aec1a537d352c7`  
		Last Modified: Wed, 08 Jan 2025 03:56:22 GMT  
		Size: 2.5 MB (2490433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a61f7d3bd7f1b766dd82ac7614bd866d72f90ce70edc9e94a2a43f456690a9`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:baf96c616849c4d1d23e96f65ef40142976b04a9bd31048aef3c3724bff9b91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226661032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302413e460202530b5f35e15c220dfe03a2c6ee89f0e8d56f9328056ed0b6a80`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 08 Jan 2025 03:54:57 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b2a88177d095ef2396a9cee65f9816b044c7caa52d8bc3f7501cedf944417`  
		Last Modified: Wed, 16 Oct 2024 19:46:44 GMT  
		Size: 199.3 MB (199302703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:754cd1e98709c3ed8351e45e4d59e2122ee81280d532fc3a000b31acf40bc2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278d38bda85a5e701967eb67967171fc887f1afdf34ff8a0c4a15b0103b95f79`

```dockerfile
```

-	Layers:
	-	`sha256:9252cc18cabe818a32c7698fc59b153695b1d426a1bba1b846338ee78ee056a7`  
		Size: 2.5 MB (2490789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4a001fb0ea2238b9b5ffc0228db5a45e098fccefa516bcc00914ccc97b042c`  
		Last Modified: Wed, 16 Oct 2024 19:46:39 GMT  
		Size: 10.1 KB (10067 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eb6f4ea76980071e74c6fd402f5e4430e5f9c7832dca71cf6aa88055240e2e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221963151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c3a5239dce2d2ace47e84771034d121ff564e229aeffd7e3a33dce6bd6b28f`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:029629869ec053e0e8ddb7cfcc02d6ffdfef6cb2fd820695dde658cb223e4f6e`  
		Last Modified: Wed, 16 Oct 2024 20:21:06 GMT  
		Size: 187.5 MB (187514909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b86feb17df871a240bb52a3bafeae13d3d342da52ae484d2dece174e983d5102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d9b56fa07ef907a427faeace746fddd6bdd9ffeca4bb3dd87ba45dd696bf5`

```dockerfile
```

-	Layers:
	-	`sha256:91a3f7357d394d064a5f0ce347a0bcba8057b12fc6e1fc70ef240d83b538e6fd`  
		Last Modified: Wed, 16 Oct 2024 20:21:00 GMT  
		Size: 2.5 MB (2491862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf816b13f55bf5c6ec5d2401df71d4e3c6fbf06495219b81c768ca08adc03ac8`  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.in-toto+json
