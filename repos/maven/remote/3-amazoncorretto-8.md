## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:5ebace9511167270affc19cff58b167003d6a07c57ca0b74e57f75ce3df51f32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:7bfa961005e90f7fb644f27921b4ef29fc995041cbb4b424eb985f2777d835b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330704694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a9d09758ef9aeec7f3ac212be7ce7cce679203e14d60883e22a3b594c17a7f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8fab1cd53a92a9e8bbd717880f65104f330d69b3b7bc74d2439deb4798c25ba6`  
		Last Modified: Wed, 15 Jan 2025 16:59:20 GMT  
		Size: 62.6 MB (62633179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de46610fb4dfb52184f325cba2eede39d300a87ed63b8c5a5ab28906834aab6`  
		Last Modified: Wed, 15 Jan 2025 18:30:45 GMT  
		Size: 75.6 MB (75563604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f2acfd44ccfa87dd61de4ab76f4f79ec7da4316b74761ea0d33eeee39b9f6c`  
		Last Modified: Wed, 15 Jan 2025 19:10:10 GMT  
		Size: 153.3 MB (153281430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe3772c8506a4c455cd30adaa0321e72dcfec10808e86c43c988cd3df6e4f29`  
		Last Modified: Wed, 15 Jan 2025 19:10:09 GMT  
		Size: 30.1 MB (30054996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7dd4e59236eb6ce8af77b4232cb6eb9b906c5e7837b7737ec5c4a6f1998114`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1b1416ee1b30fe38fc496eb866809fb8dc7f8d61f635116f44d76ab8a0ccbe`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f1d4c30488f7e19fa9f011e568a5c0f0e449ca4ec74efb8b96959c0436fd97`  
		Last Modified: Wed, 15 Jan 2025 19:10:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:cb1ae04eb004cd5bfac4c97a8d3722f46b1ce580fa4165dba7f6d59ee6af3016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d1390b60de9aa7587fed1d6329ee29474fed2da47dd96c74461558ec1aaa47`

```dockerfile
```

-	Layers:
	-	`sha256:05421c9505992ce9edf5f4aba1a560adbfecfd7f787f478cea80721c0196b2ba`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 6.7 MB (6749321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d3472423a6da48ebf3b5a7550b26333004eca8dc6ab65a0f0b1fe211a566d9`  
		Last Modified: Wed, 15 Jan 2025 19:10:08 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bbc6603b069dfc29dec4e40d0cd39fd8b835224f2edc60d7ee59bc61be429b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293894233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35dad2ed2a7939436fbe32de6710e083cd91da436c8e2b7697f48e2b7b1aae64`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ee146c9a56ad020ab6e742508a6b4173854c4d74cac5e45ed0ba7c5de719c6`  
		Last Modified: Sat, 11 Jan 2025 02:55:45 GMT  
		Size: 59.7 MB (59669426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee372e4c875b18c7d5c66453bb7e966587bfbd8af9b3894d76692fb72a33570`  
		Last Modified: Sat, 11 Jan 2025 04:00:14 GMT  
		Size: 129.3 MB (129276111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dd9251face3e2fe255b0066803e87a35d1f238ebc837cd1ee6b03af6757a1f`  
		Last Modified: Sat, 11 Jan 2025 04:00:12 GMT  
		Size: 31.2 MB (31186915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b00ac6a85e4f2c456668e2a309a03633887f4a1e4843489c34f55dc4b2a74eb`  
		Last Modified: Sat, 11 Jan 2025 04:00:11 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdf33e044079ad0ace480c9e01cf1971b61549b0a721dd5638c01ac44c50c12`  
		Last Modified: Sat, 11 Jan 2025 04:00:11 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8223a6ef839e60f2e50f3b0c203f3163ecdc2461083111f41d432f76e160af9`  
		Last Modified: Sat, 11 Jan 2025 04:00:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:e26a49df1207d18ad0f5033dea64e99f942e77fa664207069291d468b099162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6744884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d28922662df73f8de37e71e452cadaaac207fb605a83802dc39b48874f16ee`

```dockerfile
```

-	Layers:
	-	`sha256:3c54aad9a098aa1c0a2c56470b18b7f4f06e138cd7ff68564c0300e9c2d124c8`  
		Last Modified: Sat, 11 Jan 2025 04:00:11 GMT  
		Size: 6.7 MB (6726518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c86fb28a16fd94378e295133bc5ddf975488e58e51aeffc78159761d8a01ed7`  
		Last Modified: Sat, 11 Jan 2025 04:00:10 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json
