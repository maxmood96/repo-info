## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:0e30b42d04fa1534d6da869240dd381a5f1f25242e62176a15fdc399aff80f21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:e247518f26bfe5ef2cb00ac728b1d01213fc76a70484249356eddc44115f00a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351504697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5df1dc14ddc37eace3d0b3d0b4ad398f780ffc8f03538ff59123071c15ed2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:04 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:17:04 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:17:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:23:02 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:23:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:23:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:23:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:23:11 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:23:11 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:23:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:23:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:23:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80894dab91952a05cdc8c31d3d369cd7a718bcbf79123ecd960e8e93563b7686`  
		Last Modified: Thu, 18 Dec 2025 01:17:31 GMT  
		Size: 76.1 MB (76052455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd12e81b0d506edece5677550fe1f082800e2938187909a3d2d87b3ba72550db`  
		Last Modified: Thu, 18 Dec 2025 03:20:32 GMT  
		Size: 173.1 MB (173125312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cead0888ac8efee692ee504c792393d303d56f49a2bc756ad7d702e3ee056b`  
		Last Modified: Thu, 18 Dec 2025 03:20:24 GMT  
		Size: 30.1 MB (30072669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c13d122cc5cd412123efcb9f1c22d3e925b5f7c981fa1383f3c38ee60a5bfb6`  
		Last Modified: Thu, 18 Dec 2025 03:20:21 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8c39ff5838f00e842d2b89c7eb8b1bcbb2f1849c0b0743aa15b35b74eeefa`  
		Last Modified: Thu, 18 Dec 2025 03:20:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2293943a2744fc753f85cba8f468ebcbb883de179e245b7c7cb4c13d1fa3fbab`  
		Last Modified: Thu, 18 Dec 2025 03:20:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:9cc106c1a73c6538750dc5cb51fbd40a49f01583925f87391625a939c419d118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69f6242e09b36e07502b07368d8d3bb526b14bb5597f7a5022311f74632ff52`

```dockerfile
```

-	Layers:
	-	`sha256:70daae9532672244523d598753cb18726effec1f5eab43bc99474256d12c632d`  
		Last Modified: Thu, 18 Dec 2025 03:28:43 GMT  
		Size: 6.8 MB (6773617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:257d04ed67fc8e463cedd9ae65efb5fd71e5f3b80820ff4e39108249835f40fe`  
		Last Modified: Thu, 18 Dec 2025 03:28:44 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:737d8d931ec3fc41acbe9b8733247705b47204cd2c238bb065c9dc9b722accd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314505795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c689003b021adf88a805f99c61f105ce0c058f6f5593c89ef8b7a60360e546`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:24:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:24:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:24:25 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:23:41 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:23:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:23:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:23:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:23:49 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:23:49 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:23:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:23:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:23:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909fe2bc51d4f2e9dc917f97ac6bb1a9aea7b2afc8fdc287ac788a885c135dd7`  
		Last Modified: Thu, 18 Dec 2025 01:24:53 GMT  
		Size: 60.1 MB (60118031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79122f3eb69a6e48f30b482b6fbfbf6ff98d69f4f485138844b0395e966ce9e1`  
		Last Modified: Thu, 18 Dec 2025 02:24:15 GMT  
		Size: 149.1 MB (149076307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12d31c4e41c406f1cecce82fa1c8937a578503b54c446aa7ed4b66397014f4f`  
		Last Modified: Thu, 18 Dec 2025 02:24:25 GMT  
		Size: 31.2 MB (31202411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07d8bb7a1e2cb934024377550edf6761278635778471b1070569f9e07b43ef`  
		Last Modified: Thu, 18 Dec 2025 02:24:22 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f80578e64f027b551aa08755f329e142edc54c9085d232525d91a4d7091ce7`  
		Last Modified: Thu, 18 Dec 2025 03:09:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceedcf8b6b2d70c4048f07f9f4a9e613340d013583a4ddbd2c75be2003fb80a9`  
		Last Modified: Thu, 18 Dec 2025 02:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:c1a69d09013a47b8af380a978ef1d8014bd8fcfdaa45bd4c886978384bfffbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5d34916779d7a0a40fcce98f291829fe3c37e5ddcdef65f3f80325cfe32b49`

```dockerfile
```

-	Layers:
	-	`sha256:c394c794bce6d869c70bdc3de29b406b970aeccafba82f4a5281564c1aef0a04`  
		Last Modified: Thu, 18 Dec 2025 03:28:50 GMT  
		Size: 6.8 MB (6750814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5525a60ca1ec7e61ce363244d89c649f52115f92e58a182e8a576f8ea4342342`  
		Last Modified: Thu, 18 Dec 2025 03:28:51 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
