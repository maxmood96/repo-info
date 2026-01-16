## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:1b66508dbcca4227ba4ba4a7de35af300b236b673f9c1afb55b2bb9798203a6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:f13d080f4926e6ec0160199a374c86d3f45cc804476e376105ef33f35cdeec80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241675990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d7bb33b597cd1dedc991820f9593de82eb6779d0eb8692504235ec0da5f17b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:41:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:41:38 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:41:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 13 Jan 2026 03:41:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 13 Jan 2026 03:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:41:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:41:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 13 Jan 2026 03:41:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Jan 2026 03:41:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 13 Jan 2026 03:41:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:41:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 13 Jan 2026 03:41:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 13 Jan 2026 03:41:38 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 13 Jan 2026 03:41:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Jan 2026 03:41:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Jan 2026 03:41:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Jan 2026 03:41:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30e4752c291530ddc3fb394953cdce345286b5793e79e21138f1c6715e6586d`  
		Last Modified: Tue, 13 Jan 2026 07:20:39 GMT  
		Size: 202.6 MB (202589023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce69e559c18646cb92175205e61d30efa7e5f6934475fec38cb7d9ca7d0906bd`  
		Last Modified: Tue, 13 Jan 2026 03:42:07 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45d2eeb458607a7a5a666625847c08fff191159a927ea42af13a4fdb93036c9`  
		Last Modified: Tue, 13 Jan 2026 03:41:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581aaf0c3517eb03387e3c739be9fe6f4397c402a855cea6992569f41377b61`  
		Last Modified: Tue, 13 Jan 2026 03:42:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:bfb7e915177e72d2422075a91cf07992100682b78e03b6368fe49e27ef09fe8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856f7d31f4d73aabd6a89890a3f8585eb70e3d33d32e2edfe8055ce37faf0b81`

```dockerfile
```

-	Layers:
	-	`sha256:198f9ea1e8e480450ab762cf7ecfd56b9d9b2be8a7591a05037338c615144ce2`  
		Last Modified: Tue, 13 Jan 2026 06:29:30 GMT  
		Size: 3.1 MB (3109818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8636535b46e17688e333862df78c854ef8e9bc0e9a3dea905b62e77b0c8834c4`  
		Last Modified: Tue, 13 Jan 2026 06:29:31 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f7062205470cbc4ec81020621027c990f9031d19bf25dcc5dbeadd0c41c2a1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239013333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6311a9f3aab91d4abbbf472d9b60d8fd028c3c7d18124cb23ecd1d87626d0d3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:44:53 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:44:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:44:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 13 Jan 2026 03:44:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 13 Jan 2026 03:44:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:44:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:44:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 13 Jan 2026 03:44:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Jan 2026 03:44:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 13 Jan 2026 03:44:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:44:53 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 13 Jan 2026 03:44:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 13 Jan 2026 03:44:53 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 13 Jan 2026 03:44:53 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Jan 2026 03:44:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Jan 2026 03:44:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Jan 2026 03:44:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93daddb103373381e05962d99a1137317b909f54953fca76e83f1301e7fc9a13`  
		Last Modified: Tue, 13 Jan 2026 11:27:25 GMT  
		Size: 199.6 MB (199566008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7a549a679da20b6430838599bcaf7d8131dcc1d1e5203107c27db98be24695`  
		Last Modified: Tue, 13 Jan 2026 03:45:29 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab73800af4fe47272325b113a40a8668f267a67758dd284c8e0e49fb22dc1e1`  
		Last Modified: Tue, 13 Jan 2026 03:45:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b004110072e6bcc121d8c0a7c75f7ebac68e59d8d27203641f312fc2589ce726`  
		Last Modified: Tue, 13 Jan 2026 03:45:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:9d8d05e54c5201b07d431e5b52a7e19ab3c024b3b4a592c2e0068ade824acb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3492f1d0cebf8426920ea6445c21c9552ffea256a9b1cdd6f4d7f9e77f870d`

```dockerfile
```

-	Layers:
	-	`sha256:fd15e15ef07e4952b021df639d5b8a7092c77c8f6a531f2b140b5edceb7bf7a6`  
		Last Modified: Tue, 13 Jan 2026 06:29:35 GMT  
		Size: 3.1 MB (3110118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ebf2be04b12906836a715c05598102bd6f8e6c9b6086a193ee4857ab9629a5`  
		Last Modified: Tue, 13 Jan 2026 06:29:36 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
