## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:09e85c48daef769f40303b123f713829b65ce5473f838b2c1254cbb143eef151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:1230cdb7f077cc4370b0717a3d0705ba141394ccfad742725d8bf326552601bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381587810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df1f27ce2d00cf73b1a06455e4decf5944a357b72e8bc234db547e694b5258e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=21.0.3.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6587bf502e0fddfa3d71e42fc5be22a5dada226ab4e30f31f4c34ed43581b965`  
		Last Modified: Thu, 20 Jun 2024 18:23:58 GMT  
		Size: 165.7 MB (165682272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d3ed75213bab1fc0c2c0e6d58165ca67a82471d87322c499ae3af11e38f4fd`  
		Last Modified: Fri, 21 Jun 2024 02:01:53 GMT  
		Size: 143.6 MB (143610460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8ea93bd134c0462a8e81c8e2951c0b4ce82831cfc0a6afa9749ac70805f387`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 9.6 MB (9647582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa0c27804aa80de79c5aeef8177026810971d0a0bd6249ec59b77999bf6730c`  
		Last Modified: Fri, 21 Jun 2024 02:01:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328bbd393b88407eec5ada1fb386550dc701897180e5b90a0f0bfaaeb42f29ad`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:923446ea1d8d5ba934459d81b12a7b5aaef7dc4fdb3da9ded28581e4e2d07b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b2f3d78fc56957cdfe7215bd68a5119eda2f5b7091a16d93cb40e5be7bb46f`

```dockerfile
```

-	Layers:
	-	`sha256:2d15282170510f71bccff270bcac445776211d8008b823ee01e128a9fbb266d5`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 5.6 MB (5613336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb00b570ab2221f9770d8ea7206cb05bf56e85559d9402cc4d334c7100ec8464`  
		Last Modified: Fri, 21 Jun 2024 02:01:49 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3283cea540966919942b93b53a9a04219f66ec0bed4203272d35f14a741fcf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357584131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eafdd966d4915ae5bb40096d66ef0cc4f04e7a5899235121a05eb8a363be5d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=21.0.3.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eb46e585a9749ebf27644a669f43b430553a5e83c39e1f6219d51b8a62684a`  
		Last Modified: Wed, 05 Jun 2024 02:45:58 GMT  
		Size: 163.7 MB (163748486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079f3c6d99e5f4ce0ca4f33552ccd14516bf378fdf54633bd05b865f0d1ed72b`  
		Last Modified: Fri, 21 Jun 2024 16:58:07 GMT  
		Size: 119.6 MB (119611525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb8b2ecac71d0b15ec19fc8a2a293c3704ed03fa112c0bf9be36ce6a2b4cd7b`  
		Last Modified: Fri, 21 Jun 2024 16:58:04 GMT  
		Size: 9.6 MB (9647629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b0bc1a495a62430a29c9e4fd2034b185b240285709bb8acb123a00777c5da`  
		Last Modified: Fri, 21 Jun 2024 16:58:04 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834253e75fbd7ff0dcd4c4f19080cdb8410066596a6f0cddd9daefc8816620b`  
		Last Modified: Fri, 21 Jun 2024 16:58:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:49ad5a36785c0a2ec3a1416ddcb37e0451fb02227331836d007322acf73d93fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99605ee96d41443cd555fd365cf75815ce8f09a552e49828321cace055630fdb`

```dockerfile
```

-	Layers:
	-	`sha256:fae63251d74e827097d9b9458c39b30ca8ee122c420e852b3d0545944ad37181`  
		Last Modified: Fri, 21 Jun 2024 16:58:04 GMT  
		Size: 5.6 MB (5611963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a9a41e9b888c5dfe397bacd4d40ba300856e1df81e015c3f8744642e2ca811`  
		Last Modified: Fri, 21 Jun 2024 16:58:04 GMT  
		Size: 16.8 KB (16796 bytes)  
		MIME: application/vnd.in-toto+json
