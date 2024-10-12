## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:e74936587f0a50835c4d55994318ef4c2bcad1a906c3ba62749ea85f21f06042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:93a52eb03399fcef1a63da0f237ab1429d3a568fdb5755cd36c8a47479ee074b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264799564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4351e2b7a455c8a3d76a4f977760b1a4bf6f4b8c6cea07e89305cf47e469974`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4388343ff89e58cb79f36854e3f9013dfb86b97ad3f609f7c5fbe800c0720c`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 200.4 MB (200431985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322b2a5ffe1a767ad81c1f7a3f792daa1c8bbdbda45002f3e6e7de2af99a4bf`  
		Last Modified: Sat, 12 Oct 2024 01:56:54 GMT  
		Size: 25.4 MB (25445653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ef8c34bf0777fb448e6dbe39866bac0523b02e4eef145dc0bdb300fc10fb32`  
		Last Modified: Sat, 12 Oct 2024 01:56:54 GMT  
		Size: 9.2 MB (9170431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe1d5968f6817bdd4447b0bd77fc36014e1edf718b073e6baf8a34961201f7b`  
		Last Modified: Sat, 12 Oct 2024 01:56:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726e1851ec663f01d06e6f6c29a75d83f3e75e705f6881f4fcaa3bcfb0e28951`  
		Last Modified: Sat, 12 Oct 2024 01:56:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:e3d98b3c78524dc9b097f8a6097c2c55c15282ba224cd4a38b52980534a7b4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb5bc1bc6105e910dbc40ecaf323f39763fdddc74f8c2518a4a43e60b8c8d80`

```dockerfile
```

-	Layers:
	-	`sha256:24192d35a000e8c03ec8db795d73e138effd1de4228b89f3fe4d2f96a304a2a5`  
		Last Modified: Sat, 12 Oct 2024 01:56:54 GMT  
		Size: 4.1 MB (4129557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4e73902820b5c8be77acd1e4423a55bd12e0218d70a7b5a3117a52a4d818e7`  
		Last Modified: Sat, 12 Oct 2024 01:56:53 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:22ba136584ae8dcab432842dda4b246539e7a5d60a556ecfc842cb8caecec3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262661650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e77bd59ca7182530c50457e964ac92962838d647849ae50094fe85784ff65`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
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
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4ef29297c203f8c3f825637f08ed456ddf2f44a4ba769c04be1da4048b9683`  
		Last Modified: Wed, 02 Oct 2024 03:57:19 GMT  
		Size: 199.1 MB (199081070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b238407f2077ecd8973e75d52d7a9aec025d33aa9a2719635e14c1c4b18e5f81`  
		Last Modified: Wed, 02 Oct 2024 07:14:08 GMT  
		Size: 25.5 MB (25523660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6fe730476b81bcf20c5dde4080859a307a8b974ae31c224a1a7f437c9ae99`  
		Last Modified: Wed, 02 Oct 2024 07:14:08 GMT  
		Size: 9.2 MB (9170451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90389fcaa2aa956debe443060841fe5c06e88bec7c1a2c06d1a4444e10931b7`  
		Last Modified: Wed, 02 Oct 2024 07:14:07 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f5c2170cded0fe9e6de79d44afe6cbefd01ab1587511503dddb8331f95ec38`  
		Last Modified: Wed, 02 Oct 2024 07:14:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:bd6e1e5f3e61c27d6dd341d350c4f15ce3f63b69719bce8942a0243d82add77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0380bcd30594948d00d698ce2ae9f1f9adc7b228e0ccd4a6b9590270a10a87`

```dockerfile
```

-	Layers:
	-	`sha256:0bbc541dc6fb6f99c58525a0c88c441232b67283540bd5f7957a423c191807b2`  
		Last Modified: Wed, 02 Oct 2024 07:14:08 GMT  
		Size: 4.1 MB (4135446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb66b41b1992e754db55f74fd0910704ca6b6ad68d899c33ef9392b3db7c2b55`  
		Last Modified: Wed, 02 Oct 2024 07:14:07 GMT  
		Size: 16.7 KB (16673 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:89a4e020bd45f5d60db9ed61a5876a5225cb29ad84c6b366738b0db00eaf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275320928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8d497ef08df9e13d32839d956e1af38c9bfd9291a60a03e793d6fe0ee8fe93`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
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
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a63b36847726c03144ac71938f7a5236ff3eaddd9c1b3ccc873919c645edcd`  
		Last Modified: Wed, 02 Oct 2024 03:10:12 GMT  
		Size: 201.6 MB (201637598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be576f2a1ece38042421d07ec1855986f437b31ef620466bde663522bd0612`  
		Last Modified: Wed, 02 Oct 2024 05:09:25 GMT  
		Size: 30.1 MB (30119825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89972099ab0d611f7f090ede2e551b9544ee4f16f4f8e06bbf0543fe65128a93`  
		Last Modified: Wed, 02 Oct 2024 05:09:24 GMT  
		Size: 9.2 MB (9170446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abef54a50f7abdc744b3b0af416f62459480dd2b2125c84c2f82c3f3c671826`  
		Last Modified: Wed, 02 Oct 2024 05:09:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3541cc65cba405ea728aad21e4dc2793511ff0ff91f68d5a0fcc81c064f08829`  
		Last Modified: Wed, 02 Oct 2024 05:09:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:01a4fb9182402b825f364eba31b63bdbcaa4c03092976968f62c1ae6444127c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3162c980a5ec9e0f20a75e00cfe7bb7f388bfbbb6c789043b963f015333963d`

```dockerfile
```

-	Layers:
	-	`sha256:d4f105abe74fa21b84dd15b6809ad5cd2848280ca520b913f439f958e5aae934`  
		Last Modified: Wed, 02 Oct 2024 05:09:24 GMT  
		Size: 4.1 MB (4133768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb45f81ca5d31b499721e1e0f76bea7507efee24e3e39e1c37b6265d62610022`  
		Last Modified: Wed, 02 Oct 2024 05:09:23 GMT  
		Size: 16.6 KB (16590 bytes)  
		MIME: application/vnd.in-toto+json
