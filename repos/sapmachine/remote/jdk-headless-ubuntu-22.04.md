## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3dfcdbaf17c0f91d2138e48ff400c512812958252e7db36e471d62f3191d83a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b4dd6a0c64671f56c8a36899373f7d0cffb03d118e24ae3e21012f55fbf07eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241537318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bf183c46f6c68251085c7655b8b4e1945a7b53704513ca10106e7450a60e8f`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37de014020b783b494347f0c7032126246fb7c289f2e1b5bb1dffd55894475e6`  
		Last Modified: Sat, 17 Aug 2024 02:02:31 GMT  
		Size: 212.0 MB (212001293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f28d753cc2558cfeaa8f30f7d6e8cc5b808500b167248e3afb9e666e5629d6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41a6d16c23f14c8b098a1019633225017bf22c0c79f088bc007e623bdba80e`

```dockerfile
```

-	Layers:
	-	`sha256:55d510e8562d9d0a857f2183af2150656c3f072d3551cb86bec4bef0f894494e`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 2.2 MB (2231771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ad83df498e97ea6da0268ef91f323f4df9edb869d3f5005b41cb9be42d434c`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:949624cc93dc7fc206ec962fc3ba9f9b795799804b3894dc710958ac6289eb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247381725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f809d083488769c0f425d4ad91d4762f861ada14caf3d53c115d273466c7ef`
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
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4f3c50773d537aa95b1caced0571b8b36644cc0ec4fe1d7078e5d836ee9fc3`  
		Last Modified: Sat, 17 Aug 2024 02:34:24 GMT  
		Size: 212.9 MB (212917547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c2a8ea2c1c2e6fe1c07c51071b7f248a419be686f246d59d20f4745c5f8b6041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9783cca14dd001c4e069609ce35b888cc70778a987fb6539cbb1fd605924305f`

```dockerfile
```

-	Layers:
	-	`sha256:7c8ca75c9302cabc9cf55b2b3a3d887a73feb0227444d7cbdddb0d2c43fb2f2b`  
		Last Modified: Sat, 17 Aug 2024 02:34:18 GMT  
		Size: 2.2 MB (2233124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95b53477998d3ca1fc096ae9d95400db84b45ffee4bee722d30cd5c35cb8814`  
		Last Modified: Sat, 17 Aug 2024 02:34:18 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json
