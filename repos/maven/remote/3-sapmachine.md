## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:1696e070027ff188ae35e434f4e80234f766e90221ed694af7d22027e700f2b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:60e6dd3e0277389352a711707e3fb7d17ed5ec3cb0265ad524dbd2a6e2981128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278197424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12105eb398660f2963bffcc6498f62a313273b38bddfd0cf102c57bd8ea7df52`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 27 Jun 2024 09:17:07 GMT
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799e6c8a18494d282df4c820ebf58962cdbe65114f284259876e154b4c38e63d`  
		Last Modified: Sat, 17 Aug 2024 02:05:55 GMT  
		Size: 215.6 MB (215596028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf5c2ad12f42064ad460d9e91d37176dc49401752845b747d297a68422fc5fa`  
		Last Modified: Sat, 17 Aug 2024 04:07:45 GMT  
		Size: 23.7 MB (23732246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3547e0c33004faae6960b1d360fdefac7e238879c8e70cf920c6602c952af1a4`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02c825021632b381889470cb258c3ade265792d501d09229f18ad01055151`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e124c03bf687a16875846abcc960dfd760a77d45bc4d5875b25b30a6565f70`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:eff2ae7f97940bd743bb5237a6142a23b3e714275ae9f8d7286b81245e05b409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed841a8e37ee0a132dbc79ea4480b5f2c80ad35ac480e52dc30394cbde65329f`

```dockerfile
```

-	Layers:
	-	`sha256:6ddf61f17f66c5d02bb901edaa484f74ec094749da33febc2b402602d45adb3e`  
		Last Modified: Sat, 17 Aug 2024 04:07:45 GMT  
		Size: 4.1 MB (4088274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee580b725e5016b6cdee9aa2e4057c1e223de36b52497c1914b9ada7355e5fde`  
		Last Modified: Sat, 17 Aug 2024 04:07:45 GMT  
		Size: 17.7 KB (17710 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a361d31eb2ef770d9c9d481a3bf6df6a7020a1c1bcc0853ac3ca045b69d291ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275525801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf24babb4227622c4db4dac264df585d81bad40b9eccf02afc30d863f168c72`
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
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 27 Jun 2024 09:17:07 GMT
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
	-	`sha256:449cd0fe4136fb4bc886851588de52573da728d4ee027a91372e2ee9d773a4e6`  
		Last Modified: Sat, 20 Jul 2024 00:09:00 GMT  
		Size: 213.7 MB (213700687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bdc593f8f28fd4c8abc8c0dc6f1f9c3b33cf3abe10cd121d0928034248ad74`  
		Last Modified: Wed, 24 Jul 2024 19:19:05 GMT  
		Size: 23.8 MB (23819240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba757737397c5b5fe1bf3416f0c098717dbd22b032c8c8ad17986510d1c06d9`  
		Last Modified: Wed, 24 Jul 2024 19:19:05 GMT  
		Size: 9.2 MB (9161792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d7a7342bfa2398fe174e09ad0267f712d16ab8f788c48e4e17c4f22427bc43`  
		Last Modified: Wed, 24 Jul 2024 19:19:04 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14f55e13fc86a6c4e613546f1ece3fda98cd227925e1ae4f85cc5734a2be8c0`  
		Last Modified: Wed, 24 Jul 2024 19:19:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:77cae1623b328e7f6600554b00bba2d0d9f89a3c01c631144950e31fd66bf14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27a3a5616f3202ace0251cfa6253ef3c3b85b6182694dcc2a22fda16194bf8a`

```dockerfile
```

-	Layers:
	-	`sha256:de1e46a608955e74dba3efc3ce5aeb9ad4acd6a8328182bf302468bbf2aee517`  
		Last Modified: Fri, 26 Jul 2024 02:19:04 GMT  
		Size: 4.1 MB (4094827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53dd6aec7abd892bd9303ff888e117b0161c50ec2d96a394e5fd127bdaf0dd61`  
		Last Modified: Fri, 26 Jul 2024 02:19:03 GMT  
		Size: 18.5 KB (18483 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:6e20a8538a6bd2fbfcf8bff8045e7c865b2609b50e529267af60699be11789f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288589771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b17d0c96a1f5b3bd40bc69a2dc05a9b8dc7ac6eb5ad8806832f04d4b510d25`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 27 Jun 2024 09:17:07 GMT
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
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b635f6eb6a60370f38c733b410c2c5c704b50b31485a59ebb304b4975e12d0`  
		Last Modified: Sat, 17 Aug 2024 02:46:41 GMT  
		Size: 217.1 MB (217058172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a507e68a8bb57c85ce10a6ebb12faceb3544b865f97a54345b30bb196efc44c`  
		Last Modified: Sat, 17 Aug 2024 11:56:04 GMT  
		Size: 27.9 MB (27861175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d918a59ffb7678280b72ec47a83cde82084db0194fe8efa6f10925e50f88eab4`  
		Last Modified: Sat, 17 Aug 2024 11:56:02 GMT  
		Size: 9.2 MB (9161814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c86d1d11a7d5ab59adc33499b5424afcff0ba4290b608124a19fa0f8b9b9873`  
		Last Modified: Sat, 17 Aug 2024 11:56:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2d21b9bfea502e3a6dba32dc1880af206fb73f242ff9007e010da278970d58`  
		Last Modified: Sat, 17 Aug 2024 11:56:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:91130715222d3e8f27db31dfee68324ffc20148aa1e09191bcc899335b341c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e5b16f8d7663fd4adb6772868ab0baa27881fc0865c5ea067c4bef14c803c5`

```dockerfile
```

-	Layers:
	-	`sha256:513e630f577f76f075c0f601e5f69b219f343dc10fdee03ac7e6cb2f76e76df8`  
		Last Modified: Sat, 17 Aug 2024 11:56:02 GMT  
		Size: 4.1 MB (4093127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7d808c78fd0cda202dc7b9f44bcfa435ea7de41e4204734b09e8a7e9b47491`  
		Last Modified: Sat, 17 Aug 2024 11:56:02 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json
