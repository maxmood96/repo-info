## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:9c16ab92522956f5ef5858c9ed48283ef09e640848cce64dcd80931dd15586d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:97ec97900ffd4201349314b1c3bba600373c58db22a93be774a612ec38adc4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265607482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0431d1d93a1221d4f046c9203276c76d2a31438f453880afbc24075aa9cf8dd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef724932d71ea48dc040303276ee799bafb5f05bf9326603847899207fd470d`  
		Last Modified: Tue, 03 Dec 2024 02:37:07 GMT  
		Size: 201.2 MB (201237858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5487e239fe244ab923cca4abec5de8cad41b0f0be22bb959b5ae12ac71f842b`  
		Last Modified: Tue, 03 Dec 2024 04:34:03 GMT  
		Size: 25.4 MB (25446182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b233909cea15b2e33dfea69e8b22b7cde616b4af7ae49a753a30f1abc601f68`  
		Last Modified: Tue, 03 Dec 2024 04:34:02 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18580c769e8f1e43ec00ed9b9205053cc2bf3b4a02dd17b7bbbff7d41d3b6a8c`  
		Last Modified: Tue, 03 Dec 2024 04:34:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3564c36ffc551ab4708b2afe8862c929349bc99fbc0ab2e487c4b6fb36091213`  
		Last Modified: Tue, 03 Dec 2024 04:34:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:f13f781802b898f0cd4d994ad6415b23b6dde1a6a27f270363233e7f71f77baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4188959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbdb1a4aee21e5e7dfbfd2bedcf5b38a867d47e47b267ef1ea3c672a2e1cdcd`

```dockerfile
```

-	Layers:
	-	`sha256:e2c0004fba22f427bf41148b0c80b3f596d12e3eecb0dd18ae34c66fcf80be6e`  
		Last Modified: Tue, 03 Dec 2024 04:34:02 GMT  
		Size: 4.2 MB (4172421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe56874b6b272002b6e8087ffb444310b65600e81b2a518c81d2ba6e625dcb08`  
		Last Modified: Tue, 03 Dec 2024 04:34:02 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fd1e7f19a805092f47d477b789f1c7024e0bc4aa7b5dec9527d63e398fef7876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263328935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fb15f8ce1d7e95fd51e602cc5b8d5f5e69005134557595128fbd4959f788d3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038ca03857cb9230b91955cd3fa6db65d7d2f415b902b2113e5dbd120ddc7e18`  
		Last Modified: Sat, 16 Nov 2024 03:54:35 GMT  
		Size: 199.7 MB (199739837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecbfb9345156655191f1b3fe8c073cf71c970bc1f097fc959f1efb960bcf0d8`  
		Last Modified: Sat, 16 Nov 2024 08:05:01 GMT  
		Size: 25.5 MB (25525194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78db1096399c592ff9824c00d1ee9d39ec4b5643286742cb4d7ee06cbf691a98`  
		Last Modified: Sat, 16 Nov 2024 08:05:01 GMT  
		Size: 9.2 MB (9170445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64266f8c01b9c18ac1e501c7bfced41d4c8dde15cfe0a393f8e359f17708c1`  
		Last Modified: Sat, 16 Nov 2024 08:05:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408517ef33ad61ae7ceac93bc6e7d3937a8e7c6a0e4f21ee4561bdda700f0818`  
		Last Modified: Sat, 16 Nov 2024 08:05:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:6598aebd0ff23d7e3705bd96083bb9bf98ff228a045c802f43704c8065bb1a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9494d08a13475d00b4bdb09dae503fd02c337160ae8316b2ddd30aa4be1c23dc`

```dockerfile
```

-	Layers:
	-	`sha256:fcb0c9dbc2235307a27dcc864ef9c228f444f5f8cfef15b64a8a793010564cd9`  
		Last Modified: Sat, 16 Nov 2024 08:05:01 GMT  
		Size: 4.2 MB (4179557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e765f1de63382fd63ddfa58ef730acacf049e26f5452a69b4009fcaf405059`  
		Last Modified: Sat, 16 Nov 2024 08:05:00 GMT  
		Size: 16.7 KB (16672 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-11` - linux; ppc64le

```console
$ docker pull maven@sha256:28bc0fef934c67ce8a05691f3ffb9bd311fabb9f2d8456b6297a3ca333d5b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261695721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6232315a37d2f60d12d94dee97875ce6552be6d5a9d8e26591fa0f5aaaa0e326`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0054bdc255dc1b06b8b1161447179fa9c23f8df02f78bc2fe0b702ac092d803e`  
		Last Modified: Tue, 03 Dec 2024 08:45:42 GMT  
		Size: 188.0 MB (188023984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f9ced8258ff2cf4c6c8ddeb7814480bf1b73dd5b13099af794acc5dc90a2b6`  
		Last Modified: Tue, 03 Dec 2024 23:12:17 GMT  
		Size: 30.1 MB (30111453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c923fbaee3ef3bca4aba1fbdc7adb661640fa94b3c629f734ea2ccd479c0c48`  
		Last Modified: Tue, 03 Dec 2024 23:12:17 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdbd7ca85f07f6f8543556cb26f4a4f792b2f8f9760a69a61f9586d22759774`  
		Last Modified: Tue, 03 Dec 2024 23:12:16 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcac9e0ea8b72fa7fa848eea6728aab69ae37d3050093bae9ef17e7365584ea`  
		Last Modified: Tue, 03 Dec 2024 23:12:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:11f07495cb5f3a45f5fafb3563abd279089dce92244ef3b84797d04e8fdbd3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4193235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a518a9f39b64d4ecdaa7b88018dc188ff2db4b9ff09d9f93626c814b7f69bf4`

```dockerfile
```

-	Layers:
	-	`sha256:b8c2354eb1ae4d8d8ab17977f343e1faa952c19222fa27078e923754fe590af5`  
		Last Modified: Tue, 03 Dec 2024 23:12:16 GMT  
		Size: 4.2 MB (4176646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5dfc09ffa1a4ec1dcf8a81bfbe3be31509523b374ac08197a8989adc296ed7d`  
		Last Modified: Tue, 03 Dec 2024 23:12:16 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
