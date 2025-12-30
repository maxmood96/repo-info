## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:2ec8e4eefdf74df220d41fd56fb4b7d865337bf41db444d9d6c2ed4888ade762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:944cdd5cfbb5ec29a64577174dcee4ab775f06dd21bffb3d7402455a374433e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274321326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45961aa8b32fa04aaef28487dd03d91a2f116aee8c6b139c6f3faa28b7a48390`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:11:33 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:11:33 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Dec 2025 01:11:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:11:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:11:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:11:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:11:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:11:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:11:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:11:33 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:11:33 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:11:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:11:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:11:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25281ed1753afa5f9da1a5fb1b27001f105ca8bf6615b28b5dea2e07dcf2dbd4`  
		Last Modified: Tue, 30 Dec 2025 01:13:48 GMT  
		Size: 235.2 MB (235231514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0a780575e274b9de59ef060f08e82c1d4b958baa47833a4ae8a2ed91da9e`  
		Last Modified: Tue, 30 Dec 2025 01:12:07 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0013e6d374d53406a0ac7405482ae27e309fa625492a926abc6845daf2f85`  
		Last Modified: Tue, 30 Dec 2025 01:12:07 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ee03158fd587c87627a5770823ba9775dd30489fb170d14c6a5318763a361`  
		Last Modified: Tue, 30 Dec 2025 01:12:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:4fc3423cc506357d6f720d8516d248992cb92482e3768315d4dedcee692a1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f59b5de557c0fd98832b491d7fb2c20d885931b55ee4b519b44e6187fc2be5`

```dockerfile
```

-	Layers:
	-	`sha256:83225a6eaee6733195fad3a486e7051e7eb7bf311968665ad424e34da163c802`  
		Last Modified: Tue, 30 Dec 2025 03:29:06 GMT  
		Size: 3.1 MB (3112964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8067c50f8f6521f58f005f73daf98375c619f841186b6e43c4f584f8c6b57d`  
		Last Modified: Tue, 30 Dec 2025 03:29:06 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:32b00701de3a2e8d5ec5ab3fb8a55c15a3d41ba1f6e344d77c8551ce306c4f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272418527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca9f5b9adbde25fe72b91793fd95658844c5b93aeb0c084fcbe62224d7ed93f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:12:47 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:12:47 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:12:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Dec 2025 01:12:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:12:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:12:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:12:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:12:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:12:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:12:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:12:48 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:12:48 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:12:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:12:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:12:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aea08c01842ce159118e27dac225e2c9cbc8db7fa02c76ea36b67e9294bbbef`  
		Last Modified: Tue, 30 Dec 2025 01:14:41 GMT  
		Size: 233.0 MB (232966609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dbe5c8b59dfdc6094a5e2add9db88eee870cf024a283bdeb255dedb5a79a3f`  
		Last Modified: Tue, 30 Dec 2025 01:13:21 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0487481324c2234fc0a053132cb09b3f199c2dde97937dbe9eebf8b8534420`  
		Last Modified: Tue, 30 Dec 2025 01:13:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa67cec915c6ef60d9aa57a19651967ace90031f8da95f398616ece456a3ae`  
		Last Modified: Tue, 30 Dec 2025 01:13:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:e88f4627e51d6e9958b5d321aa3ba3ad9c1312b485d8de1898b7ca3208330f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4a65acdf011d7c57651c142f415bcb98c5b8a61ce2e235dfae83d4387d2170`

```dockerfile
```

-	Layers:
	-	`sha256:05f02c18ba54cca0c18359f68234fa1b54683b9609542ccd639f947901568a63`  
		Last Modified: Tue, 30 Dec 2025 03:29:10 GMT  
		Size: 3.1 MB (3112624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4850760cde0ae18ccb41a5b0e66af07fbc3f4c37e3fa844ce4ae997d0917d2d4`  
		Last Modified: Tue, 30 Dec 2025 03:29:11 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
