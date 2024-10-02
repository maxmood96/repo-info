## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:e85e493a7b639fe9257a4917407dbd9e9dc0a3342bd3008935484481369fb34d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:f7b1ddbc65f1ea1765c872e3b08b5d73cf4e9f2921616649bb170548983e5afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402448709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091bb0be7546e575011f9b86a7b9f3a5866989d91d15a897e55c831a617412e0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.12.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b45a8065fa810969d1a7ad2d02ce0e3de81402ebff98decd2b63731c4947a13`  
		Last Modified: Tue, 24 Sep 2024 01:56:52 GMT  
		Size: 152.2 MB (152247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed9a8049ddb47a4faee553f43981dc6936c9170931bbdeae2fc939b972bd4da`  
		Last Modified: Wed, 02 Oct 2024 03:59:10 GMT  
		Size: 148.3 MB (148282899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561c514c681af4327893eb50569c427307488af0313d96bbb9b1e7568df88cae`  
		Last Modified: Wed, 02 Oct 2024 03:59:07 GMT  
		Size: 30.1 MB (30068316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6cd7c9b2b48c1a327d320a9bd0858bbc3dd53ed0d4ca59acd6092e89c0990`  
		Last Modified: Wed, 02 Oct 2024 03:59:07 GMT  
		Size: 9.2 MB (9170405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d939abe6547ca52fc5e7eb23fd33f188ce3ace83b10a833428a9b21c4836c675`  
		Last Modified: Wed, 02 Oct 2024 03:59:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864a9fcfa7eebc8ef10573521e207f95516db70570bc44aac9bd70d7aa0ab93d`  
		Last Modified: Wed, 02 Oct 2024 03:59:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:24fe3b536c67d2e7b0d893499b0b5d138cc8ed512c25d49870505df1f6440830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6936732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581b65d10a057d91feec7532830b67ce114d9d9134890400a77508657d13ead9`

```dockerfile
```

-	Layers:
	-	`sha256:e23cacf4d7f6e8de846f0f233f4b29fb79603d3f99385466cb9dd9cd9c748b2b`  
		Last Modified: Wed, 02 Oct 2024 03:59:07 GMT  
		Size: 6.9 MB (6917259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49a55c9901fd4bc0127bc232237a376d6ac78b8a37f1e86765ca4bc88d03e55`  
		Last Modified: Wed, 02 Oct 2024 03:59:06 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ce31497b4d81616be9e4357b5c56557c5cfd20b8fd3a991ff1181cc0fc14b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380123331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbec7998810b84fa0e2dad5e6e6e6e799df6cd268a90ab6b37f93381025db7de`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.12.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46effa7b22d687fc510d9b6c929635519e7c4f3d222388e71564cea3659e1e`  
		Last Modified: Tue, 24 Sep 2024 02:36:02 GMT  
		Size: 150.9 MB (150865036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415bcdce6f262265fecac682905f407f8cfd4edb1abe8e127cad0be0d5728fd`  
		Last Modified: Tue, 24 Sep 2024 03:08:53 GMT  
		Size: 124.3 MB (124319418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c8523231366685dafe8d9a8dbb81aa2411f42da3b623ba17c57421ae58a8e`  
		Last Modified: Tue, 24 Sep 2024 03:08:52 GMT  
		Size: 31.2 MB (31180841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebfcddc82bd774ff8e47259d0d7c2678dd7f2fd0d0688d4081a5157e0a027d9`  
		Last Modified: Tue, 24 Sep 2024 03:08:51 GMT  
		Size: 9.2 MB (9170448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbbff0a623bd441963793a7108c0a56b2db3f986953b55981c0bafd637e8436`  
		Last Modified: Tue, 24 Sep 2024 03:08:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216e944b8846a5e404826301eba4e9400e3b07f61f5d7573b139d708948c25d`  
		Last Modified: Tue, 24 Sep 2024 03:08:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:231e2b479f6f868e5457bfdfb4d96cd30a5a1c83d741ffe2aa67e67711b07707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6934942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce99de4c278721593cca5cf8424d70e6011be8afd191f7cbce9c9f70d2b59592`

```dockerfile
```

-	Layers:
	-	`sha256:ee8e963c8a64aa0f9a607bd1af2c30e79ba3390ce9d45cd0d101e3c8ebd539af`  
		Last Modified: Sat, 28 Sep 2024 03:38:13 GMT  
		Size: 6.9 MB (6914702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c68783f1d82f159411321a11eed819cc96834c9ea1bd65a3396878e9ece324`  
		Last Modified: Sat, 28 Sep 2024 03:38:12 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json
