## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:08061dcf57bd3cf0bde3e7405286e9ff05a2d2983c383d50075d5e181abc2c60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:b70aa8d3e14473d3647db6e43dae5620389410bdb718778d977b8f0c83b13849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.4 MB (430356122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ddad2e6364d73a828938ef40047bc614f8903da3ae3a374cf3a3b1f9e39164`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:50 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:12:50 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:12:50 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 09 Mar 2026 19:13:51 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 09 Mar 2026 19:13:59 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:13:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:00 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89257e0640a148754b27ea19438c565af935054d2354ace1f7ecc2c7e2d9b538`  
		Last Modified: Mon, 02 Mar 2026 23:13:08 GMT  
		Size: 152.5 MB (152455379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04388d5342b7560669df3eb10c30ea208218b631f33b21f2f52b38a6f7c429b6`  
		Last Modified: Mon, 09 Mar 2026 19:14:28 GMT  
		Size: 175.2 MB (175159613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074cfc6756feb33148d1f4da1316035462784f8f860a814025cf3addd090f8e6`  
		Last Modified: Mon, 09 Mar 2026 19:14:25 GMT  
		Size: 30.1 MB (30082337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be9ee63f7274aa6973f558f7d40c99e4fca2e9acc527903b4b33e58f80a83d`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 9.7 MB (9697522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d58a8a7850b099619a32fe11f8ace120b1258cab57fda0b82520e0c92c3b4`  
		Last Modified: Mon, 09 Mar 2026 19:14:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431a6782254319612af2914a6b62c890b810c9f73d4565574284e6445000bf3`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:ffbd944d42d616befd5f85728c4c9179bca06f5aaaa39ce58f1644ee4af871c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfb836fe33058712127a61781da7076883044b3fd6a483580531cddf049c153`

```dockerfile
```

-	Layers:
	-	`sha256:bddabb5dd9d0dd6a0180c2bbf52aa8d44c017a197ee91ff3215c1e5d1a17e38f`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 6.9 MB (6938738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722e3ac562b18dc5d8579bdb7120eda348e0433741a567d4aac854fdd008e99f`  
		Last Modified: Mon, 09 Mar 2026 19:14:23 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:97bb781563f314a18db8297c07e27176515d9ea32b34a153730e6e29afc1f3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407488269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d39cd4aa2d01063d6a42fa2e9111684db488845351fa46af72ccd40f7a0f6cd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:46 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:46 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:46 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 09 Mar 2026 19:13:33 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:13:41 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:13:41 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:13:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:13:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a6f64c6c904e9ef9b020d55ef2c8e5977ab0ae43c95f0454e34c21342702b`  
		Last Modified: Mon, 02 Mar 2026 23:15:09 GMT  
		Size: 151.0 MB (150975227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ba83952e4393be9e829441860e0e6efeed8e8c91dec975b2c99a7f2578df8c`  
		Last Modified: Mon, 09 Mar 2026 19:14:08 GMT  
		Size: 150.8 MB (150784728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03534c2f3b569f31f87b7b9cdb7b7810e04a0464c7656fcdf2ee38cf3fa6e4de`  
		Last Modified: Mon, 09 Mar 2026 19:14:05 GMT  
		Size: 31.2 MB (31218309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81fe5e9b45e38d8bf8ec32531ab0ff33117d1fafe0c7df7b2b0d1680723635`  
		Last Modified: Mon, 09 Mar 2026 19:14:05 GMT  
		Size: 9.7 MB (9697556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737d80053891d2f75e48236dc6a30f112f727f72748d3c05a4e5c0c4c08ed8c`  
		Last Modified: Mon, 09 Mar 2026 19:14:04 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59a8bf693109dbb5664704c9c2e2b6cb68009ba065161fa1d3679d638038674`  
		Last Modified: Mon, 09 Mar 2026 19:14:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:ab2d3ce57a8bd75de263b2674f8c9bd25716ac07b44a4d83c04bc7f01265bdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925199ba2e592bbe87adcd76d9de4b2973ec4e65063629f738f63257e53af93b`

```dockerfile
```

-	Layers:
	-	`sha256:ef1eb0d7bcdadb9bf0a5621ef172e95c2b737fcab30241623d2156d977fc7106`  
		Last Modified: Mon, 09 Mar 2026 19:14:05 GMT  
		Size: 6.9 MB (6936137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12050a4d370645908960fb99a53c89d614066539f8813182c4fbba9812bd87ef`  
		Last Modified: Mon, 09 Mar 2026 19:14:04 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
