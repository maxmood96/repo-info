## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:7d92ae44f67f1104150d6230dd96783c91e7a573662fc0a81fe1ebed2e5d2f43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:62d134909d369b9645d29b3989da4e6c3f517d934f84ad93cbdaab1499fde23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.0 MB (424967133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8f522f5bddd673a2cbc59cde9dd783bd97b293996cf45e3e55a775787abd00`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:41 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:12:41 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:41 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:11:56 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 27 Jan 2026 23:12:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:12:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:12:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 27 Jan 2026 23:12:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Jan 2026 23:12:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 27 Jan 2026 23:12:04 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Jan 2026 23:12:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Jan 2026 23:12:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Jan 2026 23:12:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab537c006158cb59c0f5895965cca6f481a368f6abb61f4e81c796777a9eed5`  
		Last Modified: Tue, 27 Jan 2026 22:13:02 GMT  
		Size: 148.1 MB (148131195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf179d12cc8b387d1c6a6f168a279684231a89b79e3fcc5704757784a60fe1`  
		Last Modified: Tue, 27 Jan 2026 23:12:32 GMT  
		Size: 174.5 MB (174481059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b253f025240aa080e8e01d5bee44c9df88f3905ea3b816d940db84305078fe`  
		Last Modified: Tue, 27 Jan 2026 23:12:28 GMT  
		Size: 30.1 MB (30077885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081feddf3643b6463d771d61c8543f9da9846e72fa3fa6709b74dfefba0ab23e`  
		Last Modified: Tue, 27 Jan 2026 23:12:27 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e46e5ff9373d950d8c29b26c8e10bdbe9b4cbc98f6a74708e7998d599d958fb`  
		Last Modified: Tue, 27 Jan 2026 23:12:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a62be3882df17f8b9de737f404320cef1f7248448e986985cb51cadccb3856`  
		Last Modified: Tue, 27 Jan 2026 23:12:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:a5cf6d2af9501bdd549ec8760b9664df897d52ffad90386e4d0dd1024147cf66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bc7c22dc56e16f7510c457457f578939f5d75917e00f810cbd882507117ac1`

```dockerfile
```

-	Layers:
	-	`sha256:fbc8577d4d442b398d13d2d9cdfefb91f081011ccf05f66a6839d2d6c81cd7be`  
		Last Modified: Tue, 27 Jan 2026 23:12:27 GMT  
		Size: 6.9 MB (6939566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f7fec19c7aee576917a5a9f1c49eaee82430392739b5c40311fabc734c4798`  
		Last Modified: Tue, 27 Jan 2026 23:12:26 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:17d332794ea170f797d10ea282c7df94e47bc56993c335a7291fc11c5d59ceae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400850531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7b6c05df730e1dcc5c05a17a83657ab628370c3c862ff8f15c14aadd3a2e0b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:08 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:08 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:27:08 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 28 Jan 2026 05:40:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:41:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:41:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:41:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:41:07 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:41:07 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:41:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:41:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:41:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848e8ff28e37232003d119f3814367e3bd0c965552f4ce08dfd6f5d55ede073`  
		Last Modified: Wed, 28 Jan 2026 04:27:29 GMT  
		Size: 145.2 MB (145224227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df36c3368f9d0cd17f7077c6a0a54985c65569f749cfdb675ee92b66914ed87f`  
		Last Modified: Wed, 28 Jan 2026 05:41:32 GMT  
		Size: 150.3 MB (150310657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc757555a0afc89ccde716a99eb8bfa752860dcaf2b39dce300987d2aca98c0`  
		Last Modified: Wed, 28 Jan 2026 05:41:30 GMT  
		Size: 31.2 MB (31203466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9a547f7cc08265605810748d243309643b7716cd7f6f581b5ae0df5f13372b`  
		Last Modified: Wed, 28 Jan 2026 05:41:29 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6275cf0bc56053f34120d428fbb5325023b78e88522a251ff184cdbe186c11e`  
		Last Modified: Wed, 28 Jan 2026 05:41:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016448da4216eedba52840577277284253584c5c13f5f72217eb837b60dc9679`  
		Last Modified: Wed, 28 Jan 2026 05:41:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:bb2bbc217ab4572e462ae271c051053555b059a43f90384f0f0610c8ee0c3a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d58d6427f7f255b6c5c934317c429d2b0845cf1f3c18095499ccb11576be8a`

```dockerfile
```

-	Layers:
	-	`sha256:00d75c5442c6a2522eb1010c3c96615a213b9728e914a3fde0abc42149e27740`  
		Last Modified: Wed, 28 Jan 2026 05:41:29 GMT  
		Size: 6.9 MB (6937770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13ad5d5a2f980ebc48e8b9d54d7097eeaab5120c59c87cc181807840b3fb9a1`  
		Last Modified: Wed, 28 Jan 2026 05:41:28 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
