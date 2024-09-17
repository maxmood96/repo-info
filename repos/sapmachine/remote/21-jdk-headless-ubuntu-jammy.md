## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:7309ffbb36b02267a83b83a16607b0fd969ce2c0ba00e07eccec07cbe8b5ded5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:29952a43d32794bafad1f3ea5ead85366b837776f1dbb848968c20022e799e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243533382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc525f377c0a0d218852749a1904e8226bf4d03e2a3b86763396f0a979388e81`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32aa4e2de54fcc083c4024715e825e2e76a128bd7ced1088e25f9ac789a21b`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 214.0 MB (213997694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e93a79ab16758e093a29e14b757efa6b8e6be1ff7493e9da04954db490aa6268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b411ae1ef2d0d2bb670216b26b9ebb12625d9bec5eb1c2a9c6f9d947ec4e295`

```dockerfile
```

-	Layers:
	-	`sha256:7f4a1f75363d9b0f63466ab83a6a02cf6f518f94b9038616a27cd3b8b78395f8`  
		Last Modified: Tue, 17 Sep 2024 01:00:53 GMT  
		Size: 2.2 MB (2231168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0716496376ba863b707ca9312ddc22570ea7f04e1b021172e467f646dbcc7209`  
		Last Modified: Tue, 17 Sep 2024 01:00:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cbc86fb253669241ba4869a6743011f5acb09edc0c098de4718631504fc961ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663dd9612961f6fc6fef3d7af56567b5711e310aeedc89cd0c3b65ae0298fd73`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776de449750c0b09806d701f2eb43a30b642b46442f57ed99b35c8e0a707a1fc`  
		Last Modified: Sat, 17 Aug 2024 04:21:38 GMT  
		Size: 212.0 MB (212049711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12bb35e4eb4e9c500eb75903f19fadab7cd05491507b6392f14e68420909cea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9649a2664555a5156e0876457ede7028cda084f5bccfa8c1cf942ce50ecbdcf5`

```dockerfile
```

-	Layers:
	-	`sha256:bf5482b9399746ae2e2ccac9906bc37051cc0803c2f4a5d9d836cca362b1ab96`  
		Last Modified: Sat, 17 Aug 2024 04:21:34 GMT  
		Size: 2.2 MB (2230862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56155b893afd34a01c6801601c03644b1450a26ac16e4cc2f9f28ef777c23b6e`  
		Last Modified: Sat, 17 Aug 2024 04:21:34 GMT  
		Size: 9.7 KB (9699 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d5b025129258cd8f17a8d631b19f3f77d6770e29d7d724d808e7842e2fd291c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249607968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2feffaa153b4d6dbe3bca81447e0f75c416526985b758238037269adf1767a4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846049fc299499bdb9bb4d425f492f379986184630720b11d0020669313aff6`  
		Last Modified: Sat, 17 Aug 2024 02:55:25 GMT  
		Size: 215.1 MB (215143790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7c77f3fc660a3ef97d58a7ade196d2ff347640440c5fd92fcf5ae7c00eaea3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833e078f1820ec949f1ac1ca7e37fe7e11e5901eec28035cb540fb8579692b3a`

```dockerfile
```

-	Layers:
	-	`sha256:6b96cdf7824e786431ee409235861a49593bb4394c402ba07bdc4b565de07241`  
		Last Modified: Sat, 17 Aug 2024 02:55:19 GMT  
		Size: 2.2 MB (2233140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73782eae9169f5b5249c8ad6850a32c398ef277e5ff5660bd9cdceae890ac273`  
		Last Modified: Sat, 17 Aug 2024 02:55:18 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json
