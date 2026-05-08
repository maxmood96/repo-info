## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:8ae7dd9a33a04fdf1f6cac3f05a160a4e0fc22658a3c8c887b56a923084e3120
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:e859bcc3ab2cc4bc418468b869723d96e775af85219cd936c906a78c0d3df90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255972516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99118a42ebfa2f59f7722b7b22026532dce4bac9578a3c36b26653936dab8e2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:33 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:21:33 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:21:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 08 May 2026 20:21:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:21:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:21:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:21:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:21:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:21:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:21:33 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:21:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:21:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:21:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73a8fd1b5bf65fd7d8640f68656e45545fe5eecad8bf65314930b4024f2f793`  
		Last Modified: Fri, 08 May 2026 20:21:57 GMT  
		Size: 216.9 MB (216879042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d36066b17b2f31316af085457e3dc5e776d575e814dda4fc6da3e7aa76ada`  
		Last Modified: Fri, 08 May 2026 20:21:53 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bebdbd593c89d4c39fd6adaaabeefa6f7faa809f9adf57f5b0a1f3d4c1bc638`  
		Last Modified: Fri, 08 May 2026 20:21:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa6b1a86bc8ef016a31d6b1d5ee471299fa3cc57ff6de12cf0491cd04d1beb8`  
		Last Modified: Fri, 08 May 2026 20:21:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:640691a5e120f110ebfc16b774c63eaf17a94410928cf563f3608e78de572bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7c8177e3fde58e09b20c84013d7199c806d01b79ca641b5224018fd4c6bb55`

```dockerfile
```

-	Layers:
	-	`sha256:c4ddcdf18f58ff930d9cf258eb223eca2358a66993dcb13a0d0738e74dcb87ca`  
		Last Modified: Fri, 08 May 2026 20:21:53 GMT  
		Size: 3.1 MB (3104636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01eb8d1f12b86aa9c0abd89cfcbdb99b269ecae722df1ab0dea790e81929431`  
		Last Modified: Fri, 08 May 2026 20:21:53 GMT  
		Size: 17.7 KB (17679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c16abf4d93d8ccadd3e4bd1d02c78034abc6eab421f7dfbec578d5dd96c48626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254383571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfdadc51b21f5c60e94f08214f7cdfbf813f005c161a88fa7827ac1e8c519f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:26:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:07 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:26:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 08 May 2026 20:26:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:26:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:26:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:26:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:26:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:26:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:26:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:26:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:26:07 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:26:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:26:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:26:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9391c3d6a71c88035c04e22ce225df72dfae58db4c9efa0d8b5bf198c30a2ad`  
		Last Modified: Fri, 08 May 2026 20:26:33 GMT  
		Size: 214.9 MB (214926674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b5925dc62c4249b25841012b69526ef08b811fe9e774171d89f1d703de9876`  
		Last Modified: Fri, 08 May 2026 20:26:28 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa260fe991a15999b4c128f1985b1877543ded5f185ca8bbfb49687d84e733c`  
		Last Modified: Fri, 08 May 2026 20:26:28 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7166588b862d395fdf6080ca1a54d795f5af84bc64a106fb58feb96aab201ceb`  
		Last Modified: Fri, 08 May 2026 20:26:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:90d070cb0ec3f7f749881099b600144997419c99ef37c86cb53ada88a9cb03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8961aba16df5f7c5fdd36ec27addafabe17e191a6bb516304788a97336a231`

```dockerfile
```

-	Layers:
	-	`sha256:59708fd4ec2d9b989949625adce49a04c50ae7557c5abaff94d79646ab5c801e`  
		Last Modified: Fri, 08 May 2026 20:26:28 GMT  
		Size: 3.1 MB (3104299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2516f7f5734f89531404ffb9932a13882eaf2ca21c22d915adf3cc47b0a7a3fa`  
		Last Modified: Fri, 08 May 2026 20:26:28 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json
