## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:a24a5dbc9aa2cd83f944c2cab2931f4cd625fec982329548c75accae9ca12bb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:1203367079b1b4c56eea88706f7df3871f0afdee4c9cd667eb483120327f9c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427808191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69c93345ece78a0cb5d2b67b530bb6ea74df348544d024aca91748214bf4f5a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:25 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:25 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:25 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:20:58 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Dec 2025 22:21:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:21:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:21:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Dec 2025 22:21:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Dec 2025 22:21:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Dec 2025 22:21:07 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 11 Dec 2025 22:21:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Dec 2025 22:21:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Dec 2025 22:21:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Dec 2025 22:21:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac57126ecd86ebc8bfbf2f8c72cef47008c2e2b42c706b3d2d81f5f916ccec5b`  
		Last Modified: Thu, 11 Dec 2025 22:13:15 GMT  
		Size: 152.4 MB (152417728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4fbd7e436048dadc823693e0a370f3a25e450dcb6a8b21e090d2e03bce5a7f`  
		Last Modified: Fri, 12 Dec 2025 00:31:12 GMT  
		Size: 173.1 MB (173138167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a226d361d45714e7fe241e4700cadf7e26889ed84930e4d08c75b7736a53e`  
		Last Modified: Thu, 11 Dec 2025 22:21:42 GMT  
		Size: 30.1 MB (30067702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c4d58054dd61db7dd8487384431e00f222d62a178b5249f3c6349346d74e5f`  
		Last Modified: Thu, 11 Dec 2025 22:21:39 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3eaa84a85ab3e2fe189cd1d80a4ee8fd8b26662e32b0762a5dd7517e6743a`  
		Last Modified: Thu, 11 Dec 2025 22:21:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74ae6f6bce0f327bb8e8cfe2a1ee9b1ecdb99d8b1c842bef827e05632060178`  
		Last Modified: Thu, 11 Dec 2025 22:21:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:7ce6236ae78660ce222669ca4a7ff8e672009559b5ddb417a796e1464c9e3719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510e8fc75e3c175531f57a6b27fcb2e2f0d0758739262987bdc93efe2676d861`

```dockerfile
```

-	Layers:
	-	`sha256:47c8ec3a197712b6afe9b8d3d10f7a7241a5a4859cef41b3e08f44a3a006991f`  
		Last Modified: Fri, 12 Dec 2025 00:27:49 GMT  
		Size: 6.9 MB (6932262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360805f7b1598e727e4fe0e1a2df4e69ebcd0f8f83e6b7dc0f24d1ed2d8c97de`  
		Last Modified: Fri, 12 Dec 2025 00:27:50 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0e9b02cb02e674a16ac5c194323bf4426006d3645e6a0d4ef9c6dd1eeecf292c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.3 MB (405302638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7279c31480c2de5774b4a6c1742596d86414efb3d183a3ee1eafbc6bd4d7a2f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:02 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:02 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:20:58 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Dec 2025 22:21:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:21:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:21:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Dec 2025 22:21:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Dec 2025 22:21:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Dec 2025 22:21:06 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 11 Dec 2025 22:21:06 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Dec 2025 22:21:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Dec 2025 22:21:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Dec 2025 22:21:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67bc37dbe272db9b7b10c3283dea952f31754f43ec167dae43bf6ef83012ea9`  
		Last Modified: Thu, 11 Dec 2025 22:12:56 GMT  
		Size: 151.0 MB (150989128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da25c922ea3ec7bbe5cbbe61399547412e5fa29142edf19b159c04196b56af`  
		Last Modified: Fri, 12 Dec 2025 01:04:09 GMT  
		Size: 149.1 MB (149078644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced1bf784e0dd19b72ce63f9df7dd26d2a74d8d23897a411672b609f898fb3a`  
		Last Modified: Thu, 11 Dec 2025 22:21:39 GMT  
		Size: 31.2 MB (31195499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d944c4f6b9a657e1064ed50d972adaad6e3b985469482fdb73db98c1fc97a99`  
		Last Modified: Thu, 11 Dec 2025 22:21:38 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d5449288c0446e197d03896523b066b05accd7546d759fdfff4a0044fd48c6`  
		Last Modified: Thu, 11 Dec 2025 22:21:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e32b682ad97fb002247590b5ce0a0b0324832013c1ec3b6be918fa2906ea8`  
		Last Modified: Thu, 11 Dec 2025 22:21:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:a60514b7c725b856ceb96e11a6df88b14e33c7a2c80be76b11bf233f96b02058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47ca68751c2bf62daef8ce2dca12b7d1377b4aaba4b19056de343a992fbdca8`

```dockerfile
```

-	Layers:
	-	`sha256:6c5d33babbf3083c596f7dd22939a07c86752a133fdd1da0197bb3a55a215bff`  
		Last Modified: Fri, 12 Dec 2025 00:27:56 GMT  
		Size: 6.9 MB (6929661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9c8b629a8897a430be3cbb393845ac127195df965c82e490b50e5a2e5ed44f`  
		Last Modified: Fri, 12 Dec 2025 00:27:56 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
