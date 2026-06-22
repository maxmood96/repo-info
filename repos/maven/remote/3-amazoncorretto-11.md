## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:3821d5a6a0b0bf3970dc85238682eb8c0f6aece45669cb0b723aefaadf98251a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:028d3dbd7a262762815378934e0805a6d81932609bd751fd9059323dfbf4d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432371106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000ef0aee52875c5408e03f2e2fa7c9240aebd7555ada507a6098ccaba514a35`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:15 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:15 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:14:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:26:08 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 22 Jun 2026 18:26:15 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 22 Jun 2026 18:26:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:26:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:26:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:26:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:26:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:26:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:26:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:26:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:26:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:26:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:26:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:26:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217234256a41616d365629661b23b2d22888dcf063a0fb9197e01bfa3ff9b293`  
		Last Modified: Mon, 22 Jun 2026 18:14:37 GMT  
		Size: 148.2 MB (148198162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea39e9dd89db839f8d8359603f33e44f4eb805dde861ad78bb0ff47555d4f82`  
		Last Modified: Mon, 22 Jun 2026 18:26:45 GMT  
		Size: 181.8 MB (181799092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12841cceadbe25b695d81d4ff9bc48942736fd6dab3b17f00b1f2c40719c8fdb`  
		Last Modified: Mon, 22 Jun 2026 18:26:42 GMT  
		Size: 30.1 MB (30070847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bb79c7c8d62acc94d2dae02e0b0733b7424915a166a63191f3ccd3a29dc527`  
		Last Modified: Mon, 22 Jun 2026 18:26:41 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df87d31b803d7a827ffd86446961742df594225113df804ef854b1c453ac43dd`  
		Last Modified: Mon, 22 Jun 2026 18:26:40 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcf4377a4900bda5e6c8cc3b63dafda9ae956d09195f12141fe86d4d597ebd3`  
		Last Modified: Mon, 22 Jun 2026 18:26:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:aed416a7a9e9df909948d22aa02a80ec0f297339c3a62f3e2c8f59e32abe46d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ce53dc70572f279fd5ecd9bc675278cc6c8bdfe0aa998740f246cf026efbfa`

```dockerfile
```

-	Layers:
	-	`sha256:696f5e2fd34f32587957774d78a3fec289675256af5ff9d4b5ab71337f588cfa`  
		Last Modified: Mon, 22 Jun 2026 18:26:40 GMT  
		Size: 6.9 MB (6939658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8fccd9c4d303364629d1898bf693ea4a0930c4dcba84862fd62f59c17455c1d`  
		Last Modified: Mon, 22 Jun 2026 18:26:40 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2fe953ace04598287355efd0482e84a0d66d4e733ba888b29d09da5e7d477700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (407991089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2467da0a8e6dda469f3b2e65a89d24a00a01be455512767d135c0a18ac3601`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:13:50 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:13:50 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:13:50 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:13:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:33:46 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 22 Jun 2026 18:33:53 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 22 Jun 2026 18:33:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:33:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:33:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:33:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:33:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:33:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:33:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:33:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:33:53 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:33:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:33:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:33:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ea3272638ab517d8e400aeeefc58e26962b698431ddaf38ca7e3315bf2881`  
		Last Modified: Mon, 22 Jun 2026 18:14:11 GMT  
		Size: 145.3 MB (145323839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41913b6f5e89480f32b09c028b97c4bf5e1263aa3239f40db965e706a10800ed`  
		Last Modified: Mon, 22 Jun 2026 18:34:22 GMT  
		Size: 157.3 MB (157303507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b163b18173ca7a325388b13160db0ee5095bf069b4d1d6b6b314ebf43e8db`  
		Last Modified: Mon, 22 Jun 2026 18:34:19 GMT  
		Size: 31.2 MB (31208026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352dfb4ea9ac67ee31fa6373f7f1f4aa683f4271aba7a904b74aa17aaee406f8`  
		Last Modified: Mon, 22 Jun 2026 18:34:18 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664ef9bcb63338434f936d72e580979f9703ada43841cc09f16b80946aaa8b90`  
		Last Modified: Mon, 22 Jun 2026 18:34:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8916fdb8d55fca28460ba3fab9413c1911baadc73ad3828737e87fc4dfa79d7`  
		Last Modified: Mon, 22 Jun 2026 18:34:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:dbfbd62c2cae52b1f739b1dabecb80562ebd04b3137de9a7702af1e4c237dbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f09d126928362040e0862f35a82778e55f5ce6d6d0ed211afb2c0a249ce5b2`

```dockerfile
```

-	Layers:
	-	`sha256:ee81b8988f65fb35837e60983737dbbe4243fd9c9ecc4e3b927caeefe4cdab18`  
		Last Modified: Mon, 22 Jun 2026 18:34:18 GMT  
		Size: 6.9 MB (6937862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27b69d3d7affc9809a9d6eaac6bdd202696c13b92aee17a6ba95756d7d99a0d`  
		Last Modified: Mon, 22 Jun 2026 18:34:17 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
