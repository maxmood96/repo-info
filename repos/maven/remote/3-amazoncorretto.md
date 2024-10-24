## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:0e97ddca54bdfc40c4cbe8fa7222607212517879b5dde9a552435eadd4923564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:eb32d22ef9235703209845efffe7d3f6e9c747250e58f0b8ab12d13b969bf611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403577067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc08e48776abbb4f2fb71650c5ce221e42386d4a9d563996ab9404c787cebaf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
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
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66244e4b15839e8eabcae9bb42a203318664f4779635534564952783b057030b`  
		Last Modified: Mon, 21 Oct 2024 18:57:01 GMT  
		Size: 151.6 MB (151614974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ee2aeab3836878211655b94b1dbe968cf2fb641c3b9dd490a20cf29a710d7b`  
		Last Modified: Thu, 24 Oct 2024 02:56:20 GMT  
		Size: 150.0 MB (150041989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6894d0fa56ed52d8d8e9fc20d162a4b3cac9ff34eb1511be7f8917d2b6f5a560`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 30.1 MB (30069086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e078f1d624d6f1524e6a11525dd43e33211d838b361aec04bfa350279774f`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773bd9c45d3be94c98a0e8b573a4a99ad043753224765cf993a95841de17518`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57274c8edfa0031cdde44170725ecbafeef43eea9c623e15045f8fc590965631`  
		Last Modified: Thu, 24 Oct 2024 02:56:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:5ee68f449acd93f6153db04104e20c1ba27a251ccbf3f912930215d6ba4dc3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6942661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc81a2f71d33439414b3aab7692c5356355c0101cd3329b088980119d791478`

```dockerfile
```

-	Layers:
	-	`sha256:16a9ca6799cc9ac800419306371b77705ea4dd5131e8cde095eb8b5308f546a5`  
		Last Modified: Thu, 24 Oct 2024 02:56:17 GMT  
		Size: 6.9 MB (6923159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37da8f0830ba07cfa6479174bef17a315a731bf8bc7bd216f18a2daa5bde0f07`  
		Last Modified: Thu, 24 Oct 2024 02:56:16 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:92b7aa809939d321d59108cec8937bbccede831608482593b612491a0fb53c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381280637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef15a2ef41df8fef2a78c9398b2ff38d89d2587f3ba6417131b9722e46e9e64`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
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
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b0d2256b215b37f265efa060f7500e983c3d10f7b2dc68ea4119590267fe8`  
		Last Modified: Mon, 21 Oct 2024 19:20:16 GMT  
		Size: 150.2 MB (150238727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ceb02d4a53fb89d8f0eca59c1bd2d1a67815e2eee5eca86de214bd25d1f239`  
		Last Modified: Thu, 24 Oct 2024 13:19:09 GMT  
		Size: 126.1 MB (126098156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea58b9780e37d7f04471bbb24aa3c6a823866f92cd00def6b23d6f6553ae6a84`  
		Last Modified: Thu, 24 Oct 2024 13:19:07 GMT  
		Size: 31.2 MB (31185192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61943a51f0b8e875f84ffd3b07552567c38edb21ba8356f1f65938040394b455`  
		Last Modified: Thu, 24 Oct 2024 13:19:07 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6feb14e1dea31ab1bf325a50e1e7d78db72be5368e1f4048787279472efbda6`  
		Last Modified: Thu, 24 Oct 2024 13:19:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793aa5945c2cc2e6db5822a9455fd227deead8e4212acaf70f4bedd462b47868`  
		Last Modified: Thu, 24 Oct 2024 13:19:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:d8e772a032cd4f872cd60c828071402bf5a2d24ab42e4a9ee844739936008e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6940300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e9713e0e0dcd2890145f81b12591a059867a972112bd45425b48b56f9e431c`

```dockerfile
```

-	Layers:
	-	`sha256:7e0012f9e5898c62f58985a46a77f575374f7607a687812b3e7c4f78d60ee4e6`  
		Last Modified: Thu, 24 Oct 2024 13:19:07 GMT  
		Size: 6.9 MB (6920602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f221941de883feafd21eade2dc61492a2dd1aef20a349f8f17e9f85f2281b6d9`  
		Last Modified: Thu, 24 Oct 2024 13:19:06 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json
