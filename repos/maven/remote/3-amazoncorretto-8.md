## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:d8bcf68b6b58b8a41c22087758fe86e9f295a3f123bd8cd7f6a7ef26a202a022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:7931a79c5e421e2a570216747ba103f57a2adad25d784403741a829cd72ef2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351963418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0aba2fdb133d2b6cf12f8f817d5f24d8f9d3658ad47de282f53e2b94faa82b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:15 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:15 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:08:15 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 16 Jan 2026 02:47:01 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:47:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:47:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:47:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:47:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:47:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:47:10 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:47:10 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:47:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:47:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:47:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95512b2044a8f80c577659eead5e19c14c6cec9a57545ced886f0055475bb3a1`  
		Last Modified: Thu, 15 Jan 2026 22:08:55 GMT  
		Size: 76.0 MB (76044822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187751f4503e75a4047c56b4e476e2cad54182dfb34af38700ce5640faed67ab`  
		Last Modified: Fri, 16 Jan 2026 03:40:56 GMT  
		Size: 173.6 MB (173600652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4faa1cfe5e667710d3730946766ec0c424535f18c36d30efcdf58e0c0882a2`  
		Last Modified: Fri, 16 Jan 2026 02:47:44 GMT  
		Size: 30.1 MB (30064502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b80686a367dce24d336b4a3b2a6858204d50aa1834041ae4541a4e0085284d`  
		Last Modified: Fri, 16 Jan 2026 02:47:42 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd992fe3edcd0d0fc8beb45752e5daf90599a0ece93dda61dc9d3a187c1ac95e`  
		Last Modified: Fri, 16 Jan 2026 02:47:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa43fff455b11c8aaaf8a5633227299e3980f82da913267f535c1227394ef48`  
		Last Modified: Fri, 16 Jan 2026 02:47:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:96e93f246762bb697a3e0c038302d28aa4ce31f9cdf102c9eecb8d5ea2d16813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975891c14c8e2f17edd3f7f27774b5bf067c2b66d68575e59bd0efa94ff59f19`

```dockerfile
```

-	Layers:
	-	`sha256:fc95f42d657c9d23aa6475e8a78d98edb0a09d8b94c2ce7a127c79e4e6dec06e`  
		Last Modified: Fri, 16 Jan 2026 03:29:56 GMT  
		Size: 6.8 MB (6773617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540bbdc41774c632e784b5ff7f1a7903a0dd5b1016f46b60ef902243e5af49b1`  
		Last Modified: Fri, 16 Jan 2026 03:29:57 GMT  
		Size: 18.2 KB (18187 bytes)  
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
		Last Modified: Thu, 18 Dec 2025 03:51:14 GMT  
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
