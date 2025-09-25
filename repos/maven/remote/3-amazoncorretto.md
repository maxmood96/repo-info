## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:76e3de06610e5a792df1c4163e06f52643c923322135bf30d1b5caef361f45c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:080efa8497890adc4f8fd1c04495600e6d4e58c90839490a2daa354c730bee56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.4 MB (421404515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a085e51e76b6e4a28a1f73f22c949b071fd6406451246ae411820501e9ec68`
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
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9366c5e7bd5a6d2a9b3c3bd58e67cb4e92dc15ea766d757f065f39f426a045`  
		Last Modified: Fri, 12 Sep 2025 02:10:25 GMT  
		Size: 151.9 MB (151889560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c43ab44b5673d9c240bc67fc4374d9bdeb273c6e898e96a9d7030f53e0b31d`  
		Last Modified: Tue, 16 Sep 2025 02:32:05 GMT  
		Size: 167.2 MB (167168725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075fbc57b5dcafc0bc574ce13f39d394e770cd58f58ed758ab5625fa43e425a`  
		Last Modified: Tue, 16 Sep 2025 02:32:00 GMT  
		Size: 30.1 MB (30119329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaabf4b4af9ff8c7ec3bda6b48d5de3ca29dc22ea9a976f4da766319f0d37ca`  
		Last Modified: Tue, 16 Sep 2025 00:51:21 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4509ac7afd3461aa3c72d6774fce6711581b81fb7dea0e9942e272e1ccb86f`  
		Last Modified: Tue, 16 Sep 2025 00:51:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23adb5bfee953f468ee4b2f04956d14c5b45babca67f79253f5df75aa5ac81a`  
		Last Modified: Tue, 16 Sep 2025 00:51:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:47df526e84ac81b05b0c32c474021cf3503ae6bb2383f4ff43c7f0e64f8b4677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619314caee9737cac03dd317868d24f878251eef00041c79903094c01c1605dd`

```dockerfile
```

-	Layers:
	-	`sha256:8f8c416e1d57d38fcf35ca43ae5660212cff990f8abe940539dbe444980c9b5f`  
		Last Modified: Tue, 16 Sep 2025 02:27:38 GMT  
		Size: 6.9 MB (6930301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f1b89ee5c5ad6aa7ac81da3359265be2fea053e4c79ba1fdf50b732e9e9eb7`  
		Last Modified: Tue, 16 Sep 2025 02:27:39 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1d2a0d15dff7658acd69816dc6398e0e42f66f898dfd048dfb683cbee0ef012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 MB (399660445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a8e7ae089890dc769ddfca90430a8b0aaebabb4ed57ee56068ff1d6987dc6b`
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
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5799c11fcb9bea8c5f9b4a5d739394e37910fc3fdaeef7102c5e1f03bf0c50`  
		Last Modified: Wed, 24 Sep 2025 22:13:02 GMT  
		Size: 150.4 MB (150393249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8e4e195af9665db88446a3437a983a42c512b43382b357b2cce3ec2833e8ed`  
		Last Modified: Thu, 25 Sep 2025 02:42:27 GMT  
		Size: 144.0 MB (144045602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ba28d2c2f2396b8babcb0bd4d69aa17ab2ed4cde2fe07f0f963b8a11621e3c`  
		Last Modified: Wed, 24 Sep 2025 22:15:18 GMT  
		Size: 31.2 MB (31184824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76d2c6533ff8df4be022eb41fd765aac6057887ed57a54524bf2ab6834ab609`  
		Last Modified: Wed, 24 Sep 2025 22:15:17 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcda723b908666866b370f944dc4e6757fb6a575f69235d252ace68c9aed905`  
		Last Modified: Wed, 24 Sep 2025 22:15:16 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d818f1c48a8795aab0cbaf8f49aed1f2ba60a2b75b49abfcf74d1d27075dc70e`  
		Last Modified: Wed, 24 Sep 2025 22:15:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:fc7175f343aa450108a58eecdc9ea48140972d2a350b0ce71298c99333197f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c523470ecfbf326688faf9698612af6e7c42917896080eaa72d81504f0c2be`

```dockerfile
```

-	Layers:
	-	`sha256:6cd4f3cf550cd7fbd760e8468ec45baea8d6aaecdd4befd132af098cb9ebcbb8`  
		Last Modified: Thu, 25 Sep 2025 02:27:26 GMT  
		Size: 6.9 MB (6927748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f61ff123b0b1d22f9d917af2b7e332f80a8698747929ddd129c60b11a3f012`  
		Last Modified: Thu, 25 Sep 2025 02:27:27 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json
