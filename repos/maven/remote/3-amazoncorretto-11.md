## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:63cc70f3c0ab6860b2498f07cd81541dac3294c3a66488f9b5048d4a38558d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:5db12faea52bfaba77109c88dbb99a8c205bf51312638d9bfdf00ea6eaf060c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408374021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aaf9f081b394138e2104634671999eb0e675c3e2869fde9d07756976c04426`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.27.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe545608f09f13a373878770c982b3170240cf89fec38751899698424970c47`  
		Last Modified: Tue, 15 Apr 2025 23:55:54 GMT  
		Size: 148.3 MB (148289539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f994cf4b969b8cf876003722ef5b37c0f6ce0a13ddb4d45153e0b8c08a1f2d`  
		Last Modified: Wed, 16 Apr 2025 00:08:54 GMT  
		Size: 158.1 MB (158077927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f941c90f4dd5c5b50dfe9b98a3a047cac8f653cd447aac54d982b32044f159d4`  
		Last Modified: Wed, 16 Apr 2025 00:08:51 GMT  
		Size: 30.1 MB (30082180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88001af3bb412f9f9b537c8cc59a76b182b1242e4fb52a5c0fb651d86f8d120`  
		Last Modified: Wed, 16 Apr 2025 00:08:51 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d818a4e31438400e82eda407a4ab10c94d9409b8915a1551109c06674fe5fde8`  
		Last Modified: Wed, 16 Apr 2025 00:08:50 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78f2131aa3d4ddb9d990eeddc8d0c1259e7ef01f137c213f070feb330bfca8f`  
		Last Modified: Wed, 16 Apr 2025 00:08:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:bef2754279ba4c6c7bbc9f00c36ee390c6453c4b15c195a72cff039ba9b30d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f4d45aa35979f77160beaf088652405835cafd177cbd7245aec8548b15e35`

```dockerfile
```

-	Layers:
	-	`sha256:060bd956488f09bd1eebd16345a621339f709e03324bce3f80cf8cc89652482e`  
		Last Modified: Wed, 16 Apr 2025 00:08:51 GMT  
		Size: 6.9 MB (6914508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2316c555d78e252b8d01d0328b48831363976c56766661a1cdfb5486117bf36`  
		Last Modified: Wed, 16 Apr 2025 00:08:50 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c28916b86a5843b6169dc81f2c55d32f89c36fde4cb6fd6bf10a76e79e99d19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384337013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467207a85eed95f14045ebc6d3b7a650bc7be9da27831a1dcf1a6373f12f3771`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.27.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ccb924d5aea1ecd0b7aa6ee9015b77d1eda6fbff9ebbc620dd2766d808ea14`  
		Last Modified: Wed, 16 Apr 2025 00:01:17 GMT  
		Size: 145.3 MB (145326260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8808280545de23a31e828db8c7129c1eebc8b36f5bf2ab52fd07f4be10ce1b`  
		Last Modified: Wed, 16 Apr 2025 00:35:52 GMT  
		Size: 134.1 MB (134087607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5490945093cb6096c1ded7a4ad87513d2bda10114332a1ee2faeec4af165d2d4`  
		Last Modified: Wed, 16 Apr 2025 00:35:49 GMT  
		Size: 31.2 MB (31185847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07aa18d5efcf92809c5e51c58d506a6ff613f3da211e2f8024769630474420d7`  
		Last Modified: Wed, 16 Apr 2025 00:35:49 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636eab6fb35b090c5220d56738dc4cd3a87fd26696e03d5a5e9ef59e7f5ffbac`  
		Last Modified: Wed, 16 Apr 2025 00:35:48 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a381b404b88b0ae6e35df9f3ca68b09ff121e57e49edbcc04c41508f112a50`  
		Last Modified: Wed, 16 Apr 2025 00:35:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:5840594af1c622070524f43e06f672e109fcbf83c98dc1bbd2479b182942e3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6931089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231ff68064fbf8133a29cec4494674604d65404ace28e7ca95cf4ea5bd3de090`

```dockerfile
```

-	Layers:
	-	`sha256:d0ed1a7726b6fa8de23a05527c607c0b0513419952303539d79fb1bd6cbd13bd`  
		Last Modified: Wed, 16 Apr 2025 00:35:49 GMT  
		Size: 6.9 MB (6912712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e526f280402c101aa26cbf0f05237e7f862b689f880b50ce9235d9a9592053`  
		Last Modified: Wed, 16 Apr 2025 00:35:48 GMT  
		Size: 18.4 KB (18377 bytes)  
		MIME: application/vnd.in-toto+json
