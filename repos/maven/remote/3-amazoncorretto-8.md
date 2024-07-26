## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:8d0b3bcd6f416127e0f7c6aee4f5ccb5d4091af23bb8aefc8186436d51bbab52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b9c4c012b9c09ec4c83a69cb36cd30da2f3f0340555c4f4eb43f55cfdf274aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292878554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fca34dda8845537057d984a6dd5969bf5034a06a3be2d45b3c005eb84be848b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_422.b05-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba3e469516848c9e5827a5c193c9649717e5fc70dc9e65985a1ab4065891012`  
		Last Modified: Thu, 25 Jul 2024 21:01:03 GMT  
		Size: 75.6 MB (75568332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf714fdc7b98433b68fb6348b1372d98226e3607230bc0328c0ed1ef53b51b`  
		Last Modified: Thu, 25 Jul 2024 22:00:59 GMT  
		Size: 145.5 MB (145468203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee900f67db0f8d50d276584539b078139aa05d581f6fdb99293352bbbb6d5d31`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 9.2 MB (9161812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d67e2edf295da41a7ceee7bbd107d49b9e05f4e18942304b4ac47e5fd9f75`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0450f50869147e83b4242939f5c2289b76e5ab2b4781714e4f50a72351d64480`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:ff35adb1f354efe59e452190dfd2dacd07ed0042dbd3fe93d2cd59dbb110c441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5500645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd6b8a394220e624eca2300e0ef1a39f63b563171a0f91e2bc7aa4b389fcf23`

```dockerfile
```

-	Layers:
	-	`sha256:dd2aead8ff0d400b3ac18245ff9d02d7dd36ab3082ee542c77d8941afc0efd1e`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 5.5 MB (5484370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d46dc4428e3b95ba9efb578e1546df6a3f72decd05fb5c91a31142d6e90a738`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f36aee17c947e558a2589109ffa60b8f9d86eb619730a5e17c2776582e42c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254836076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30fe5c3dc725ca3c5e45e986540fa8939941acc093f37ad49c8bf76da0402fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_422.b05-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
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
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1a293592675dedef36879a73d5ca3a5f38d1373c13888a09927e61b13d983c`  
		Last Modified: Fri, 26 Jul 2024 01:46:03 GMT  
		Size: 59.7 MB (59656039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f94a31d7a2d2790445da8177b152e322e71b2f21befb5aa095564dbd3d24aa5`  
		Last Modified: Fri, 26 Jul 2024 02:43:14 GMT  
		Size: 121.4 MB (121444514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68939ab96277b293fb53ca663b9fefb7a605a3c9d419ebd41aaf7e57d62ec10`  
		Last Modified: Fri, 26 Jul 2024 02:43:11 GMT  
		Size: 9.2 MB (9161778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213538b0e0e4e8cf05aac0e837b487270879e3f7c8d45464fc0d39e7f0fb97d3`  
		Last Modified: Fri, 26 Jul 2024 02:43:11 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44686d61c75d3eb08eaa108641290fb0d6947d5ad619ec2a2383b18ac0a93cff`  
		Last Modified: Fri, 26 Jul 2024 02:43:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:e5aaad5c88e21b0202999e45c82745315ec8ec235ebdafb0e37c02b4bb00d475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5479845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61ba6cafc13c09f7f21438911bd88ec13eb22fed52ca738356faf9e72285a9`

```dockerfile
```

-	Layers:
	-	`sha256:7e4509196949f6074900a1b114acafefdd37f81b9bbb3f0b956dd834ad77abb3`  
		Last Modified: Fri, 26 Jul 2024 02:43:11 GMT  
		Size: 5.5 MB (5462845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381b09fdeb6e10e4db4c56b084f15ac2102d0bdffdb7388d7b179c27f41e14d6`  
		Last Modified: Fri, 26 Jul 2024 02:43:11 GMT  
		Size: 17.0 KB (17000 bytes)  
		MIME: application/vnd.in-toto+json
