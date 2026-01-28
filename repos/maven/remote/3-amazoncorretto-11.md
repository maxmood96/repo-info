## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:33b841d898b7a7bc1415354094f527c3e46469519a05b0e01aae7a8e4770487f
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
$ docker pull maven@sha256:3ad9ff5b8c50a61a6df2701732ee86117c474dcc54cce3fa85e74c1eda0bc07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400850577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb52ab11f23303cbee87db9e1b870fe13a950fa08bf0ed5284bc185b01ecb94`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:39 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:11:39 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:11:39 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:14:29 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 27 Jan 2026 23:14:36 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 27 Jan 2026 23:14:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 27 Jan 2026 23:14:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 27 Jan 2026 23:14:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Jan 2026 23:14:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 27 Jan 2026 23:14:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 27 Jan 2026 23:14:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 27 Jan 2026 23:14:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 27 Jan 2026 23:14:37 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 27 Jan 2026 23:14:37 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Jan 2026 23:14:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Jan 2026 23:14:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb2c67e2d580b2ad17d6de4766ea5018821f410e94f6e448143ef2823d1e4c8`  
		Last Modified: Tue, 27 Jan 2026 22:12:00 GMT  
		Size: 145.2 MB (145224244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4dd7335e3171f59a8f7ecde98d06ad09b0a2edb4e0d88244f58d2a64ce77a`  
		Last Modified: Tue, 27 Jan 2026 23:15:04 GMT  
		Size: 150.3 MB (150310784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6edb4051416085a5acdf0e202768f291b6a8e736ecca0d2cbf7721f821e2b`  
		Last Modified: Tue, 27 Jan 2026 23:15:01 GMT  
		Size: 31.2 MB (31203382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce0d84bc6140096674bf2a8c80fc65917dfffcf97b953a2de284fde42a3e12a`  
		Last Modified: Tue, 27 Jan 2026 23:15:00 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe7ef90ef783c3d60b760ff5b98cca88ab5a5991b80e66b104fbff970998712`  
		Last Modified: Tue, 27 Jan 2026 23:15:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0f2573c12d3e6f6d7e44976e1e6cf296f0eeb3eb31064c261d00b8606e46f`  
		Last Modified: Tue, 27 Jan 2026 23:15:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:bc2e285dc292a86145f39ca5577f2e68fb87dfda86e017a68769ff5dfdf66ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f84a32553b85adc7ae7b537cebea1017264010d59305ebf11f179364ef600d`

```dockerfile
```

-	Layers:
	-	`sha256:7b038e00f54a792d1107974fc3284dfdef1c7ef57106e5bd024005eb62454612`  
		Last Modified: Tue, 27 Jan 2026 23:15:00 GMT  
		Size: 6.9 MB (6937770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92381560e15b5411e1535afe138f171a82b7ab9cd2125d3cfb36f921ea906b57`  
		Last Modified: Tue, 27 Jan 2026 23:15:00 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
