## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:8151add1e403d174b9ebc14628f114ea27b96d63df17ef613fcabf633a2db022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:fd260e5d5828d11434774584ed820044a86b584455272f9b7b7ce62083cefb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355310198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ad92151bbf436ed83d7da839770444be46cf904c41572f393d1c8e2aa9b1c7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:10:49 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:10:49 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:10:49 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 04 May 2026 20:45:08 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 04 May 2026 20:45:16 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:45:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:45:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:45:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:45:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:45:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:45:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:45:17 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:45:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:45:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:45:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c02de56533fff71bf18fbfad92f6106e8f409b7dd02965c624405e9ebf1699`  
		Last Modified: Mon, 04 May 2026 20:11:06 GMT  
		Size: 76.1 MB (76071848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3e656e20fbedf11718bc8cc8a498f1bac7e011afe3c0c668437f6aec5417e`  
		Last Modified: Mon, 04 May 2026 20:45:44 GMT  
		Size: 177.0 MB (176981712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cda61b050894d68a05b0fc5dbcb2f893486ea2ddb7b5ada411b7368ca0d85a3`  
		Last Modified: Mon, 04 May 2026 20:45:40 GMT  
		Size: 30.1 MB (30083421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3153566d39c40509b769717b70a39b18d463d4f2caa792c31e80f13bcc3f91`  
		Last Modified: Mon, 04 May 2026 20:45:39 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be470440d3d1285bbf6351c2f5293543aeeb3e2d593f011a83fea7354dad0e82`  
		Last Modified: Mon, 04 May 2026 20:45:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f378c94dc1ce6f021b36029f63a6aae3cefcc263908ff2c7cae313a3a4f34d`  
		Last Modified: Mon, 04 May 2026 20:45:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:01281ebdca27d807d0734ed225081f987d0091dc44a2f1fbb725536d920ba02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43cf5c09120826c4323102a7cc01ce9909bc60a02b3d498e1a429353c551a95`

```dockerfile
```

-	Layers:
	-	`sha256:812a6b4ef200edb008b48360f0145559a2a0185a84896c9b6ae8ae5c46452069`  
		Last Modified: Mon, 04 May 2026 20:45:39 GMT  
		Size: 6.8 MB (6773702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06a70bade129b77085f4209bcf260332f0cc1c04f29184bd5ff6032e426deaa`  
		Last Modified: Mon, 04 May 2026 20:45:38 GMT  
		Size: 16.2 KB (16186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5eac84d554ea4d3e07ad51c8153d90548eac90709f2caf2415faee27b654d63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317755107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b114fe82e0352cb1a61d98ffe24bf1986b62ef544d875cc73dbd85632a1e49`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:10:30 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:10:30 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:10:30 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:10:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 04 May 2026 20:45:26 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 04 May 2026 20:45:34 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:45:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:45:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:45:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:45:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:45:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:45:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:45:34 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:45:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:45:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:45:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da2e05bee31f87c0f97d9a6b58641e0711b23eaad8853fe098cccf3966d6702`  
		Last Modified: Mon, 04 May 2026 20:10:45 GMT  
		Size: 60.0 MB (59950173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3fbd874a6fc71d53556fb5c1b7d3bd4730ea83244c1698d3794c9a997d90fb`  
		Last Modified: Mon, 04 May 2026 20:46:02 GMT  
		Size: 152.5 MB (152508511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5d5320fd8988126db906543d93b8c8f353025d5e420d37bdb6882c7ffa6477`  
		Last Modified: Mon, 04 May 2026 20:45:58 GMT  
		Size: 31.2 MB (31187626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaf210c40978c894bfbd21c3605bd47a3da0afbb670d60ef75fa142d02a4274`  
		Last Modified: Mon, 04 May 2026 20:45:57 GMT  
		Size: 9.3 MB (9312256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27a3b859e38bd62e4977700717ca0cb77fd52a0a841568629329fbd9b91f50`  
		Last Modified: Mon, 04 May 2026 20:45:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cf8e0fd731320b1ad9c8893d1dcc291da2fb7d278c12ac192e67ea8d2fc88f`  
		Last Modified: Mon, 04 May 2026 20:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:ff5056f2b1e59f472469615a2065fa1aa3b96ee52faf3653370733aa57ba8dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a2d30cebfd09f143d287257ca7a1ee42a3d8a970e0439c525cf7345fe328e0`

```dockerfile
```

-	Layers:
	-	`sha256:fc45cb82f6364e6ec1704b13174223048b41022b13cf320700a1921a19397910`  
		Last Modified: Mon, 04 May 2026 20:45:57 GMT  
		Size: 6.8 MB (6750899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41af6d97b0af84bb8e7da6103d364c6fd5e4a4b0a6b5d1fb63d90eb310ff5bc`  
		Last Modified: Mon, 04 May 2026 20:45:56 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
