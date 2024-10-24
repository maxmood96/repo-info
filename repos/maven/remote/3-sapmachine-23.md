## `maven:3-sapmachine-23`

```console
$ docker pull maven@sha256:494a84dab7b16e0e51a71b1ca75269dcd042f2599c4d26af265d0292c9aed7b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-23` - linux; amd64

```console
$ docker pull maven@sha256:23484b04334df008992c9affd8b9361c48240b7ac0403d9c2615dbde5e9d5c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286901492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a702c9782b66e7b8c955b491f0abbe7a3a5ebb8d487191c102ce0a24043cb9e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d89d178e9798a7399a0e2265c51ed3fb09e3339863584dfc52a6c3a3abb03`  
		Last Modified: Wed, 16 Oct 2024 18:59:04 GMT  
		Size: 222.5 MB (222533919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7ddf263eaa5ee21c0bb0eda15e95f762da5cbaad38b1eff546f14b92c82f9`  
		Last Modified: Thu, 24 Oct 2024 02:57:01 GMT  
		Size: 25.4 MB (25445739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bafe36fb478fe5db210113df6b14033683959c6234226ef900c36ee98266cfd`  
		Last Modified: Thu, 24 Oct 2024 02:57:00 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8520ea4a3ada6b62e465f5b6c015d71190e9683c670906353bb15792054255f`  
		Last Modified: Thu, 24 Oct 2024 02:57:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0917ecd2aeb0d3479bb9736a90f7c8b8bdd4a35b9077e6e1c1d23905caa923b`  
		Last Modified: Thu, 24 Oct 2024 02:57:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-23` - unknown; unknown

```console
$ docker pull maven@sha256:e378452096704f6f571fff222783832b93c89ab47f7e8d75ef5eb343cb8e48f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2d12a0c095f973315b558bc2b58408d7db628d4edc677039c37148399d8c45`

```dockerfile
```

-	Layers:
	-	`sha256:6f2108d45fc7a3e5eb5b81a641503421a40621a5373a4a5d5ae403c35ab4a0de`  
		Last Modified: Thu, 24 Oct 2024 02:57:00 GMT  
		Size: 4.2 MB (4163639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd3798b93641dc12385008e9839b81f9de9351f330c6187ebfcf7a5e70fe3f9`  
		Last Modified: Thu, 24 Oct 2024 02:57:00 GMT  
		Size: 16.5 KB (16539 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9a6df4ca4ef9fb3d3f08bebb9415f76bbdca7044d2638c53e744ead735b7d01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284099269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becf836d698cd7170392056ea89ce674cf72fc94f5bdcfecd9b0610439fda96c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeef27d15eb0de1a2843de2a60ca495828be93f7a46641dc5990d8f3ce051ea`  
		Last Modified: Wed, 16 Oct 2024 18:58:43 GMT  
		Size: 220.5 MB (220517427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d63afdb26158aea9904d79e666285cf36768caedbcb49a3f308797494b8db4f`  
		Last Modified: Wed, 16 Oct 2024 20:45:49 GMT  
		Size: 25.5 MB (25524522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db9b55db0c87be30826f4362ee3080b4a6c5891f5bf13f94b655bbaed284706`  
		Last Modified: Wed, 16 Oct 2024 20:45:48 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2bc0cfaf681c64cf139535ae6407b243b6c6d8555c7ed7f85df3ed9a31530`  
		Last Modified: Wed, 16 Oct 2024 20:45:48 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0717e26a6081a1976f645ae237dca7acc18acb64ed99092a1f17c966633d2`  
		Last Modified: Wed, 16 Oct 2024 20:45:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-23` - unknown; unknown

```console
$ docker pull maven@sha256:e159b56b478305f2922f0f444ba4bb149437f68e53bf200298469644de0a211f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2ecd71fdfee12e5852b761e6d2950edab3e81f4c31da8e87d944978e8b0b3d`

```dockerfile
```

-	Layers:
	-	`sha256:64f28b5c67a0aa1ca168474b844af7e9e8e4b60c39e012fa1ae89db4dc3e62a7`  
		Last Modified: Sat, 19 Oct 2024 22:52:56 GMT  
		Size: 4.2 MB (4169536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcef701f31b112187ef6598daa048d619935c12ecee86451feffa71757027f9d`  
		Last Modified: Sat, 19 Oct 2024 22:52:55 GMT  
		Size: 16.7 KB (16672 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-23` - linux; ppc64le

```console
$ docker pull maven@sha256:9f21a0dc939ccb2d965aafed0f15f0397577e0282876b2e0e8aba6ecd8186408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297362745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe822b69b10b2a6fabb8e8cb0d32b946261b8b705259ce9f96792cfb06e04fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750abcfad739c02a09e3c6f61e6cdea4270ced245042f8eb08f90c778ff8282e`  
		Last Modified: Wed, 16 Oct 2024 18:59:14 GMT  
		Size: 223.7 MB (223682109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39139d0e81e159e99e89dcd243e8872e0090d2ae5f622964d686b526ea38000`  
		Last Modified: Thu, 24 Oct 2024 10:29:28 GMT  
		Size: 30.1 MB (30120194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a685cdd90890632dfd665a5fd6c2145bcbda6915bda69ee7444fb259ab6a770`  
		Last Modified: Thu, 24 Oct 2024 10:29:27 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b541e4e8ec0845775bf3fae261b009c791482b16879d8065d92192218a7a69e1`  
		Last Modified: Thu, 24 Oct 2024 10:29:26 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e24a584959587ff2e8be91b1c4808aca028249369547c26418e61164fe8e1b`  
		Last Modified: Thu, 24 Oct 2024 10:29:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-23` - unknown; unknown

```console
$ docker pull maven@sha256:7274767f468a045dfc073572037649763b8d8d26439b0c755b5f9033a28d2e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8298b585b53e4876a2b03999d0284829e6dba3db98b83a16f81dcd78146f76c`

```dockerfile
```

-	Layers:
	-	`sha256:873b5090f08c9fe1447f412f7446178cb6b7ae22588ab982d2f1972c40d5583d`  
		Last Modified: Thu, 24 Oct 2024 10:29:27 GMT  
		Size: 4.2 MB (4167870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59d02671c069f1dc88426664399e2e36c90b9b075199e6dca29a251ad63ed60`  
		Last Modified: Thu, 24 Oct 2024 10:29:26 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
