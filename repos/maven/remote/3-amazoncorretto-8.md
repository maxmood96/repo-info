## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:2955e231f79677c238ff802123da87362e328b0030688dd67879ff8cf32b7f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:f3338431ca62c77bcb75773e77b88aa5ceae81efabb2ad098090452c888278c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353255782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48457dca9c85701c02a2aca6fa84253e324855262791209834f75202f926472`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:34 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:30:34 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 17 Feb 2026 22:30:18 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:30:27 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:30:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:30:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:30:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:30:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:30:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:30:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:30:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:30:28 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:30:28 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:30:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:30:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:30:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7faf293aa85d1b8fb9da66170ba497f59fe1f7baa68fa40f05f4030be8e3c1`  
		Last Modified: Tue, 10 Feb 2026 18:30:50 GMT  
		Size: 76.1 MB (76138902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f150408cf12712c055064d9cfa94b2405b80694de2b845f07c19b5762945b185`  
		Last Modified: Tue, 17 Feb 2026 22:30:56 GMT  
		Size: 174.8 MB (174769133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af65856cd5f215af234a55664968f2770859fa929f2dc44eb08861a539353353`  
		Last Modified: Tue, 17 Feb 2026 22:30:53 GMT  
		Size: 30.1 MB (30075513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ab8431af70a4e34fbd4894e9a1616d4ac5ea1900d61d7c8fabcf365c1b752`  
		Last Modified: Tue, 17 Feb 2026 22:30:52 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662a31de39503d2ef6ed742f197f8b8aec0d4bbf7a62557ae880c0550247963`  
		Last Modified: Tue, 17 Feb 2026 22:30:52 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2237bbbef6bf8337fdc13c79cf4ec01c4c12e2209b7384b3f0ec67dd5ec57f59`  
		Last Modified: Tue, 17 Feb 2026 22:30:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:1dad771b902e7c5b28704e61114a2a5b0e540b1f019db88e3f85b33ac4fab9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0525745fc63f4939a3b4ee1ea8943f6f4e0019f1a720d1bdd3cef29fd6f04411`

```dockerfile
```

-	Layers:
	-	`sha256:c09156d063d44c377a95f1c022e2be561d60c8a672342d04c526f25062ca7b34`  
		Last Modified: Tue, 17 Feb 2026 22:30:52 GMT  
		Size: 6.8 MB (6773617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072da69d75994fb9ba708277d55bc386c6f1dade30229f6d577abd0481a2e8c9`  
		Last Modified: Tue, 17 Feb 2026 22:30:52 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0b547905e1a8d641022a67374c0cd368cc0875d51880ab2221eeded91b78e945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315644515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c53e81afbb565d114aefca67761603cb53fe4ec850e799469aff0eb9790a67`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:28 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:28 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:30:28 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 17 Feb 2026 22:18:41 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:49 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:49 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134f14ee5011f8c88f8601f9827bdb627310b071f5f0a3b5869d4a2f4e9df5c2`  
		Last Modified: Tue, 10 Feb 2026 18:30:45 GMT  
		Size: 59.9 MB (59920333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b286bde0bd438f9a2b919d698396a9dcc48c15046e70d6460e08a94a6e6c4d5`  
		Last Modified: Tue, 17 Feb 2026 22:19:15 GMT  
		Size: 150.4 MB (150412712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760b0472d79d4b1c26a91d10af21b926994f6acaf6240017e97bd5aef1467fdb`  
		Last Modified: Tue, 17 Feb 2026 22:19:13 GMT  
		Size: 31.2 MB (31198712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b2a66161ec482a98602d45b78dbff898f1a1ce8c9ca2e399dc9252ea5a59cb`  
		Last Modified: Tue, 17 Feb 2026 22:19:12 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bed5016deb5170fde227049b7d53a3d7f880dd5187e188e900853139347db35`  
		Last Modified: Tue, 17 Feb 2026 22:19:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36345d1fd7ce381e58fcec77ac0b330c08443e694b12828bea3d0d9106a508d1`  
		Last Modified: Tue, 17 Feb 2026 22:19:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:13aa8c47d4fdf346adb84777b7b173e823cc231d84e3cc2e9c6ce6bccb6b724d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbebac268662f0ea8f9eecc622e0bad2239b7cbc60c423ca0a5c011f82bb315`

```dockerfile
```

-	Layers:
	-	`sha256:ff1f49f7c6d65cc8b8b217cef7e3676a94310773da37d7008f9f6ce471a67c6f`  
		Last Modified: Tue, 17 Feb 2026 22:19:12 GMT  
		Size: 6.8 MB (6750814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723e66d692f5ba3d2cc4a83896b3566d2390a098f4bfc2488b3f406ce4bdc113`  
		Last Modified: Tue, 17 Feb 2026 22:19:11 GMT  
		Size: 18.3 KB (18333 bytes)  
		MIME: application/vnd.in-toto+json
