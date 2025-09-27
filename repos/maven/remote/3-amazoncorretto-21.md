## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:99dbe2c7ef98e032bb09cf1e4bcd3561fccbac06cd03fc1c5a4beb5f8d4aea20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:72719e54fdcfdf32c712f95339e0711ec8778e170db8e1d449cfcf617dc6db97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435432400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf63f0bc8e1710cededa0e5009ee3883beec7c91dd00d20e1aa122cdea9b9dd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
ARG MAVEN_VERSION=3.9.11
# Sun, 21 Sep 2025 11:32:02 GMT
ARG USER_HOME_DIR=/root
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 21 Sep 2025 11:32:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 21 Sep 2025 11:32:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e750caf8f1aace6b2a40b4d03ac34238ad41147f9852aea71ac3fd0f305ecc01`  
		Last Modified: Thu, 25 Sep 2025 03:16:04 GMT  
		Size: 165.0 MB (165044322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32051578efb97987fdda6c62bfe59653b56f3bd1dd7eafa2494908bda49478a4`  
		Last Modified: Fri, 26 Sep 2025 23:33:24 GMT  
		Size: 168.1 MB (168136280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e51a91d785da30bc91ed3ce8fad97a20e3e88da674c499bf0edb06ab63904e2`  
		Last Modified: Fri, 26 Sep 2025 21:36:05 GMT  
		Size: 30.1 MB (30074340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3ab7d8760c35d66bd886a273cdf67a76e69fb5289122c36ba29b72c3e55c0`  
		Last Modified: Fri, 26 Sep 2025 21:36:02 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9c4f42d6f648ec8c64c21809b5ef7bd3e44eb47288c0355daaa616d29ce9f1`  
		Last Modified: Fri, 26 Sep 2025 21:36:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f458153e4b26399e390fc9938d9a9da17e9a69254833c0a98a4a31c6c4c3689e`  
		Last Modified: Fri, 26 Sep 2025 21:36:01 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:3a468dac0dfb93d2d8650acce81ac16297ff1f830f67ea87822b2e650cdb3e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09919f206fa403ca816ab94ea473811a59cf4fb5c28dc30020c81c845336b67`

```dockerfile
```

-	Layers:
	-	`sha256:cc61c6ffcccaa596b28aac67929a186a2a7bdea4555e7bd67b8c8d998f5d4c72`  
		Last Modified: Fri, 26 Sep 2025 23:27:49 GMT  
		Size: 6.9 MB (6928924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bff7283ee99aa557f3f5059da559bd6ecfd15e1a85bbc0aee64e675588d563`  
		Last Modified: Fri, 26 Sep 2025 23:27:49 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:479a76822de1e8364f9b1592e34a3088fa870264093d518e512030637ecef2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.4 MB (412382056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9231413b41cf47839d50dc8e5dc93074d9c6e5177d3a8632817bd03f97e0063`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
ARG MAVEN_VERSION=3.9.11
# Sun, 21 Sep 2025 11:32:02 GMT
ARG USER_HOME_DIR=/root
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 21 Sep 2025 11:32:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 21 Sep 2025 11:32:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c868e5c107db6ab89ab40ef0c51c4a502a10ecc34ea2109f2dd64bd446a85`  
		Last Modified: Wed, 24 Sep 2025 22:12:58 GMT  
		Size: 163.1 MB (163112265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ef0624eef05ded2b93df65e44f5c0bdf715ff5a9a4ebfbf87cbefb772502e`  
		Last Modified: Fri, 26 Sep 2025 23:33:16 GMT  
		Size: 144.0 MB (144047784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb591d945063c5066344f72a81dd55498d0501201a0e844d09c08868103e3e96`  
		Last Modified: Fri, 26 Sep 2025 21:35:26 GMT  
		Size: 31.2 MB (31185240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe107cdd088f4fdc0052130d0b4486c2a361095e2582c2f5d9b86a029ac6531`  
		Last Modified: Fri, 26 Sep 2025 21:35:27 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9f1b08f48c5e7998be969e19bfe34d7ce092b751e94fd78d0c6338ae59ac3`  
		Last Modified: Fri, 26 Sep 2025 21:35:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfbfd4349d0bd4f05cbe4896ce2128138d68021673cbe01ef9fe0325b6b5e62`  
		Last Modified: Fri, 26 Sep 2025 21:35:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:8dfcb2d7872478f93b01d019c32554334aa3364e23af4ac30e438b5e3eca1831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8cede8bb229c45e6f3128a9f16099e54cd1e553afce5cfb27208c734e23577`

```dockerfile
```

-	Layers:
	-	`sha256:76ed259916aff99efde3a85e53ffdec36c2bebc88dd1e4ebc8243fe2872b6416`  
		Last Modified: Fri, 26 Sep 2025 23:27:55 GMT  
		Size: 6.9 MB (6926323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832ab759223d61e663c46988d930d66ab3b2fc3215b6e33d4527fdcf35919396`  
		Last Modified: Fri, 26 Sep 2025 23:27:55 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
