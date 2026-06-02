## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:5417f4bccfba76ca10870aaf86f750a777b5c74ac4ef23b4633ab352ab5d4883
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:1ef665a51a3ec846da71a414cede46a088eda7b32fde317acb6e804c9657a8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434943443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879f55a0fa4b4183f2289140b0b973c2060b9e531df9d22c0de35b9813ed212b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:34 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:34 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:34 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 02 Jun 2026 10:24:05 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 02 Jun 2026 10:24:13 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:24:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:24:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:24:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:24:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:24:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:24:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:24:13 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:24:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:24:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:24:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a8a7978ba0ff58ed98a62aa94453f0163b3b048a2891c3f00e0f937576d6f6`  
		Last Modified: Sat, 30 May 2026 01:11:54 GMT  
		Size: 152.7 MB (152678214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61c05d3cfffe4cce020c846dab647ddd0b74566134e3ac01338c98b3411973d`  
		Last Modified: Tue, 02 Jun 2026 10:24:42 GMT  
		Size: 179.9 MB (179891680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71b83b7263dd2b0c9ea0da75cbe2c59d94b0bc224e5765d22434cafbb8588c3`  
		Last Modified: Tue, 02 Jun 2026 10:24:38 GMT  
		Size: 30.1 MB (30070634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7214a9e2d42dbda1c2b955b94dd82245d29a9249aefbe4a7437949556625cf`  
		Last Modified: Tue, 02 Jun 2026 10:24:38 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d83b06706afc520f6cf5633364ebbe3167148f85ee74ffce24eb53f0a06ee`  
		Last Modified: Tue, 02 Jun 2026 10:24:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f9642ef02dc5152f6d8757cedeb4c52c8432faa1039e2f7075d61c36056b9e`  
		Last Modified: Tue, 02 Jun 2026 10:24:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:074d18525b1c206dcc66457d99714b4d7e28a27c2b3b47d5ad72e9faec2a0fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567379e49d76726cc653302fca8855e5aafd48194ac0456b19372ac4afeeeec1`

```dockerfile
```

-	Layers:
	-	`sha256:6c33a16e13a21c2dbc8b777de890856b58ed3577ca79c15216204dcf08e667db`  
		Last Modified: Tue, 02 Jun 2026 10:24:37 GMT  
		Size: 6.9 MB (6933165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706e71dc419c6ad3f94c03af4f71777bdc895d95a1ffb1737a8b947032762a60`  
		Last Modified: Tue, 02 Jun 2026 10:24:37 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:abdbfa7e41408019e92e8f258922ee52d5c2c7156010f6c22a2f9b9cce9ec890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.1 MB (412136226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d86e00a1d91a9cb8f037ef828c14ba55cd66901948d5b0ac38c45a742f2aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:36 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:36 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:36 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 02 Jun 2026 10:21:20 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 02 Jun 2026 10:21:27 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:21:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:21:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:21:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:21:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:21:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:21:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:21:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:21:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:21:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:21:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeed7018fa6b115148f6bea5857f5dcf0cebdc10077dc033be3c7b430dc97a5`  
		Last Modified: Sat, 30 May 2026 01:11:57 GMT  
		Size: 151.3 MB (151318832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3783f7d3f48d25c1755fc8b555ce4fa1bb7f566d2f892261578c4ea91e10a12`  
		Last Modified: Tue, 02 Jun 2026 10:21:55 GMT  
		Size: 155.5 MB (155460765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf00644e4a00f005593a990faaf69edcc5ce1acc2cb92cd2edaba3ff26ebfafa`  
		Last Modified: Tue, 02 Jun 2026 10:21:52 GMT  
		Size: 31.2 MB (31204949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e70e2782d58d8998b78349e482e4410ff2305943057a9419bd4bf0673428b7`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 9.4 MB (9359962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09beff0b6242b4f7035873a435f890b79cce15b48652089ef9eaf8af472a`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad806be8739bc1a607ddf4d310b14372427b17aa25ef545b7853dff5c10c14b5`  
		Last Modified: Tue, 02 Jun 2026 10:21:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:0fe0ad3d886bc83c9fbdb56ae5be5c722b1c88e854a0658dd43b2996c29e1977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a01df0338afbefea7d89b64be6c4462f72f499738dcd740a35ee4225c2e786`

```dockerfile
```

-	Layers:
	-	`sha256:a10c4119877b8e510f2b1f91e5a724b359d0d3bb8c80e3b52b95948a170a3f03`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 6.9 MB (6930564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3095e031572e9ac7f5f33e102e6ab7d9d2c7b9bc7ce517f413e4c36468ff1074`  
		Last Modified: Tue, 02 Jun 2026 10:21:50 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
