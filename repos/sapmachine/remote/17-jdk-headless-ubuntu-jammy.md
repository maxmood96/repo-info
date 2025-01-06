## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:608cd535f2e27d17d2253aba9053fd911cea2511547d4817a775fc90fbd73d7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4f2bdbc179c168c3207036940fff7cc28836070968410837f7be08f46125f3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228137603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa5acbe30cb180c4a941a88a3401019019d0deef159e782ce98640ca14094e`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cada231f23ad2e3e04bacb10d7b61446a17257d75c2a91daade48cfece16096b`  
		Last Modified: Wed, 16 Oct 2024 19:00:47 GMT  
		Size: 198.6 MB (198601915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e442f3c438e2799bfd65a7795acb1c9145256fc7f984cd4da75f9eab086d998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2b2b8419fe1b9b7a45bcbc537539a8148403c0f8deffaa604b15763af304eb`

```dockerfile
```

-	Layers:
	-	`sha256:9821d6403942702e394724fcb2ee02ae6ab566dad5fb189156a7ec2217795367`  
		Last Modified: Wed, 16 Oct 2024 19:00:43 GMT  
		Size: 2.2 MB (2234614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172a4d61e6adb94473007dee06fcf7a6dfa8c8e45f90553af25a45798dd0efd8`  
		Last Modified: Wed, 16 Oct 2024 19:00:42 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fdf82929d81292864a939ef00fa442763c5a25e02211f377022991a7cfee0a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224624367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0952522d1a71e7d82e2e601704cb5a509e5f898a76511ee7bb8993f8ea52fa49`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdb5639bebd39f71c146cae804892c7fba9e72e1dc9a0181e655f6f6b92220c`  
		Last Modified: Wed, 16 Oct 2024 19:34:28 GMT  
		Size: 197.3 MB (197266038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1c62406c7447d51a07024269b6cc24eacf2d1961ada54ba735496af94752456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a274106139501a7c32504cef2a90689c11583844f970953c435e9c6f64eb1e6`

```dockerfile
```

-	Layers:
	-	`sha256:58141c1bee0cc29a765e9e9745750034c09f497b4dc85a66f0ca84b69b8969b8`  
		Last Modified: Wed, 16 Oct 2024 19:34:22 GMT  
		Size: 2.2 MB (2234284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b076a54863aea6184785f3c8aed883bda98ef2833c369e01ca8d8c55654f902`  
		Last Modified: Wed, 16 Oct 2024 19:34:22 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:03be726115d8fa153cfbc46ebe53fba5d0d3be027ab27476cb47e33e2dcdd1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233948594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0261b43d3e35f2275ebc2f20bc600803642a1c95b8bc335c18a39ba1af04054`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f62a060e674753eaa25d24e1b95f0a2e8dec20c4a9f2fcd92a447c90be721a`  
		Last Modified: Wed, 16 Oct 2024 19:59:15 GMT  
		Size: 199.5 MB (199500352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df48a54e8176ee2ead34b8303c970e00d3742f5df2259e875e4460a3ff3852e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9252a4dca0d74c9f04e68b8d0cd73d4a31fc9512b411c64bb4b730346374ad`

```dockerfile
```

-	Layers:
	-	`sha256:0e6f8aaadab6049e19b36c42e5baf82c254d066a12be2990cbda17b3b3185ef7`  
		Size: 2.2 MB (2236574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2eca891462243b662cafbd2957bad8afb47da6d645787cd620b1e33289f16a8`  
		Last Modified: Wed, 16 Oct 2024 19:59:07 GMT  
		Size: 8.8 KB (8755 bytes)  
		MIME: application/vnd.in-toto+json
