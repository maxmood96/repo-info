## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:f57b25ed9d66acfe0d1bfbd89f8a225f7d708fee12479ee6de6b51af905700aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:3ac333dfbd0846a0e85c939eb8e74ebc6b4488d0795df5cba9e3075e76c763a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279403921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8eaa31506ea31c1792f5b157dfa6be42172549f8626698534f2455f3b2fda5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
ARG RELEASE
# Mon, 27 May 2024 15:57:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 May 2024 15:57:48 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 May 2024 15:57:48 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44c14fa70ddf63252b0cae7a2141bdbf20da1144f121287213ee8f5d90e71e`  
		Last Modified: Mon, 17 Jun 2024 23:30:13 GMT  
		Size: 215.5 MB (215456844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe803046e3445a57efb2f941c8848816cb8a94a9701ea7860643ffb6eaccc727`  
		Last Modified: Fri, 21 Jun 2024 02:01:55 GMT  
		Size: 23.7 MB (23731831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cb37cda38eabe8e180414b35bb69911b4a4e67882f8240fc274310787ca945`  
		Last Modified: Fri, 21 Jun 2024 02:01:54 GMT  
		Size: 9.6 MB (9647576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5870b2c78789fbd431e27426c059e21d883736f1ce4452a45e5c1f01664920df`  
		Last Modified: Fri, 21 Jun 2024 02:01:54 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8b593699e6a985c8d6c193886eb03470fb2cce7304ab47ffa4869ab24dbe9`  
		Last Modified: Fri, 21 Jun 2024 02:01:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:5bc1a4780beb7bb626e28dc8f72dd776d781c1d3c75cc8d056c27fef99aaa584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dca2addf0591566fa33ead0ad93f9684aef8640897eb57b666e68b6b58b62aa`

```dockerfile
```

-	Layers:
	-	`sha256:d18b61a2b1fc0185ddac9250905754430675d4c63967b2bcc13aa35531893795`  
		Last Modified: Fri, 21 Jun 2024 02:01:54 GMT  
		Size: 4.0 MB (4048779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4913ff25b6e75d49dfb1bcaa49d4432872253c6b1dad6cfa75d4897ab80a50fb`  
		Last Modified: Fri, 21 Jun 2024 02:01:54 GMT  
		Size: 17.6 KB (17564 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:89c07c9195a09cb4e569fff3eb65f61de146a43d122445bb6a381f89f6af931a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276938305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d542510a6196a705158f2f68f84607354c10ee6b72ac47a7bc7c31129b96fee6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:27:49 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:27:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 23:27:51 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a9145a93588cf400771b8ccef8e27359bdfc30d0d7ba0fa748eecc20886e5`  
		Last Modified: Mon, 17 Jun 2024 23:37:36 GMT  
		Size: 213.6 MB (213560230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5191fe49edf5123818e001e62cb6e9cec1d51aa726118f05e39dd5c09ce577`  
		Last Modified: Tue, 18 Jun 2024 00:14:21 GMT  
		Size: 23.8 MB (23821177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0514aceb6af39389528dd3a8fca6cbb3edfb141b36ba98ba04df42da90f593`  
		Last Modified: Tue, 18 Jun 2024 00:14:18 GMT  
		Size: 9.6 MB (9647544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a906f28fc73c24652201caf0288609903aa8d4559ba79c321d6e7640881704d7`  
		Last Modified: Tue, 18 Jun 2024 00:14:18 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee7303e53b673d4301cd05927bd5634c28c409f66ed0beddb93b42c293c8ffd`  
		Last Modified: Tue, 18 Jun 2024 00:14:18 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ead3a3090f5c003cfb8a58842dbd377568a55a702d86bfb39b9642c878af4b`  
		Last Modified: Tue, 18 Jun 2024 00:14:18 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:ba975998dfeb607fa2b0b0d2dbeba26d874eaaba443d1aaee501c667a302852a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290050676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b8b8283ca5fb1840f2ba3eb9a810375ab935583229af5c8646eb0d2db36e44`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
ARG RELEASE
# Mon, 27 May 2024 15:57:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 May 2024 15:57:48 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 May 2024 15:57:48 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d03952f1ef0b93942eb4a115658ba187c7c63ef5e41c36c631306e050f50bd`  
		Last Modified: Mon, 17 Jun 2024 23:11:03 GMT  
		Size: 216.9 MB (216915461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078af06ced54bfdc390f0f504d25e030da778963b3c02d37d5c5e36cbf000b7`  
		Last Modified: Fri, 21 Jun 2024 07:25:02 GMT  
		Size: 27.9 MB (27859614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039017f4f2eb37981df10f4a1757ef02dbf5022137a65db359731e0ba93bf2e`  
		Last Modified: Fri, 21 Jun 2024 07:25:01 GMT  
		Size: 9.6 MB (9647601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528347c1a67d074eb7f278000683c1c2412a88b51b31ed36956c0f055162315f`  
		Last Modified: Fri, 21 Jun 2024 07:25:00 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b592aadb14285a9913a8d1f81110e1977bcce5bea30ce847e77ddfbbcd369449`  
		Last Modified: Fri, 21 Jun 2024 07:25:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:f7e0bda798f753b04265bcf3599a0458fd3cede34fa0c569e6fbcd8434feaa89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5d8262ede13e70ca39cbb4597cf17fbc1412e345c0b73ce3a13412cc34862f`

```dockerfile
```

-	Layers:
	-	`sha256:e597ef0d7b5962cb90e38a89d2cf951004cec22157fd4767697477dcaa29ef79`  
		Last Modified: Fri, 21 Jun 2024 07:25:01 GMT  
		Size: 4.1 MB (4053632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26789bdc265a36315b01ba80502270b9833b9f83022acdbb697f9c5abc0f7996`  
		Last Modified: Fri, 21 Jun 2024 07:25:00 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json
