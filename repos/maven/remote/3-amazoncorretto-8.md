## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:941841930f163d928f93b70b3377aacff439d2404d861aec87120bf84b0127dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:2bd759d71349d3b9f69d55a3e77e98b13581689fbef1fb878a34420e16e48727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbb9256dd6a8a47c1b065abfb5e50407d6e971b30702f5fd45c83e0d2130037`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:05 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:05 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:05 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:20:42 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:20:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:20:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:20:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:20:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:20:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:20:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:20:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:20:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:20:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:20:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f778b828927a548aac19be726dfcfecc006ab044b72c43bffff784fd5318e`  
		Last Modified: Fri, 14 Nov 2025 02:15:12 GMT  
		Size: 76.0 MB (76043129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7039cc546664eccd84c1250b129009e79fdcd0a8117900d827fdc569440afcb3`  
		Last Modified: Fri, 14 Nov 2025 06:36:39 GMT  
		Size: 172.1 MB (172145983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0bb85d51e638bc0f9bdddc04a57457ae34f0227d5a06476ff37625754ae9c3`  
		Last Modified: Fri, 14 Nov 2025 03:21:26 GMT  
		Size: 30.1 MB (30055851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea3b16e552977f0defe4955b6794d9a3f129426f9154d6474865f0c52bbac5`  
		Last Modified: Fri, 14 Nov 2025 03:21:25 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356891acea557e749593968203bc6b55ef6a24ef2f29860a86c8cf7243d38c43`  
		Last Modified: Fri, 14 Nov 2025 03:21:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadc37e0e998e208ea7425a5b72d0d849804c939855041c863af0b3547a8a9f9`  
		Last Modified: Fri, 14 Nov 2025 03:21:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:4abf264d1ac5743aeb3376d46fb9498321f7d043a7e65b1df1c659dad4b1acd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5676c1acf4c576cb2b73962a178e33d001b4d0274eba0a40212219912412347a`

```dockerfile
```

-	Layers:
	-	`sha256:0d900afd38e3e352d9c555797274c2b7d6039f356664647a1848d120393cf4e1`  
		Last Modified: Fri, 14 Nov 2025 06:28:40 GMT  
		Size: 6.8 MB (6773614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99befbf57e8fcb184941ff5e82d848ad2b0be1ef8ef1bbf489c8d6685edb9c32`  
		Last Modified: Fri, 14 Nov 2025 06:28:41 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f46d53ad4af2e1d41b7679ed57f326cda69917d84c636700159ba7de55181305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313391748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442daeea08e5139feb15ae06bd7a8536566ff665e4059491637533df3f42b8a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:10 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:10 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:10 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:21:32 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:21:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:21:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:21:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:21:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:21:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:21:40 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:21:40 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:21:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:21:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:21:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c3f5dbd2a8b15f4cf535cdf778733a42929423d33a86e69f9714169993ae82`  
		Last Modified: Fri, 14 Nov 2025 02:15:15 GMT  
		Size: 60.1 MB (60119081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987f7638ed180518bdd13b56689bef65930739e128a18bdf9538067c451c6770`  
		Last Modified: Fri, 14 Nov 2025 09:53:43 GMT  
		Size: 148.0 MB (148028272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41d106604ab9c38f0a948905e035acf2b06afc35664cb98a83336a84adccc33`  
		Last Modified: Fri, 14 Nov 2025 03:22:15 GMT  
		Size: 31.2 MB (31207976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5289dbfd9848b90c0b47e0f4f36baa911a8d2788cc2c7b75e05af3276a7a347`  
		Last Modified: Fri, 14 Nov 2025 03:22:13 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e754a8b040f033cf86b07d7a602da1c4b642bd3ea13fbff4879388f14ab187`  
		Last Modified: Fri, 14 Nov 2025 03:22:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe79669b66a259ef237e5f6e30c6927f1ad053214c77dd0884f1546cd1efa65`  
		Last Modified: Fri, 14 Nov 2025 03:22:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:2cbc110929ff76de1e250d4f696c3f6f46745123789390c9dc5843be929d4565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdc3014f2192a4b455bca6d3d43b47e9955d145907338d8cd485f80c9bd66ad`

```dockerfile
```

-	Layers:
	-	`sha256:e5e4d1f366b1f943e39565b418855c957f93a632c8a68f568871b10b518187b7`  
		Last Modified: Fri, 14 Nov 2025 06:28:46 GMT  
		Size: 6.8 MB (6750811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21389909f554d71215fd010971a8384eba386d1945669c209d4b46c1945167f2`  
		Last Modified: Fri, 14 Nov 2025 06:28:47 GMT  
		Size: 18.3 KB (18334 bytes)  
		MIME: application/vnd.in-toto+json
