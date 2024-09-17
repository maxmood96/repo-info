## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:417f52d408b9be4ffe5ffaa58781c371a5aefaef7907e5bc069ee6fa8deee2f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-22` - linux; amd64

```console
$ docker pull maven@sha256:1605890561a1ce7585ecae39b71fdc3a2a5dc4f03f67cd43eeadb399ed10f36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280388073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b489991ed7754a38b225beccf50e6e9467c12ba04d1a90ebee16378c0a482789`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a45005dbcfff9284ebd035cf1c77b246cb1ea07d6c928b2cf18a1e6039347f3`  
		Last Modified: Tue, 17 Sep 2024 01:00:58 GMT  
		Size: 216.0 MB (216021752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07381024ad5fab71bd149ca78dc2366b4e72a2970334acbd778a0e422a29ac8`  
		Last Modified: Tue, 17 Sep 2024 03:03:08 GMT  
		Size: 25.4 MB (25445015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e823c81b0223eccaa0c0ed2b34504563b4fe63676b7a4d69a106af83af843c1`  
		Last Modified: Tue, 17 Sep 2024 03:03:07 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abf1a66e007f1aee9f8c03c75760b6bb7a6a9e315dd4305b455bcde5871c0fe`  
		Last Modified: Tue, 17 Sep 2024 03:03:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871c32ce53254d60a732a415ccb1ac955e750049a7a1b97199e8ff433652fd2d`  
		Last Modified: Tue, 17 Sep 2024 03:03:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:4e1cad0a18bbba9790ad548bf1f9de0fbedc297671b9edd3762dad48074f7f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c853dcc19896a18c690fb97e011fa81d45f489a61c343f75cf543499bb4adfdb`

```dockerfile
```

-	Layers:
	-	`sha256:b8c282b5e423f6135e1ad87280c63dcfbb39869d2953c9476773f480c87b0506`  
		Last Modified: Tue, 17 Sep 2024 03:03:07 GMT  
		Size: 4.1 MB (4132037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5041d9c7730eb0d1b9a6bef8927ef4b63eeac52a20513ee0ef795674277053e2`  
		Last Modified: Tue, 17 Sep 2024 03:03:07 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0e0b500fc2bd2207ab7c4baa4ae4c7bbe4287f19c5f504846a41c7c5bd56e5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275148623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a63c4a1079467d957e8c75af5940506791991c56b10081b7ac642d44222b4e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfadeeff48aee1833c0bcead3ce70130628740a0c8f0a5679b3e4344f0147c2`  
		Last Modified: Sat, 17 Aug 2024 04:03:59 GMT  
		Size: 211.6 MB (211611087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c16018626e250c9f2e4d028feb291b6bccf1f4aa180ac3e4f838738489e7e8a`  
		Last Modified: Mon, 19 Aug 2024 19:33:24 GMT  
		Size: 25.5 MB (25522371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e25b9f592343cd0f0b15628377a4260e698242d32ce7874add0a894492e870`  
		Last Modified: Mon, 19 Aug 2024 19:33:23 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd91cdf80234bc0f07479cd8c44a4f253dbd61d4524e126397baa8631764204b`  
		Last Modified: Mon, 19 Aug 2024 19:33:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b176eb1a93815e2f6629f6cb9e4a239909b780df4b49683d402b9578cf41c9`  
		Last Modified: Mon, 19 Aug 2024 19:33:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:7e6befb43cb7b68d1bd1e869b22536d9c0adf58a370de294ef70447dd43d6db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08f17be0f6af7e756cc1551a35705811945f01ff85eb0248edd6e4a2f29284`

```dockerfile
```

-	Layers:
	-	`sha256:1b80450835b3a5452f364a322b0357e5224edffe6e30b9358c0d58cb8275476f`  
		Last Modified: Sat, 24 Aug 2024 03:26:26 GMT  
		Size: 4.1 MB (4135364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892f6e13a98ffac4a72057f2aef228dac05f344afdca737af710e5703961ba44`  
		Last Modified: Sat, 24 Aug 2024 03:26:25 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; ppc64le

```console
$ docker pull maven@sha256:30929fe020ede0dfa5687ff2532fd85d384cc2866bf3074d7a49f23eb21a1250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288669528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc938221ed01d4f8700065036a2e681785ac069cdcc323c2372dcadef3b49c3f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9532c4c5000556df154a237634817f3c1c27c39c6d8ec47c69390d07b795c34f`  
		Last Modified: Sat, 17 Aug 2024 02:25:41 GMT  
		Size: 214.8 MB (214838877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbde76a4e182d5c7dc84769b036d5779c817309543f7e8b2a67e74a229725d`  
		Last Modified: Mon, 19 Aug 2024 19:32:23 GMT  
		Size: 30.2 MB (30151597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d188ad610ff782bf95fe3d733f0f9bd726b5264b41d4958e9357bdc0f3430e`  
		Last Modified: Mon, 19 Aug 2024 19:32:23 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c104cd09bf968ef681ff4580da54b32e2a35558d047ded55bb67e2198b7cb2fc`  
		Last Modified: Mon, 19 Aug 2024 19:32:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919fea739d01adc3eced1b5915d3461098aff4ce6fb2d93e936466b1fdea451d`  
		Last Modified: Mon, 19 Aug 2024 19:32:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:0f21a61b9b479e7d3f6ef93f95769ed6d0da5f560b959f2eea990a9b7146cce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b4d81fea3c325d35406c9bed12158fbab88a2fd16aa7104aa3609ecf9c6593`

```dockerfile
```

-	Layers:
	-	`sha256:2e8870662f4d1ac51812442ababb7a1ec4aebf18d99bc5d67d0bc638dbf18db9`  
		Last Modified: Fri, 23 Aug 2024 23:40:46 GMT  
		Size: 4.1 MB (4133698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34ddfcec2d6cde39048051cf444d7926ee2a68e06b05fc0d57ee0e6caa889df5`  
		Last Modified: Fri, 23 Aug 2024 23:40:46 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json
