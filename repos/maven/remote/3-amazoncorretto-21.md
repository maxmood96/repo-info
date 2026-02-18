## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:22cd2d8f18db7e8932beab8c2870d23d157d2472ebec0aa93d4f531a3f0e52a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:f79584091e613e1234ad5e95e820f73ad955e020d3f577dd5675b015af033d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.7 MB (442660439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea81b95861e33e325cf92fd81a31a57dd6a113ee3927cfb800a8033a746b0f11`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:49 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:31:49 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:31:49 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Feb 2026 22:29:42 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:51 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:51 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3745b42022da445724f2547e61ae0b2dc6b897418dde7d9377a2fb3f5b48d3`  
		Last Modified: Tue, 10 Feb 2026 18:32:09 GMT  
		Size: 165.5 MB (165548198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fcb48fc243c16fc84eab88897b94ac6a3116c8180ea326f9fc32bd271d3b8f`  
		Last Modified: Tue, 17 Feb 2026 22:30:22 GMT  
		Size: 174.8 MB (174757071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23963f6c41a215d809c4fc98bd9e0b2941833b2d1673c4f6024d75197da6af39`  
		Last Modified: Tue, 17 Feb 2026 22:30:19 GMT  
		Size: 30.1 MB (30082932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effaf1a89c365073986aafb14617b4a09559f59f7cecd131fe3a67596cd9a5fa`  
		Last Modified: Tue, 17 Feb 2026 22:30:18 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d4d062c741053fdff0256187731097b4d294cc88df03ec58a0a19d0b10394a`  
		Last Modified: Tue, 17 Feb 2026 22:30:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649426242f44922825bc5cd8c7e24a0cee25c922341b72507047a21e0c1d8e2c`  
		Last Modified: Tue, 17 Feb 2026 22:30:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:08d82cb7c4bbafb9f15067233ede7ed78141829f459f1c743c3b55ac6d76d0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5590cfdefc5c22ee4f3c15cd1ffb2c2a5e2f38b480515769e382752b7fafca1`

```dockerfile
```

-	Layers:
	-	`sha256:615b599f47687ff38db3d9ab3f9a11dea3de3937dbd1e65047e5b0ce1bd0d981`  
		Last Modified: Tue, 17 Feb 2026 22:30:18 GMT  
		Size: 6.9 MB (6932164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e4ab1b88226134852410201f17a94834784b243f4a3ec17b083afe2e8ad68e`  
		Last Modified: Tue, 17 Feb 2026 22:30:17 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:dcc660fd8cb305495cc156b7dd10fa110e5b130128edb616781be6843b971db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.3 MB (419326085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13e3cf00586bed8d7326aded84e70d7ba04ad0d5e94707244c63415e4e8298`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:44 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:31:44 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:31:44 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Feb 2026 22:17:52 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:00 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e50ffd073f08c33ad517c912c06075cc5cb34829d2b2b85c9cfa28d50726889`  
		Last Modified: Tue, 10 Feb 2026 18:32:06 GMT  
		Size: 163.6 MB (163610743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce27ee9235d81b25e0ca2a4841359585dfba38412f11d259321685a6d4a15b`  
		Last Modified: Tue, 17 Feb 2026 22:18:29 GMT  
		Size: 150.4 MB (150410471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea279ba91bb888f272e06df062bb264f4817b7f9ec6805712d7ff7aed8f6b9`  
		Last Modified: Tue, 17 Feb 2026 22:18:26 GMT  
		Size: 31.2 MB (31192113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeef2e038016c7993c58ad1de5046f7f6ccda2daf6025cdc344351b068cbf7f8`  
		Last Modified: Tue, 17 Feb 2026 22:18:25 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351252d36a1acbef1bb0fc0b72e2e6ecb9f8f7b89606977e61fabd1e68881046`  
		Last Modified: Tue, 17 Feb 2026 22:18:25 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9e7cad499714385b0f7765aa6d4fb2e83bdcd4247c3ab9b6a050847f7cac7e`  
		Last Modified: Tue, 17 Feb 2026 22:18:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:b8adea94cd70e2288b8925c5ee2e9f71a43d8d16b079405eb6e63d8693392fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c069b8f0b9fb62537f5ed8e85988b9608aee66f3425bee70138aa157febc63c`

```dockerfile
```

-	Layers:
	-	`sha256:3c1c8ca65aaa145a61030701dad55656f93060ee076f279f0dd248b13e08a94a`  
		Last Modified: Tue, 17 Feb 2026 22:18:25 GMT  
		Size: 6.9 MB (6929563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1086d995c52e973d2c82880b1f26db2dfeafb9465886bc618dad08409520cd4a`  
		Last Modified: Tue, 17 Feb 2026 22:18:25 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json
