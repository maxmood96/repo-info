## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:0c416750522299a677ecb72aac7e8fe4f13b34ab41ab13cd775ccf223417d195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:484b9660ae9508d590ba75b0b53e06cf01686b84f432b2cd94635fc6ef7b8546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334787342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a0fd452066e4d23a9c15f5552c418fcb3ab9a92ce30d2100e73a41ed844e1f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e70b802ef91fb15807618fc5b70fda13e347c7002e575a087d2eb45acf6ad`  
		Last Modified: Thu, 13 Mar 2025 22:52:51 GMT  
		Size: 75.6 MB (75645409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cbd5833974a7e18de4c8e5a97d8828a24e19754ac985d788d1e6c64100a194`  
		Last Modified: Thu, 13 Mar 2025 23:09:47 GMT  
		Size: 157.1 MB (157108167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b26cecf3c030d775e1aa812d286b4d40eea2bfdf1e4a3d9e996e940f3909e`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 30.1 MB (30089451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d36c7037d0d489b3a06e51a124e276acf459e98081997539525251747b31e1`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ab4c1660c703358e80209c72912be04ea06df5a045c431765dd0b58b501b6`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9f5138ddef4eac0a260a742e5cd02ea744912b763e85b54aedae614d1804e`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:3c1aab35ea80efcf946a15046d8d979c317e91762a93f52a3a030b6a10c3e487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d77899c1c6dbb85fe835d260a5c1beb4dfb5370319e33c11cdf7db9eb93a7c3`

```dockerfile
```

-	Layers:
	-	`sha256:e6e4af0636a7359d24f8991dd80f377b1d3962107a3d17367252e7b58a7f5208`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 6.7 MB (6749325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b4b3d2bd17121f8e08ad6437d0812d1e8727ee609d79e1d1ac24e4e90230cd`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 18.2 KB (18218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b9b489b493a0b0fd1e68ea43fe40c6350998f8ffc1e1b679dbe0b2693cc65238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296501473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae219fca2bfac95b589002a45397e2dfbf2f8b784f38deda49e9f5773b3a9c32`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385f120b7c583c3e8c6734b7c5715f966f96e99c44472b350d802223c20ea6b`  
		Last Modified: Thu, 27 Feb 2025 21:07:53 GMT  
		Size: 59.6 MB (59610742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02a9be85bc4c8699bfdfc32bc599cd5da8ee47e02ec1faac6edc9fbe93e1242`  
		Last Modified: Thu, 27 Feb 2025 22:43:03 GMT  
		Size: 132.0 MB (132026157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b07575f2ab148fd0a4f72cbf4b4b12af340a9cc9c6f1180bbc376022d5370c`  
		Last Modified: Thu, 27 Feb 2025 22:43:00 GMT  
		Size: 31.2 MB (31171891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02859844890eac2b3cac64083e4c3ff2a4b85aad26e1dc9e3e785aa04938ce77`  
		Last Modified: Thu, 27 Feb 2025 22:43:00 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e39e47860f5eb9fbb766fb2bf5debf4534dd61f0342806ee92913a2467827`  
		Last Modified: Thu, 27 Feb 2025 22:42:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36028cfb35840282391d97ca040d4b3ec4800baaaf1958ce523d880b75c9734f`  
		Last Modified: Thu, 27 Feb 2025 22:43:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:d72541d46729f55b9555782d1e8eb62723986425defb416784558d61ccd55b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6744889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c2f949e0dbe9ba0d581cf48cefe750672a0ea50738bbc5b77c8e80f6f3d45a`

```dockerfile
```

-	Layers:
	-	`sha256:c88184d900b578f8a00c0543fe2b765b6347e97206ba3455795824ffb6723056`  
		Last Modified: Thu, 27 Feb 2025 22:43:00 GMT  
		Size: 6.7 MB (6726522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b455f5e9436baafe83f6606ac73fe7ee4c56b3fb28b56ac767ceb57aa661b3a`  
		Last Modified: Thu, 27 Feb 2025 22:42:59 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json
