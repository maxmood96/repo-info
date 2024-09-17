## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:180267ec57f9cb4525d86bb1d6efbb6bf3fd783a72775e5b8bdcb35bbbcd9670
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c3df5a4aa4a9c7a310cce9ffc40550193d862176964f84fbc8594b0db37a5107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241536855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37ad252b7dfa0dc3e072edf3df7f58027f4f1656e945b53e3dc732d3687ad32`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eea03cf948350c52c49b527dd3ce7188fb209792dc9f97f3000957ed23b20a`  
		Last Modified: Tue, 17 Sep 2024 01:00:55 GMT  
		Size: 212.0 MB (212001167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:779e9b584a343802993c78d7f8d5c1e7ee6b2adb96f1f04a966a9c97fe9df8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8cbaabc048bb7871792e692d5caa8af3626c289ccc6150cb79d8992c4ae53c`

```dockerfile
```

-	Layers:
	-	`sha256:20a48471ed615bcfb05101ca099fb1c014b6d14bf87396e2e5d0a3a46b257049`  
		Last Modified: Tue, 17 Sep 2024 01:00:52 GMT  
		Size: 2.2 MB (2231771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b3acbe101d79bcc6c683dcae2641bcbcc41dd1dffac4d84a48872f3824c0813`  
		Last Modified: Tue, 17 Sep 2024 01:00:52 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ae7d6f0711e502942b1b226532626a8c2a8f5eb5b144811bd56ecfa929d5cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237319005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4faa676c7d73fe5805eeeee38beeda826c7d3039076d251107116432d406da`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6cde4c71f7a673ab36df135038f6b6a4fc7b04216cd161b043978e0f084cb0`  
		Last Modified: Sat, 17 Aug 2024 04:09:12 GMT  
		Size: 210.0 MB (209960322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:778aaf0b9d905013b7b5f6494a4cdecb856a2409d50f0e15b2295760a6bf305a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439aee54f689b7d1f4dc040f31693425586dc047c88ea50da9f9a261a36bd609`

```dockerfile
```

-	Layers:
	-	`sha256:c96ba340c6308b4ee5c92dab159e011ebb4ec4199ee95b524b3e934b547aca82`  
		Last Modified: Sat, 17 Aug 2024 04:09:07 GMT  
		Size: 2.2 MB (2230834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039f42d5f943243d6a695830bf4903cb7aa8c640f13ca2a8510c82a2d43ef909`  
		Last Modified: Sat, 17 Aug 2024 04:09:07 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1c3c693e21f557d51a8efda90814f738279927c12db917080878ce91b4d8a1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247365771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ecd6b6b83c6f4bc5f68aaccba21d1569121cabd814e2025ff8cbcc4db59db`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696085a4e0c8f4b6082bbc2f079a3b98c734fe288e72f4da7bc5a048ad6f80de`  
		Last Modified: Tue, 17 Sep 2024 02:25:36 GMT  
		Size: 212.9 MB (212917529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:821dc1bd250ad9c7efabdad59fa0cd213e03ae3e4afa8cbc69557997dc47c2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa1574b22e5b0dfefa12f30671466129df66a5a4a21a13112b2e64ed592cd82`

```dockerfile
```

-	Layers:
	-	`sha256:549dc195695f18d64acb177da798a6edac954f041c611e21a22714436019e7ee`  
		Last Modified: Tue, 17 Sep 2024 02:25:31 GMT  
		Size: 2.2 MB (2233124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58d7ece0e8d9f9e1b840c7c12a6cfbc86bd65a386e4d67bbdcb6f3af11e796a`  
		Last Modified: Tue, 17 Sep 2024 02:25:30 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json
