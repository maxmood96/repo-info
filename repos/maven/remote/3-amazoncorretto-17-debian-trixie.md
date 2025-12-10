## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:5781a09a198f006665c3d3338e628260852df82476adc3134c70db070f7f6a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:37d20399cdb5d632d997f815005c8c03bce04e7a5e62171397e512102b23a31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240505268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adf820e338880c4a1499e062ec6b3e1f77713d99f5361f60efe35a35bc68ced`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:58:02 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:58:02 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:58:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 08 Dec 2025 23:58:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 08 Dec 2025 23:58:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
ARG MAVEN_VERSION=3.9.11
# Mon, 08 Dec 2025 23:58:03 GMT
ARG USER_HOME_DIR=/root
# Mon, 08 Dec 2025 23:58:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 08 Dec 2025 23:58:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 08 Dec 2025 23:58:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572bb7ec86de2004ddff2f2c000ffebdca1d00b92a39cc867555917a934c72b`  
		Last Modified: Tue, 09 Dec 2025 03:29:39 GMT  
		Size: 201.5 MB (201485164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9793f2abeb78167c3c0f94e5b17555e5a9b63e7a28d721d3aca778257b3dbe`  
		Last Modified: Mon, 08 Dec 2025 23:58:29 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf5c078717449bff5569514ff62f784e93a6561df7aa2dd533ad06d43cf554`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed41296c3c8c12fe31ee414e55a38f56ac34d5e1d4dede847a48564348e06c8`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:ce56913808a5aede9f606e786b40019a9c0e04787e40d9b7eb14241cd80e8712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8ac36d0f767c2f9905bb9e991b00bf370f94a670105ddffd327b59dce37fec`

```dockerfile
```

-	Layers:
	-	`sha256:12c5a24efaa4dccc03b56e6f85b1260db8e8632751a3f16b8900ea0b476230d5`  
		Last Modified: Tue, 09 Dec 2025 03:28:04 GMT  
		Size: 3.1 MB (3103962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183ce8fe0e60c798f1d182342b5c68e879543b7934e6bc2ce83846ed9f4c7db3`  
		Last Modified: Tue, 09 Dec 2025 03:28:05 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d86862e847ce3568d0562efa197d203f60770645e962d1f1e2f2119da7549a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239307731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04759338b4845655289fd8e102ef03b1ca5c2e809fadad2dffc36e3e2d6a16b9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:04:47 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:04:47 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:04:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 09 Dec 2025 00:04:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Dec 2025 00:04:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:04:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:04:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Dec 2025 00:04:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Dec 2025 00:04:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Dec 2025 00:04:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:04:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 09 Dec 2025 00:04:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Dec 2025 00:04:48 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 09 Dec 2025 00:04:48 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Dec 2025 00:04:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Dec 2025 00:04:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Dec 2025 00:04:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a0a28995245f660c864cdd70130db566344191d45a68be0e0b2c845d1d633`  
		Last Modified: Tue, 09 Dec 2025 03:34:11 GMT  
		Size: 199.9 MB (199925470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797953e36ced15138c5d6932fbe8c3e4d407b375b457d13bd339fa7dd531c895`  
		Last Modified: Tue, 09 Dec 2025 00:05:22 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce5a2e2601033865e81e30679665229e2d9146de9d8d5a45d63c0807b3f91b0`  
		Last Modified: Tue, 09 Dec 2025 00:05:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e5c9b4408fa6a05307f75af3f7880bf9dce818b4641854bc6c3db7343839b0`  
		Last Modified: Tue, 09 Dec 2025 00:05:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:2266c4c3ea328891c277b1f4c6bf3626d2464c4e5f6fb2e0260e43218c77b79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb87afa4f84352bd95a4d37b46159bfe312c1afb9883b0ffa3ae64b83bc88f2`

```dockerfile
```

-	Layers:
	-	`sha256:6b482560b0f92aae601291e8088354a10bd7108d916546a3b943ed30ea506cbb`  
		Last Modified: Tue, 09 Dec 2025 03:28:09 GMT  
		Size: 3.1 MB (3103625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7001addaae8ca865ccb913ea66d6ae3af30ae0c8104b48ea70628fd0de9590`  
		Last Modified: Tue, 09 Dec 2025 03:28:10 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
