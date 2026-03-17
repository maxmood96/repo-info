## `sapmachine:jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:a8aa32d88a465ab81af1350d583a2eb956993507705158c302fa6327995921ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:89b25c7b2b3b58592fba5ed75793b6703d1b05f96fe1065c06bd640499430d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250015692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339acabe9aa1c17b694aebfed07a1d8eb6eee62513634ffad61d6f7ab7222e07`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:23:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d4761be313a06e0ee65741a8615e0eae6308a5cf9ffc27f5993ac0dddcdf81`  
		Last Modified: Tue, 17 Mar 2026 02:23:50 GMT  
		Size: 220.3 MB (220283699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38995914a570b944ab606bc4891564bd53ca1f2a21dc7407a06bca26b95a0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd8e91ca646860d4a7076d0db78ee2154e5ee51de61ad2cdb176af4837f217`

```dockerfile
```

-	Layers:
	-	`sha256:84706b0fed91c8422c9eba50af1df804efe95e9dd2b75aed820a023ab03ce446`  
		Last Modified: Tue, 17 Mar 2026 02:23:46 GMT  
		Size: 2.4 MB (2350601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfa090fc7fffdf764585ae79f972dedb41dfa1e6904cfa46cfaa31d001a0f8f`  
		Last Modified: Tue, 17 Mar 2026 02:23:46 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1b7a2494ebc822ac984a266f0afda5c64446c98eaa29bcb1aaf8f545d21eccec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246938166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52419c1a79a7a9f67bdae49154eac4fd80a0c2a4a22337bb8b8f77ba4c909547`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:29:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4484f55571509b2ce417ea79c2eb5f1dc3539432abdf24afdcd7c925c045146`  
		Last Modified: Tue, 17 Mar 2026 02:30:14 GMT  
		Size: 218.1 MB (218068457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c203990b96060f91d635cbeb0734fa22a2daeb2a229af7d9d695ab690a8b1a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6278c95f9050325f95562f7bef46fdc117b68e1d35533d95dfe61ac5d0b338c8`

```dockerfile
```

-	Layers:
	-	`sha256:1ef501179ce48fe07b9f946172cf55a54f725036e12a9d3540b6e90c66edb86a`  
		Last Modified: Tue, 17 Mar 2026 02:30:09 GMT  
		Size: 2.4 MB (2351189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5999f2a1fbb647e96c178e6822d8436481dd4e627f1af1fb8df35415745510`  
		Last Modified: Tue, 17 Mar 2026 02:30:09 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:682a9479bc7aaab42a0b6924695be673d79865b96fd72882985d5a5013829237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255277543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59ca537bc067866f477955f9ed2f1f050b1d9be0780baf59208af7c111b2829`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:33:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:33:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 09:33:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39a893174460dbcb40b0ed8906854fc759918cba397a75c45d8d9f9b5d40586`  
		Last Modified: Tue, 17 Mar 2026 09:34:01 GMT  
		Size: 221.0 MB (220967492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f40e979da33f877743584ae1c8d0a416f1ef42204605cc15269f35a70bcb163d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e145263c5ef384d4d919465535a6292f07539e4bae4df288d419737d8faa83`

```dockerfile
```

-	Layers:
	-	`sha256:7edecd1bfbd2c20f6bf0d30c1c75796f45c4ebea69f91164f6f9827d61cf0660`  
		Last Modified: Tue, 17 Mar 2026 09:33:56 GMT  
		Size: 2.3 MB (2347496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9eb2a914d1533623ba9f426c708edda7d4f0559207ad5a9d09969edf1ca647`  
		Last Modified: Tue, 17 Mar 2026 09:33:56 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json
