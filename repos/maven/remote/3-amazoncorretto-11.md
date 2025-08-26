## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:a75dfc2882b47547f4b3ab1ee7ae328af502b85d114acf7f54d6186894d65b98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:f032c5ce425cd9d792986b87d6a6e1d83948cbee3b7164e0d71edb6691da4b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.8 MB (416770953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5995617ca4b4424a6b5c567c6e2f3af96d7c5ac3c42d4c83d69e3830d312b9d6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e392f411b02e2eab074a9b83d03cff1a29b558ba7abe1b4b224b81cf9461a623`  
		Last Modified: Mon, 25 Aug 2025 20:55:14 GMT  
		Size: 148.3 MB (148336712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0bbd113dee484ca883e3c349d3e6ef7df557155febb870abfaaf89f1258d8c`  
		Last Modified: Mon, 25 Aug 2025 23:27:51 GMT  
		Size: 166.1 MB (166100523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6d949de053117fe1571e3634342d79bcaac83e5d149703b787fca0c0d4313`  
		Last Modified: Mon, 25 Aug 2025 20:56:28 GMT  
		Size: 30.1 MB (30111966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843d61154aecd2d07649a3f8b83cc27938529b5cfb4d5b4bcfc8b71a159deb0`  
		Last Modified: Mon, 25 Aug 2025 20:56:25 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5584e647003c1fe1a1dc176794f6c38fab335a866582e45c4149681684beff`  
		Last Modified: Mon, 25 Aug 2025 20:56:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea7a5fa1dfcf1875f9db47f57173410590ea2a75274d9e9fc07c68ed91a2ab4`  
		Last Modified: Mon, 25 Aug 2025 20:56:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:3dfc720e66ca0d2a43d2bf1be5a5c3e1c431b65fd6b67a705ab040cfc4c8efd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d8ab07ca9fc6aeb551f3e946d27dc64ce70638abaa41cc0b6f7e79572e19b2`

```dockerfile
```

-	Layers:
	-	`sha256:20aa763da5ce601279ae6bc06b25a1c7863ae780c5e0f282130869685b92584d`  
		Last Modified: Mon, 25 Aug 2025 23:27:27 GMT  
		Size: 6.9 MB (6936332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5271ee718dff618ab06409520bf9534f3c9839fbdc15d7a699c7175de5ebe550`  
		Last Modified: Mon, 25 Aug 2025 23:27:28 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:690acbed26222d7a8efda4bd2281008443ef55f8dfcd728d682bd58b13a31e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.7 MB (392687555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5c970c0e5f77f84290139fc9df102b8c897793450828f84a578fa1688601ee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb7192c32fa4304183daaf2bd2088b988a2ac245d547f64ba6babe344f5546a`  
		Last Modified: Tue, 26 Aug 2025 00:49:07 GMT  
		Size: 145.4 MB (145379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886788ff20b26e2fa861dff93b51a833943b2af6a244973a762695d8fa405024`  
		Last Modified: Mon, 25 Aug 2025 23:35:16 GMT  
		Size: 142.1 MB (142053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bd902b2bec76918b98cfe420cfce895b318b2e1a1fa97b16bb5636d1a11d26`  
		Last Modified: Mon, 25 Aug 2025 23:35:14 GMT  
		Size: 31.2 MB (31209489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca833a614752eeac6f8527c8f774e18939ddd2ff3b654ae702705fb920db1a5`  
		Last Modified: Tue, 26 Aug 2025 00:10:01 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c479f82516473c8675ec734c8c00205ae360446df27bc913d382ab811b0d9f`  
		Last Modified: Tue, 26 Aug 2025 00:09:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73069fdc119c5e5eaf00df515d1c94a7bdfc56e980a21e9def2ae3192958358d`  
		Last Modified: Tue, 26 Aug 2025 00:09:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:d79e9cd74a77bf2868c1ee7fce598cdd1824f02abae87a78712edd8ebbf60d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850bb4cfe863426a1c0cb58da167c14cd613a8b2085664368ea49a724a155da7`

```dockerfile
```

-	Layers:
	-	`sha256:0111d2489056a7d27b0f962a11d6b3356df24c770089345cc5c3b5338e27dcce`  
		Last Modified: Tue, 26 Aug 2025 02:27:32 GMT  
		Size: 6.9 MB (6934536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9298771df59d5c8557ce9cbff02220a8861e3d1091b622f2d5879835efd7c915`  
		Last Modified: Tue, 26 Aug 2025 02:27:33 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json
