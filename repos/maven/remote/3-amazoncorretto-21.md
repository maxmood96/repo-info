## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:a1805724dbad65c8379a3e3843ab7161d05b66d6f5d3beb74a2159d1c0a5d783
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:d9e73da4360daca05d8fcf7b4fbb4406f4ab2fb1e35641c216ef55bb63c14e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.4 MB (443440139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5723859be85c23efcdec9e88c24ab131c47df9571aff20a2e59b4c22eb1c21`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:29 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:29 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:15:29 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 09 Mar 2026 19:14:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 09 Mar 2026 19:14:24 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:25 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:25 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bda24a0a1972d7430848f2e9c53e25d2db55ca3537798a384329ba70f9db98`  
		Last Modified: Mon, 02 Mar 2026 23:15:50 GMT  
		Size: 165.5 MB (165548489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281eb72583844ae8b6372b5a56c6280a4749774474beffbec9edf36734ac57fe`  
		Last Modified: Mon, 09 Mar 2026 19:14:55 GMT  
		Size: 175.2 MB (175161469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ce11acdeb5fc32b2e091d4dce8f38a3f3389329119b753417a0be2ccb137f6`  
		Last Modified: Mon, 09 Mar 2026 19:14:52 GMT  
		Size: 30.1 MB (30071389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774765599d1be8042b6d7ad8a301d969c2a57dbb483f10290d8b6df266192104`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 9.7 MB (9697521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9f03a4f2baf6f7fc49e5ebd04fd2c74cb0754497a61c95abbaf81e04866679`  
		Last Modified: Mon, 09 Mar 2026 19:14:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3867fe9466c8760a07f7d2119f43726b87b53e6d5544c057ccf2d6325b2a64ae`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:03ec768f3cc92a79379e266a756cfda09b346158f672dbbd71e119b6fa660ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371ef6f23806b8936987cbe3ca1adc2fcd139db10c81f4a12eb8b4bfd23cf302`

```dockerfile
```

-	Layers:
	-	`sha256:ee21796ea20f61144d52d01b3d9412a3701739bb24befb5ec1a9d320e0e01f03`  
		Last Modified: Mon, 09 Mar 2026 19:14:50 GMT  
		Size: 6.9 MB (6938641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3007b1cb87c8aa7dc2a9414ffbd76a9cf8b5189ed661550bb1d3b6b1c188df2f`  
		Last Modified: Mon, 09 Mar 2026 19:14:50 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:02650a2d7375279338cfa4cfd9f64031ea177857d8a62e5c9aa4f1eba351e73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420102321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca0b1b93dd11f78236b35d62c65b4903530280ceab0e680a1dc89611605b0da`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:44 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:14:44 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:44 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 09 Mar 2026 19:14:05 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:14 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:14 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa780b6d9640895d00c1754835e9116ebd6059e626cc1a1618dde104a8dedd`  
		Last Modified: Mon, 02 Mar 2026 23:15:05 GMT  
		Size: 163.6 MB (163606125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8660a8c380fb79b0f9f93297107cb26993d216ea900b5d98d60c8f26817bf581`  
		Last Modified: Mon, 09 Mar 2026 19:14:42 GMT  
		Size: 150.8 MB (150784668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002f9783dd8d9f575bbf72e2e5b311989930d4a3b2aa80ff06c400f10c5cc34`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 31.2 MB (31201523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a59ee9368878c09c72455947debfcf380763b8882b7a41e6fde667d3b804a9c`  
		Last Modified: Mon, 09 Mar 2026 19:14:38 GMT  
		Size: 9.7 MB (9697553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ffffd0ebc903471f53840d9d53aea03de1d53e7df88d2b8d3aa76efa79d80d`  
		Last Modified: Mon, 09 Mar 2026 19:14:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49864e79d999ef473db83be26ea2c72c61fd2307e31ca4c49e5026e1495dcc86`  
		Last Modified: Mon, 09 Mar 2026 19:14:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:8adb4234c66757d61cb0a9a907830ef37a0dbebc95f9a538cf320966ad291257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bc9250875eadddb007f7143020784459d4c0e29fce67f9335f44b0c07ea1f5`

```dockerfile
```

-	Layers:
	-	`sha256:0a1e46f406db1ce8cfd6b5aefa42349565d993c0ae70e9312800b84fb7d92892`  
		Last Modified: Mon, 09 Mar 2026 19:14:38 GMT  
		Size: 6.9 MB (6936040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e3f68b07f5c1847a2f09b2484fd27571d523c410d33f8f7289facc445839d2`  
		Last Modified: Mon, 09 Mar 2026 19:14:37 GMT  
		Size: 18.4 KB (18364 bytes)  
		MIME: application/vnd.in-toto+json
