## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:d9bdcc1b4eeef952706cfe4a648f2f44ee23894172c49da18381de0b157f389c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:b655e68cb20e022cacd4ff7132de1ccd85fcfd12338c3a761a23fe1d17a79999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.6 MB (412648811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e952b7433fd56c4d8fcee111fb0f6f52d8eea9e71029c829254658cbdd5df42c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efd55bb89ede17b069b01bec9bc2b63844e33bdc8fa87af7ef6ec754145581d`  
		Last Modified: Thu, 03 Jul 2025 23:13:08 GMT  
		Size: 148.3 MB (148300702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaf5a7dea275928a52c30a4d1629f3ee0baa54ed4d577f441ced41f7851e340`  
		Last Modified: Fri, 04 Jul 2025 02:31:56 GMT  
		Size: 162.3 MB (162341302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05208fbb9caae6350dc6f55528908eca098236dc35abc156c2b1f6d3d5f2adb6`  
		Last Modified: Thu, 03 Jul 2025 23:17:53 GMT  
		Size: 30.1 MB (30089525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e6a2e340357f9d936d74d957ac56d0e2bad091c8208c972a73af1ea01a7630`  
		Last Modified: Thu, 03 Jul 2025 23:17:37 GMT  
		Size: 9.0 MB (8953385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4702622a6512c08c48bfa36fbe697f5f31a687a16349715d7c25a0e43775fd02`  
		Last Modified: Thu, 03 Jul 2025 23:17:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38d2505d4a0f56bdaa610c0f6023cc8f9e0e722a2f96ae177d7e80bc326ed51`  
		Last Modified: Thu, 03 Jul 2025 23:17:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:ef4fb3009b25da580116dbaf6538275146faa6604208c5a29cfd60a3b008a3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd5a0a8eabaec965a96fac9b9a3ebe001212271e8eb3810edeef4c4cd8e430`

```dockerfile
```

-	Layers:
	-	`sha256:106b531fe22ccf2696d3c070b9f32ac60e7e36b5a3fa09e5d85c6e3ce95a0bcc`  
		Last Modified: Fri, 04 Jul 2025 02:27:23 GMT  
		Size: 6.9 MB (6933771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614844e8674b898790c4e1c39e7bec224b9f9a23d26b111e6e430e5eb0ff2874`  
		Last Modified: Fri, 04 Jul 2025 02:27:24 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:667e2f69310d0bbbf66198118234272c9d7becd10f808f3693e6a7d507c7602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 MB (388491321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b41ec6497b4cc84d93a9f8119d7d88d5f57f04c4d0c7d4fb8cc1eeaf24f232`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:409bf1beed8b3d18aa6739b3b654d78ea6e9842b177c58b3fde860845eae1b51`  
		Last Modified: Wed, 25 Jun 2025 19:30:21 GMT  
		Size: 64.8 MB (64794781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb4ed8902fa0220eda72ba31edf75cbe4589d65ca9caf1cc2e11165188cb57`  
		Last Modified: Fri, 04 Jul 2025 03:50:31 GMT  
		Size: 145.3 MB (145335444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b80e9c78aed903da3317e305dfdcc0cfdd5f1a8d7449311c26eaff17a36aad`  
		Last Modified: Fri, 04 Jul 2025 11:53:59 GMT  
		Size: 138.2 MB (138228510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7131c0621c0f39625c7240c68f5d0f75b49d75108ed40b04ecf7afa82c661a4e`  
		Last Modified: Fri, 04 Jul 2025 08:13:18 GMT  
		Size: 31.2 MB (31178160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7232b7d3f0db17ce86eed717332ce057a1526708335b793e33cbe262b30ea`  
		Last Modified: Fri, 04 Jul 2025 08:13:13 GMT  
		Size: 9.0 MB (8953385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8102477da316f5595d5a63808a26e9b08e2c4b4af65b079f8fd22b9db96f29c`  
		Last Modified: Fri, 04 Jul 2025 08:13:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ece3c1373caca06b8249de3250a0106d54e18cd99fe37fd30182fa4f099848`  
		Last Modified: Fri, 04 Jul 2025 08:13:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:968e6e56f51304304902af3fa410e359f10398ab2bff4ad0996ae965f715ea20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271bd662fa6bec48f4ff93a05725e5b455f2b37068ccdc35072303895fdc2179`

```dockerfile
```

-	Layers:
	-	`sha256:43fd8c7f929baa01a3296c6802832889fc255341d19914a5b1084494356400bf`  
		Last Modified: Fri, 04 Jul 2025 11:27:29 GMT  
		Size: 6.9 MB (6931975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c3b57e55a5e03b094c2eec441f553d9465f0b407864da67928d0b771e75ed2`  
		Last Modified: Fri, 04 Jul 2025 11:27:29 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json
