## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:d5efcd3f8e85e3a2d308afe4e7e38455700130a2e0463450dbc68b992540e0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:d976e032b97168c20a0779be4f4870955cbaaac158b1db36ef54a0930086f356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.5 MB (412458974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744da89719a8a510ddd1dc6d0a5e65a29218939c3800980cbf2d46ba6dd73a67`
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
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94257a018d3e9f5772f6e6292800ef2aed5b403abb6991c7db7841d955fc182c`  
		Last Modified: Fri, 13 Jun 2025 17:15:26 GMT  
		Size: 148.3 MB (148300790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0719797aa84415caa913dc538c3501e37be1fc6889f6319cb23c4a71ed62cbc`  
		Last Modified: Mon, 23 Jun 2025 17:30:56 GMT  
		Size: 162.2 MB (162154486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5013e13617353602e1e2918d468e9f31c6800171c0ab77d90a5d9244059dea`  
		Last Modified: Mon, 23 Jun 2025 17:31:16 GMT  
		Size: 30.1 MB (30086311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872496dd9b182b98b5ac635334adb4a5ce2bacbbe58f96288d43ea24bcd37f14`  
		Last Modified: Mon, 23 Jun 2025 17:31:16 GMT  
		Size: 9.0 MB (8953407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6028268fdab06230c94b7589068d7afd303c3fcd6f457d611b41a7628d7ac62`  
		Last Modified: Mon, 23 Jun 2025 17:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5825f58755fd7584e9a55ca3210d6fc1dd447e272ee0ca2d8ab8c157efb2c6d6`  
		Last Modified: Mon, 23 Jun 2025 17:31:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:d685994ced53070e283626bf13402d065c627c71d3e3cc4012b6d89f1b6bb63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8b9297eddb8c509e50c2ae2d1824ee28a06000be4991a3cee5c831830985a`

```dockerfile
```

-	Layers:
	-	`sha256:66f68fabd5b1dffaf88dfe95ee678f6b6b2b4992c6033db1b34ce50a166db4f7`  
		Last Modified: Mon, 23 Jun 2025 20:27:48 GMT  
		Size: 6.9 MB (6933771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddac2870dcef6e7989d1e36e8a45f4b2b30c594b0ed8d0eb73730f1f306bb142`  
		Last Modified: Mon, 23 Jun 2025 20:27:49 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:21045ed6a85d97d3fc2ddba9d0ce98c01caa5398de92ba44faeab13c89dd0ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388368312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426b423b208018ba718f601140ebdfd25254631a18b7735ddba24e4550f3af93`
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
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95833b4690cda234aa1b2a80bbda861c36f5508d4740f302edbd0372de994bcb`  
		Last Modified: Fri, 13 Jun 2025 21:50:50 GMT  
		Size: 145.3 MB (145335345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979bbc71eaf621ad266e2c553628e08f439b3c396e8911cdd54c195bc85e2f04`  
		Last Modified: Fri, 13 Jun 2025 23:41:52 GMT  
		Size: 138.1 MB (138110534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6916979d8f4ce171072f1d515642dae0091a69de1dccaea240f0e2bbd88c22d8`  
		Last Modified: Fri, 13 Jun 2025 23:41:50 GMT  
		Size: 31.2 MB (31177250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470703a4ee2d639129f43bde9b4558673edda8ce019f64f0a5f3c737992bd69f`  
		Last Modified: Mon, 23 Jun 2025 17:39:17 GMT  
		Size: 9.0 MB (8953395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd0798e1c59e8c32dab6fd47c16f75f2e42efd83eadfabb9fbd4413a5d106c3`  
		Last Modified: Mon, 23 Jun 2025 17:39:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbf496056508ede0b27915d7bf285e4e6a19fa1206e86298b14ea816aee16ac`  
		Last Modified: Mon, 23 Jun 2025 17:39:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:bf0a9b46e2c9615e11107907e340aa2b7ca36ff849fa8f288c425d2164c81114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93404eea4e848f668b00088126d79395cd8b617c152e72e091a32dad9565dbf`

```dockerfile
```

-	Layers:
	-	`sha256:a9ebc40b546b30a5f4c8d6c0397c6f644ce33464562f61e1e1f1c278dc3eb02a`  
		Last Modified: Mon, 23 Jun 2025 20:27:55 GMT  
		Size: 6.9 MB (6931975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca1280cbfd9e7bb68a7445c853be062748625a9b0bdb227a529428fd26e42ae`  
		Last Modified: Mon, 23 Jun 2025 20:27:56 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json
