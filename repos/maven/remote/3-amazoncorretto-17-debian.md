## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:bad2731affce3771b7c891f7b3455ee4960c385406b2a20ec8aa64d96c8328c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:6eb4b3060398cbc4e5e36456a48954f622b166c62c28410aa26881af03b93602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243874404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65a5a16e635f5a1ff336e40faf52b0b02d44e71dd9beb1afd37063057c2af09`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Mon, 18 May 2026 22:41:18 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:41:18 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 18 May 2026 22:41:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:41:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:41:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:41:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:41:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:41:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:41:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:41:18 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:41:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:41:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:41:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f76b7ad0f93d5a25cc8e542bb2b70a967bdfec67fd963cfbb35b4b11150a0`  
		Last Modified: Mon, 18 May 2026 22:41:41 GMT  
		Size: 204.7 MB (204733192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143946feaba4e30643ff92f8ab1541c602a80efd46df185cbbaab2b7c17cca31`  
		Last Modified: Mon, 18 May 2026 22:41:37 GMT  
		Size: 9.4 MB (9359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02a0aa7b8b076da86b32caf21de7d589cc5ac25448e44d1e04387ef9c68bd34`  
		Last Modified: Mon, 18 May 2026 22:41:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7870af7f0a9e0a5bafd26c5e74c52371778877d31b4653ef1809ca95c3851d`  
		Last Modified: Mon, 18 May 2026 22:41:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d2e600e3063166fc2a161ec191eddf1698556033e66285d54059a429d8c15c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38306c8f1f2e224621937645d3cd2a7060d299d2f9c9e263d764cd99d690626`

```dockerfile
```

-	Layers:
	-	`sha256:7f898aad20bbc6e78186208817e00b06cf303f62be8e648acc4202ea16985490`  
		Last Modified: Mon, 18 May 2026 22:41:37 GMT  
		Size: 3.1 MB (3104736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893e19ee907f232f9af0ca81125b5309f6fc24438edc2259009306bf6ebbf4a3`  
		Last Modified: Mon, 18 May 2026 22:41:36 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d44a9c11613f1c3c28e426b8adf5d901971efc7eccc8e52eab2c1175fd2c2020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243148203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa3e206add8f0207b99a250336b8e3da1624fa221f01abd342c2b625820f92f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Mon, 18 May 2026 22:41:35 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:41:35 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 22:41:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 18 May 2026 22:41:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:41:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:41:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:41:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:41:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:41:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:41:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:41:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:41:35 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:41:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:41:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:41:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbe745f55ac9d911ac9b51e8bfea1ae1f7274db7511a0586b3d4189a6b199d5`  
		Last Modified: Mon, 18 May 2026 22:41:58 GMT  
		Size: 203.6 MB (203643580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e993c53f039b23ddaf4b1ea63058796f28cbe119afcdd5c7f2d452c6f9a4dd65`  
		Last Modified: Mon, 18 May 2026 22:41:54 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb653264dc50b2d7c9e3e4de16be82b9e5fad4411d681e02589a77df33dc576`  
		Last Modified: Mon, 18 May 2026 22:41:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f91f639fff80487b4e32f946a10abb69eb16cb9bf880637847cba0ec9e13d`  
		Last Modified: Mon, 18 May 2026 22:41:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d8259f285d3770d9a05bf5ad47aef7b4442519c0e0901a2c810a4be8f2db5d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03dd12f9d59f9fcd669b669aa29281efedbcfd0967fd2f6cc10c6ccb7da360a`

```dockerfile
```

-	Layers:
	-	`sha256:928f7cc11c372535732addaebab10c3e72b190969ba52f28e24d715749edfc43`  
		Last Modified: Mon, 18 May 2026 22:41:54 GMT  
		Size: 3.1 MB (3104399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef58f6e990540a5d2d81b62c0f5d7763eea997c736a8dc66b8335e8dfebf8d4`  
		Last Modified: Mon, 18 May 2026 22:41:53 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
