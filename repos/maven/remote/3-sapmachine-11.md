## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:2f18a7401ebd6adfcd5971b20721ae04eec36c955c7acd274d26ad0fbc618a21
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
$ docker pull maven@sha256:fc2fb4897b146545494b339e40b5701f892f636548c4c9f173964f3955ce4453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263669594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92cfe2ebb503580a736a3aedfca389e4c208b8bbe755556ba31b543ec0c5cd4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0380c9e1dbe05c6be600d492433ced034dbbbf587f5c0ea7926ac084f8828f7c`  
		Last Modified: Tue, 25 Jun 2024 22:59:14 GMT  
		Size: 201.1 MB (201069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af91a40b81fac3cbfb68b4fbfbd006713cf95622bf41165be7f423a29c489888`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 23.7 MB (23731755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4582cb219359413c81a80b08b58c56fb2f13a5754e25c0343539bb3f91d80fee`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9815e9ff9920529b42db55144c24047dd1fcf17b9c2bac88031b2904528b166e`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5694e4b2f520f2722941cd443449860ad18f22bb00ed171c9ce71febe37502e8`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:8f77637e4da10c8ef066154242d40049a2c1e739df595c7b13b5636e178ba560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a76c1665447dc2c2000f9e8023aa10c4ae49be7ffab42c6de8ed4de52eb3ba`

```dockerfile
```

-	Layers:
	-	`sha256:497e28b43cd7087ca7c7a24184b2c8be6695b085071325ca834496df855214fe`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 4.1 MB (4064818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3c7e4b8bfce40f7b0184b5bb1828f78533dcf434f696ec498af529522212f4`  
		Last Modified: Tue, 02 Jul 2024 09:09:39 GMT  
		Size: 16.5 KB (16468 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:49d740227931f1373fcdeb3de5d4e29b5ff0d369b92286af96a5ce7788eb7ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261425676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c016305e08c5ac2b1e30f238f99c634256392c5407d091732fcabb8f168bf1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af178449a3d82005e4e48274e80ac75903c7d77ba094ecad224cc32372a13c78`  
		Last Modified: Wed, 26 Jun 2024 00:27:41 GMT  
		Size: 199.6 MB (199600542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095d85100a854ac6771ed51bc122eadd37176c9035348543a197a96587050db`  
		Last Modified: Thu, 27 Jun 2024 19:18:47 GMT  
		Size: 23.8 MB (23819239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9ba7ac22b9ce9c54dbf79bbf8b09b023eb23997dd6a0835cc756f46058f73d`  
		Last Modified: Thu, 27 Jun 2024 19:18:47 GMT  
		Size: 9.2 MB (9161808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1823f56471c01ca167f1da9b9f35955707b2f750edc4086725296d829b4946`  
		Last Modified: Thu, 27 Jun 2024 19:18:46 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe34ebcdae4bc555015252edf06ed671c2f8f61372e6211bbf6997047e5b31`  
		Last Modified: Thu, 27 Jun 2024 19:18:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:b5920540b37fc63955d02fcf36a01acf465d7ee9d872bfb3ea0e10901e5dc1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fa2f4e76982a2a9e5eee5db3d73add6a7810c2728cdb0342d084ecabd447c6`

```dockerfile
```

-	Layers:
	-	`sha256:37a6ce394ac97684070a1d941d07df0f05629f0ad895d7ffcd7bfffc7187c61c`  
		Last Modified: Thu, 27 Jun 2024 19:18:46 GMT  
		Size: 4.1 MB (4071971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2b5ffbaa3fac52c67844cbe9c3c6cadc4ceae57268104f3b8084152ca02fe8`  
		Last Modified: Thu, 27 Jun 2024 19:18:46 GMT  
		Size: 17.2 KB (17193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-11` - linux; ppc64le

```console
$ docker pull maven@sha256:c99d33710c13a2ff338329ce8ea7de8fb31e984026b34e09c0e59a8557ca92de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259397201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dd237ed0be25d5fc0762671082f92b2bc8ab7fdffe3e8232cc4668ff1f4a36`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c261f20e9a3447e9908f9559659ef384c65fd4c23b252312dcbee3d703b2e240`  
		Last Modified: Wed, 26 Jun 2024 01:08:08 GMT  
		Size: 187.9 MB (187868943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96802d3bc302b98e240366fee5d626f3915db9556cdac332437e68ec6bd27fc1`  
		Last Modified: Thu, 27 Jun 2024 19:09:59 GMT  
		Size: 27.9 MB (27859403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19128972784716dbb1d8b5eeadb6dee95bfd7a93371f0bd01ce592c57c74e9e8`  
		Last Modified: Thu, 27 Jun 2024 19:09:58 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501311918b12ab9d4c8cd892a33a5b307aecec5d8244bece83e49734e8af007e`  
		Last Modified: Thu, 27 Jun 2024 19:09:58 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a75ba8f8ab3ef980327dd1ec5ed84db111728d89f93f4c62ad3cc44dcc93aa`  
		Last Modified: Thu, 27 Jun 2024 19:09:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:cbd40d6644b78446eba19c169744bc0e7b86114f9355033ad3b8d0e90fc7de64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a78e6b3fc72fc42ce99231b51ca95992b9d5f5fc9fcffb4228daeeefb792565`

```dockerfile
```

-	Layers:
	-	`sha256:20b7f4590dad29456b1baa3c73bb77b11e6030129335fda49ddb8855ad2be6d4`  
		Last Modified: Thu, 27 Jun 2024 19:09:58 GMT  
		Size: 4.1 MB (4069022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88581207f0d1df783ff6d77482a9843676a91e18044fa82c9771949ffdef97a0`  
		Last Modified: Thu, 27 Jun 2024 19:09:57 GMT  
		Size: 16.5 KB (16549 bytes)  
		MIME: application/vnd.in-toto+json
