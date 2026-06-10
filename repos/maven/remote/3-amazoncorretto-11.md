## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:f7cc715259c848657b3642deb57062a9e8382b1a53f8a39297887b1c5c117b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:5f9eb404e1b11d2285e5de1c710f31fe434278b2cba5791ce8f07cff6c449853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432362033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3613ac20bddd47167cc265d927fe866a9f399420faf4450ce026862cc32fe8a7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:13 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:11:13 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:11:13 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 09 Jun 2026 22:07:58 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:08:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:08:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:08:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:08:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:08:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f788e3e4c9f2421a1dc74f13ea633e946d05b3c439a603b63ec4bcd2d9b5e`  
		Last Modified: Tue, 09 Jun 2026 21:11:32 GMT  
		Size: 148.2 MB (148197713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc1eb9b5f8a356efa4074ecc1212696ba9472a660fe47b206ac97fcfbb83e3c`  
		Last Modified: Tue, 09 Jun 2026 22:08:36 GMT  
		Size: 181.8 MB (181790940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9559e0933baf3220f8031336c2d17aeea588b3933ad14f3cd4d4e55840bca77`  
		Last Modified: Tue, 09 Jun 2026 22:08:38 GMT  
		Size: 30.1 MB (30070451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8575efe6507757b944b7aad0426e60ecac696871e014c3109abc62391c17fa3b`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18edbaf6f873df5d96b87040d9531bb14eda77ea427e70f863c9b76766796f2e`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9786d5d2868e1b2f1259de3f0b6b6c6708710ceac468bbd7c67cf24726cfa5e`  
		Last Modified: Tue, 09 Jun 2026 22:08:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:87a4d87d58dd156f84a1fdde0955c4fae1ae6a07ab7880639ab26a0882bf0ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a39e172236aee9aa8963bf34e764b034d5a1ea83292628c468e480f9ec4feb`

```dockerfile
```

-	Layers:
	-	`sha256:4100fba9cc0ce9d4dca497b88b987d46bbc6b1a2c283229820aeedd015f3fa30`  
		Last Modified: Tue, 09 Jun 2026 22:08:32 GMT  
		Size: 6.9 MB (6939658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79361f6e46b0c971a8bcdf398b20cee3f8cf9f7efb3b9d16a08cb3d946da654b`  
		Last Modified: Tue, 09 Jun 2026 22:08:31 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:330083209226f8339b89044bf9451dab26ea3a55248e10f9f1fa814408415aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.1 MB (408075260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2ffaffa144662d0b35f1c3f8505f40318ea8dc619270dcfda64108d4327ffc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:56 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:10:56 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:56 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 09 Jun 2026 22:09:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:09:23 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:09:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:09:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:09:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:09:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:09:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:09:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:09:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:09:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:09:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:09:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674338f6f96723415ae45000e59058e0a3106bfa1c91f82ecd657ecb6b3bc192`  
		Last Modified: Tue, 09 Jun 2026 21:11:16 GMT  
		Size: 145.4 MB (145374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ec2f31512d172201ea5188134a2d06fd3d690c875491c59013d9f9e2ca7100`  
		Last Modified: Tue, 09 Jun 2026 22:09:52 GMT  
		Size: 157.3 MB (157344509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f481f4d5397b89ff833f2fb38682b7a00aeceb1484de97117add767cbfd53ea`  
		Last Modified: Tue, 09 Jun 2026 22:09:49 GMT  
		Size: 31.2 MB (31204699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f16c14137ac9e012cbe8a2c83f42a9e3f8baac59340415870ae4046663bc718`  
		Last Modified: Tue, 09 Jun 2026 22:09:48 GMT  
		Size: 9.4 MB (9359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e4c751e6179519d3b8fe212d09f99123ef194b94fffc0d3295eb0f1d6ff9d`  
		Last Modified: Tue, 09 Jun 2026 22:09:47 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ecad2f419d54a4605677fb4352f2ecd7974d01cef379776e5807a130190027`  
		Last Modified: Tue, 09 Jun 2026 22:09:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:d5fc1118e1286a1e2449d8bfbd3ecbe4aa3a449e1e5d387469919f4fc257970b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878ff0ba4be21ff649443f455630142046d605c6fca6b0ca505018fb5ff127d7`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2a480cb3ead46eaccdacbff79dc9e3f2d50152f64d73ad239a1597ca4e542`  
		Last Modified: Tue, 09 Jun 2026 22:09:47 GMT  
		Size: 6.9 MB (6937862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0b2fb5b4ef87566b8a5172ee99dd5d32f97abace7ac8ca71817b7a66999124`  
		Last Modified: Tue, 09 Jun 2026 22:09:47 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
