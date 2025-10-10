## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:49710eef8a936d5e8df086227124dcf0ea639998f8579fad4b229ce878dd27d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:a0e0dcf6cb3c3e35044bbd60bc68a9df7871f2437c7f2288da42d0859f73c752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419619879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404d4f13bb5513b9aece78e38064a8fcbaaf80df1b8d44f4a4749567c255b5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9b18b72b93cc14d31fcd5ae947987b35e6e81f265f08584038b95dc7093a`  
		Last Modified: Mon, 06 Oct 2025 22:12:29 GMT  
		Size: 148.3 MB (148297178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86db470825a446b27fe14a99bceebe79aa47d3a4bffc701300c932223a32ab7d`  
		Last Modified: Fri, 10 Oct 2025 05:37:55 GMT  
		Size: 169.1 MB (169069945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e7bcb7ea45c8b510c76cb6d8e5e1ff1a13f5fa73f3b6168cdb887f1e7cc6ed`  
		Last Modified: Thu, 09 Oct 2025 22:51:35 GMT  
		Size: 30.1 MB (30068507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82680d9d5a1c36bd2011e5fd149781f5cca8b6c1b9a38412f577c8715bbf6f51`  
		Last Modified: Thu, 09 Oct 2025 22:51:33 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfd690375f7c73f531a5ddb7a41577332712a4cc11470557d69ae4a3fd7e8b9`  
		Last Modified: Thu, 09 Oct 2025 22:51:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a38f6a10d9c7254fff36da83eaf119ea1007300cdab3db18c7d9c88d237318`  
		Last Modified: Thu, 09 Oct 2025 22:51:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:a371edea56908990ac6bcf3716f34bbd7877b79180c67c79ea108ca893d1a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c96e6f46142c18bcdf327d49e16bcd3287fdd6f9067b21be77ebcd00fd7255`

```dockerfile
```

-	Layers:
	-	`sha256:d52c3769eae7a5237e135bdf1b00ff8927c183d528d35865248b77403d19973b`  
		Last Modified: Fri, 10 Oct 2025 05:27:41 GMT  
		Size: 6.9 MB (6936332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6334e5d7b7179fbea51e6f0a049da77aea554e11bfffb361dca0bd02b7445bc`  
		Last Modified: Fri, 10 Oct 2025 05:27:42 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fceefa4b1b9e1635d9b325efc7daa0bb5df14c454c927b18fa89d8f5f2215c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395566806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2982e5f929be32722c2db859ea203c3e8ce3d8b11a41a089f21aa6c5ab753e5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18f29a76c4aa2e6026e14aef8f8ac084f68d3ca8907802097cb0996a18302af`  
		Last Modified: Mon, 06 Oct 2025 22:10:55 GMT  
		Size: 145.4 MB (145372603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c0927072863907b5f317f5f19cd7e1b6560150887d1a09f837e67e2235b4f`  
		Last Modified: Thu, 09 Oct 2025 22:54:42 GMT  
		Size: 145.0 MB (144967269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e9933d7c12a35c156896c4c5e9f604d88a4fc60fd0e76903fc2eb901421aba`  
		Last Modified: Thu, 09 Oct 2025 22:55:02 GMT  
		Size: 31.2 MB (31190100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44c12014f5cf0ae5c62ce1f26240dd62fdf02d4e7bf0e8ea6b1e76cc0d9cf68`  
		Last Modified: Thu, 09 Oct 2025 22:55:01 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5052a79322611ba4ff96f6eb43e8d45c56ac7f68aa17c4c26fab0864e81881`  
		Last Modified: Thu, 09 Oct 2025 22:55:00 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e1c4360697f80601b192425e9ad5b7e79a7dd4251ae5dc1de657f9998a5e25`  
		Last Modified: Thu, 09 Oct 2025 22:55:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:362729d1eafd2b83fc6f8c50fd5a7f347848e2afef345055a90dacd68f9dd7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9387fdf222f0c85ea1ab164255b01e8a1fa01623df4797082421fd46fdb0`

```dockerfile
```

-	Layers:
	-	`sha256:c311353d2a7fa60cf322cb9dfe78c3f47cb0b1eaca53fdd12c509bb3ccc7e113`  
		Last Modified: Fri, 10 Oct 2025 05:27:47 GMT  
		Size: 6.9 MB (6934536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3481ac18d56ce649e0b31b171066fd03c9e095a9a49b77522f12453d5e5ba26c`  
		Last Modified: Fri, 10 Oct 2025 05:27:48 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json
