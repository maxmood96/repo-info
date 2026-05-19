## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:434bdc5df632497c647e048752ac4dc97cd65ec1c3a1d5fc9758c024ce297ceb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:5cb51f5afd65c48ae18f7020903d48565e640f29d7f8c3399e16959685d184b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277647777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ae569c6dad144af29d5b3acfbc6390576acf7ab054f7e5feb5ab5d3b5ebdc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Mon, 18 May 2026 22:42:21 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:42:21 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 22:42:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 18 May 2026 22:42:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ee4e7d170d98234a3a43144957a1e49f7ea87563bc941b20431734300685a`  
		Last Modified: Mon, 18 May 2026 22:42:49 GMT  
		Size: 238.5 MB (238506573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6bcc2fa44c3fd2b572665db5a212991a58ea678267c6298ac28fca664e00a8`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887b2018d7a94e897e20b0d8590d7177d5e37f470a58166949886f22fcc2dd74`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40caccd19de759a1bfd49637734dc639dea9d9c7fc65a2572b029ec4f8fa4f2c`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:9f8e4992a34c2bde6e90c639f4888f69b37b8d61fe9156ca83fa055f1adaf1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2752841daeea071fb35915d5e9cb829df22de54e3d2c8a8b9a2eeea3ec09ac96`

```dockerfile
```

-	Layers:
	-	`sha256:8c609307191e444a3d34500348b81d0f8a07a898005a6b29f5447b8dacc36818`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 3.1 MB (3113735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f788580980540cdc5d92bfc3c83011d77268456f9342fe9e955acc303f0a6c87`  
		Last Modified: Mon, 18 May 2026 22:42:44 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a4710d5f30a5cadf4e1fccc781f208834f650a9c1abe30d5285808e2ebfeefc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276106309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbf932114259205c063cd72bef286d6b8ba0fc929b3444e7d36a8f5f1314a48`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Mon, 18 May 2026 22:42:13 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:42:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 22:42:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 18 May 2026 22:42:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:13 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d32b3c9ee991bd7d3ef148ad5a6edeed21e22a6d520a926d72d48c9e228cc1`  
		Last Modified: Mon, 18 May 2026 22:42:41 GMT  
		Size: 236.6 MB (236601700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef7533eaaaffc1d5d6d6a77969424fc193734c49d836f70abfd2994496fad20`  
		Last Modified: Mon, 18 May 2026 22:42:36 GMT  
		Size: 9.4 MB (9359960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363a4eade012dd391c2a411315387db921a5ad241eace6cc910c4fa85eb5f565`  
		Last Modified: Mon, 18 May 2026 22:42:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76cbe558fdfc99f99f8a324969402a4dd6e8c3cbf7a7be4ea9351fedcdb0487`  
		Last Modified: Mon, 18 May 2026 22:42:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:acfa05fdb525ab0cd31371a9fee238c74f0fb439e02560bbd2302d22e42e1c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603374ae094a8617f896c2dd0cbc4f8cfa38c20b796a5c7b4f39dee33c2330e4`

```dockerfile
```

-	Layers:
	-	`sha256:508aa29d0d1e680bf763a6f1a3a786a4c5d2cce3595da50dd7b4d594553278c9`  
		Last Modified: Mon, 18 May 2026 22:42:36 GMT  
		Size: 3.1 MB (3113395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6af8daba54acddbd073b4ac147ce45c85135a1b02dbed4a04a7ee486b17cb6`  
		Last Modified: Mon, 18 May 2026 22:42:35 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
