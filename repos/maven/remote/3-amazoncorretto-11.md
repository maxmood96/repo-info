## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:96c5b7d14b2af6aaca7957d5b94d7ffa669e5b9627c8e6991f806e96d4069ba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:50a731715f62472985f5c9f3d68b29fdf51c939a66c9cc093d10df86b8a17bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.4 MB (421369480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759c7e5d7f29328eb0371a29db5a107b2b3ccc9b096eaa4ae41305c31f9dfac0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:16 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:16 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:16 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Oct 2025 01:14:29 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:37 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:37 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23136089a8ce8680867f05d0f4b446ef52c9f6f07586a59e6e50d65f3210aa7`  
		Last Modified: Fri, 31 Oct 2025 01:12:57 GMT  
		Size: 148.0 MB (148044792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9edb64ca90e6e593d8cc4541be260d227838a51ad413630019ee4953cac42a4`  
		Last Modified: Fri, 31 Oct 2025 02:48:11 GMT  
		Size: 171.1 MB (171076331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecf197f1387f04be29b7d1af93c6d4cddab6553ca83fd0a30493a396b475b73`  
		Last Modified: Fri, 31 Oct 2025 01:15:25 GMT  
		Size: 30.1 MB (30070659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c277f37a1ac9516b71344692cb2bf5a0cc8e5f2c00be1fe09f1df92d26b30a4`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1d095ea2e7b07b5e4635d1c182cd6db6de8d8b5da562b24f0fa9407e6f3f9`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746605057bf564d72224b687ce54557d9f52cffc7fc68e7931d664ff633168f`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:d8822996c92b041aadc9b02838746200855c54a710a6ba13e3ccc601cc52ad90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19851d1153c161387cd263a5a9dadba5e502dce2f0d1f0822cf363d0007f443`

```dockerfile
```

-	Layers:
	-	`sha256:c0cf109a30aeaa7f21add52cae12883ec699c22e7abf527f151bfc8c805e359e`  
		Last Modified: Fri, 31 Oct 2025 02:27:31 GMT  
		Size: 6.9 MB (6939559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e6254e680a0ad41f7b4817a6c3cb5dc1c99bc7eca32d1703c835635cc206ae`  
		Last Modified: Fri, 31 Oct 2025 02:27:32 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:63afbe76f0ecd35f9e763d0fdf499a8d0e11a5109cc23076379cf03fb47f76c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397387036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2e409b7c92f407b0b530c89870a8bc0fef5c4ee36b53d70d362385d2fcea4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:52 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:52 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:52 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Oct 2025 01:14:42 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6cd481af92c0fe698995cb064ba61c7ee112ac206d4ce6c373a6f2da02b89`  
		Last Modified: Fri, 31 Oct 2025 01:11:02 GMT  
		Size: 145.1 MB (145144721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad2129f079bcc2a1f7f69218ea1d5df639502afce03ac7e97689c1c271ec3fa`  
		Last Modified: Fri, 31 Oct 2025 04:04:35 GMT  
		Size: 147.0 MB (147013146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc9c0e616a9c37b9882492607919d312d163744f5cf3657e6a1892735f28af1`  
		Last Modified: Fri, 31 Oct 2025 01:15:23 GMT  
		Size: 31.2 MB (31192081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66de96e2572872cb58de4fc4aa84b9d82a333c9113d1659fe16bde2be7a1bca6`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f665d869e0b159767c6ce21a32bbf9bfe4f3a34b88fcdedfbfa02116b1fde`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53ab182e4f8d7b3f5e548568fa02da03c3574badf427a40155399944c4fe9cc`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:1264c0b75d0bc9956c9ed026dfc471b2cfdf61efbf13bf8acc1c7be8fd11794f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5edd0170187d3e8deb7e131ddbe9b70babc095c37f3e20277ad79dbc819bc6`

```dockerfile
```

-	Layers:
	-	`sha256:fd441efc9abe1a1908005ffbed6da91d2cc0f51864afe8d9326f5e82876d5c07`  
		Last Modified: Fri, 31 Oct 2025 02:27:39 GMT  
		Size: 6.9 MB (6937763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be8ccefc89b116e42a772530158702875d803956c7debb9538d5a34200801ce`  
		Last Modified: Fri, 31 Oct 2025 02:27:40 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
