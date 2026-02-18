## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:41e7d096085e6458fd8bf07c101c24b787b4765c4e304219c08ef2d7483fb00c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:b024f85af7b98e1d7967a41edaf42e1b1d48471cde2d76ebf7d2388562d3b6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429563056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07654666e82370c32cbd3b90dc08aff84bbe87525d6de3bcef470e836bf58e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:06 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:06 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:31:06 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Feb 2026 22:29:19 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:28 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:28 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73256cc0e9932fbfdb9e2c31c5e1d9ac875dc40ea799d030328cbcdecafa64cd`  
		Last Modified: Tue, 10 Feb 2026 18:31:32 GMT  
		Size: 152.5 MB (152453837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3c6266a8ca60e871c11e848e05c8e4fa8130efa9834e30e848c7c6fd698b3`  
		Last Modified: Tue, 17 Feb 2026 22:30:00 GMT  
		Size: 174.8 MB (174755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943ebfdf2c4bc3902a28f3155180c536348ceb81920338c515bd131c9e2cc5f1`  
		Last Modified: Tue, 17 Feb 2026 22:29:56 GMT  
		Size: 30.1 MB (30081381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4486d2136bb35130fd509fb9164e071bab50e279acc3b2899bea479061123e`  
		Last Modified: Tue, 17 Feb 2026 22:29:55 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97eca4c5a14b32b003f739674b36c7bb0b12555904dc0022f906d1738bafca2`  
		Last Modified: Tue, 17 Feb 2026 22:29:54 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a073759f487a2fe92c3592e4626e1d69182e1f4bd8cc5a0e262df1e5e5db8b5d`  
		Last Modified: Tue, 17 Feb 2026 22:29:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:c8142b1c73cabc38b2f60794b16c6d9982f53e74a719c208ba8b35f2c1b19703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04de83ace99c2adba9ca790c794ef22b35cb7e5e7b8c0e990aa237821d85c8`

```dockerfile
```

-	Layers:
	-	`sha256:a310dfd792fa173e3c60bd83a614d0e2b0442568fb33bd2d6f4e83b82903f9f8`  
		Last Modified: Tue, 17 Feb 2026 22:29:55 GMT  
		Size: 6.9 MB (6932261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb23e901249ed51b1bd58c9e368284e86e5c01998388aa4c068534fe1cd06437`  
		Last Modified: Tue, 17 Feb 2026 22:29:54 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:28840f63b27670108c9a3bbb234d032bc193ab4ea28a932197c919f3246dfed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406706266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddc8ad388d9fbc2426c151519b68c23e3d67c8f2f7dc13484bd33590475ee6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:51 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:30:51 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:30:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Feb 2026 22:17:35 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:17:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:17:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:17:43 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:17:43 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:17:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:17:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:17:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf7fc59d4f0d0db5bd751c7a35eafd6f68017e74991b9d8acaa22b0112d204f`  
		Last Modified: Tue, 10 Feb 2026 18:31:12 GMT  
		Size: 151.0 MB (150980156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1a3ab9ff3a224ddacff1d081fe10094d715a6ea7fe43dfad2ca29daada2e4c`  
		Last Modified: Tue, 17 Feb 2026 22:18:09 GMT  
		Size: 150.4 MB (150409739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4258a98ff2dd480d1e147eaec83e98885fbddb86520aead367775389717fe42`  
		Last Modified: Tue, 17 Feb 2026 22:18:07 GMT  
		Size: 31.2 MB (31203608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6430d2bcfc92e36d029fdf2915c18f2bbd14ada7138b465bf69d49f513a87d`  
		Last Modified: Tue, 17 Feb 2026 22:18:07 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc01126e7ba57388df23d53a7174c671f2cab367eba959851bca41744487267`  
		Last Modified: Tue, 17 Feb 2026 22:18:06 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c6996321a4ac4f9ad21150a3ced2845a2458d8d3ebe21cd18b6163ce896b8b`  
		Last Modified: Tue, 17 Feb 2026 22:18:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:f545186f2b838fd61ed3a6d55030bc63a01d0fafe09a6ffbe086c1bbd2e43696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef70ca3a576bfb69ff9d48109b5ccd7ca6180def6260f5b806cede61528d5ab8`

```dockerfile
```

-	Layers:
	-	`sha256:5b3d1c5060725546940e87532981532e655b99c67023fbbd4f3260582a9362a4`  
		Last Modified: Tue, 17 Feb 2026 22:18:06 GMT  
		Size: 6.9 MB (6929660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00b4d8b8a08941dadb59888cdc72f7851135c06571735c7114e0b9149ae1af2`  
		Last Modified: Tue, 17 Feb 2026 22:18:06 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
