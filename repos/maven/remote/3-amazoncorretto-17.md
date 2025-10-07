## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:99fbb50221fdee89915f2fe6964e048d9c9e994927916970d35d9bc4a083fb4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:78b2ee865c5a4b05743dbb67eac767cea32a1091a1f3b47456466c71878f79b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423116606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483f5ae67e80f46b029e8dc99c14b054dec19b8f9d1c87b00309cb2d2cc2353`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:a4adbca9d9f02b56627c3ad67e0a0e0182143600b738530c0792731416f2444b`  
		Last Modified: Mon, 06 Oct 2025 22:12:28 GMT  
		Size: 151.9 MB (151850376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f33c600db40ec718ab516288b72086978aae658d5e3e9d755c2ab0270f47ec`  
		Last Modified: Mon, 06 Oct 2025 23:32:31 GMT  
		Size: 169.0 MB (169008545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1da5718844ad37cbd26e6c5e60d4513ccca3e20cd8393c9c6a70bba3137b0a`  
		Last Modified: Mon, 06 Oct 2025 22:15:07 GMT  
		Size: 30.1 MB (30073422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac28563303e50bb7e8cd4720d8945ee8b7b4065771df398e9fcd2a8c12222cd8`  
		Last Modified: Mon, 06 Oct 2025 22:15:06 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edb4cbf044cc904ea797f1dc70cac429df7cc3eb02b576cf7643d7e71e511e9`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05db79b2d04ed1c50135056cd257ecceaadbb48fe5fac643032167b8c9efa755`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:dd8f153dedf9227e7cfe57aa376e84e73321a71c1b324618156fdb4a67361d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0a504548d0be14667ed11d1f121a6fa7e324ae46eaf9628c44b2fa939b27aa`

```dockerfile
```

-	Layers:
	-	`sha256:a176d7dd73d5581405be698b2d323b1055983b771de8c0e14b462067ec494014`  
		Last Modified: Mon, 06 Oct 2025 23:27:57 GMT  
		Size: 6.9 MB (6929027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aea10a6fdaff220b703b585ad77d6e2d7b9f366deb71cc9662955d5d78f4d29`  
		Last Modified: Mon, 06 Oct 2025 23:27:58 GMT  
		Size: 18.2 KB (18233 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a129cfd1651f622c220098ac75a64cfea4b16f981d8218057ed429cb68246d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400543781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7534c4c9d12e21844d2bcee3da4c58d6bd8c9e20021825a91f9221e05c4a240b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:b6d7ee67b7d77597ca3941670c8058b1d1b4bf49f5ac9b63034650e0a0f9cf63`  
		Last Modified: Mon, 06 Oct 2025 22:12:37 GMT  
		Size: 150.4 MB (150393463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b9c7cb2f47dcc8460cf04c403d6a6f426b819496c136e4fe1c45f40a86f69`  
		Last Modified: Tue, 07 Oct 2025 00:57:38 GMT  
		Size: 144.9 MB (144928919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63cf178b789c7d3f88dd7cb3c15de3dc137cde7eeae1809bc37699e58cdbb`  
		Last Modified: Mon, 06 Oct 2025 22:15:06 GMT  
		Size: 31.2 MB (31184572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdfaf94d75625d9bf2c7c8362319253970b07aabbd0ea7f9c108f5588f2f3bd`  
		Last Modified: Mon, 06 Oct 2025 22:15:04 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997acff7c025bbd31993f8b3b7706dab7c6ef286d7ae67321e748301039736f`  
		Last Modified: Mon, 06 Oct 2025 22:15:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a213e0fba9f1739417526d3777f85bfb7afaa219859bd3035d56712d0b28456`  
		Last Modified: Mon, 06 Oct 2025 22:15:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:a5ea6a80f244cb86c4bb9dead248a48f1168278ab3d61c6de7e1fa0e00fd942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80c9cc0feb25be3c9b7dda054f62445e002b8528eb64c0bb414f844fd8e57f6`

```dockerfile
```

-	Layers:
	-	`sha256:4c1cf2cbf933e5dd4b1955ef29dafa803afd3a556b94c578dc4552a19d31e41a`  
		Last Modified: Mon, 06 Oct 2025 23:28:03 GMT  
		Size: 6.9 MB (6926426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b19f5e0564c697e3ab5f197b45fcdd13567ca8bc77de995bbb25faa293c8c6`  
		Last Modified: Mon, 06 Oct 2025 23:28:03 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json
