## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:3574f00db26af4ae4ddfa9d808ecc2640b9c7b9ac5f0bac37ed10c26b134362a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:180fbf3d376615e35763916e8bb051a5c79f8e6592668e874a0ef70606404194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.8 MB (426848673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f5f894f65f50ddb7da72c93e16ee9961e4ce281baeef0992fa48db6430a193`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:45 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:45 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:13:45 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 07 Apr 2026 05:07:09 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:07:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:07:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:07:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:07:18 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:07:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:07:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:07:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:07:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e65fcc82c0c202279686f9169ea0135db1de90f3eb34bdf3ed744e581732b7`  
		Last Modified: Fri, 03 Apr 2026 22:14:05 GMT  
		Size: 148.1 MB (148126429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057d1215b7431cf8cc28ca546e3a7cf1d94246ac13f6b04464acf2b725f0636`  
		Last Modified: Tue, 07 Apr 2026 05:07:46 GMT  
		Size: 176.4 MB (176371044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad72b29ea784d659cb5ebf0876d01e2161f68a774e60c61b86f377de7cb31789`  
		Last Modified: Tue, 07 Apr 2026 05:07:43 GMT  
		Size: 30.1 MB (30083671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c7ccfd42462721158ff9414cf6f0dce3a9f75fe36299aa08e12bb37f53c8c`  
		Last Modified: Tue, 07 Apr 2026 05:07:42 GMT  
		Size: 9.3 MB (9311189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53084d1a526e9affaede3e8273a9469e532087fd973d2b93c3f019ed7dbd45c6`  
		Last Modified: Tue, 07 Apr 2026 05:07:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaa86aa7b0c7fdb345b79e46d78b896d496003a68f52639b7b712da9bc76947`  
		Last Modified: Tue, 07 Apr 2026 05:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:7a2d627305f190d2afe78ee4b6b1e82fba43e48de62dbd7322af64d0035e8a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344723af5efaac04f3f0752df7e841f32b792efc312822f1f97262a103c4932e`

```dockerfile
```

-	Layers:
	-	`sha256:81e00ab7ad9e18bed677baf6ee0171d33c962e855723d0e841649ad24011e0b7`  
		Last Modified: Tue, 07 Apr 2026 05:07:42 GMT  
		Size: 6.9 MB (6939651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6be30ebb3b76c67b13a29b76d5b5325f22e110ce07d8e035eeded730431a8c`  
		Last Modified: Tue, 07 Apr 2026 05:07:42 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6469b03515390f1aa5eb144ec31a793a9c8d8276b2185475df9e61b729d28717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402433840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167121221b268e752bb99123a9db7520b022131a565e4488a90db331247d528`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:12:35 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:12:35 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:12:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:12:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 07 Apr 2026 05:13:29 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:13:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:13:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:13:37 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:13:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14060804366809adc3232246da5b6f963e9f63b9c98ef312b8a5dbf6b3453bd6`  
		Last Modified: Fri, 03 Apr 2026 22:12:56 GMT  
		Size: 145.2 MB (145212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6213b9e720eda5b83a0808cb877914666d0b7eafc5f2425361e5a0d1d79260f`  
		Last Modified: Tue, 07 Apr 2026 05:14:04 GMT  
		Size: 151.9 MB (151907472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2523ff19ad7b1220e324c8c51578523d83db2e17dcbf4949fcc0ec1abb0e8bbe`  
		Last Modified: Tue, 07 Apr 2026 05:14:01 GMT  
		Size: 31.2 MB (31198711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d3b75bc4b8ff634f24084f678c2177ecca44e32ffb01a2c37223d7e22fafe5`  
		Last Modified: Tue, 07 Apr 2026 05:14:00 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6515fd6737f9cbeb37e318aa6e62bfb21d3c479cff3a24b8b6320454e53471c`  
		Last Modified: Tue, 07 Apr 2026 05:14:00 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a3e167dd136de512ab6b1dd8ac7578339a87da0d9fcca032a76f513ee074a1`  
		Last Modified: Tue, 07 Apr 2026 05:14:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:87bc94f005b624afe385f3767e6416e626617d713406448876403780a9e0e79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6083f8252c114644f5bb52a6994c0fd6190e4fc08ba3e6010eac4435177e3f`

```dockerfile
```

-	Layers:
	-	`sha256:53817d6b8f95d215cc3c6e5307e0aa13cf9c45e47d75f8025ac05b2d4b6a85db`  
		Last Modified: Tue, 07 Apr 2026 05:14:01 GMT  
		Size: 6.9 MB (6937855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42048e1025d2b543a4cf3cea9eb532cad22a86bf918029a27fa53460e4355d63`  
		Last Modified: Tue, 07 Apr 2026 05:14:00 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
