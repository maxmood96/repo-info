## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:aa254067a595778c35890250c549cfa3f4bba45eb8f1be2be2bc47d5d818da46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:694da335b3e702d9d8334e9bdeb52fa93b6a1301264fefa79208f52606fcd665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240612475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7def59a223219d1400aa0ceb17b689174a1ef3766b9947acb47f6606ca0821de`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:47:22 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:47:22 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:47:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Mar 2026 03:47:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:47:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:47:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:47:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:47:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:47:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:47:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:47:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:47:23 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:47:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:47:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:47:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:47:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d268699c43ada8982163efba2267f99e09cf8f8a2a012a344ea60e452539c768`  
		Last Modified: Tue, 17 Mar 2026 03:47:46 GMT  
		Size: 201.5 MB (201524761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17094557a6796563c5765a642ef9b9156ab39ddef555a41ca3dec55027cecab`  
		Last Modified: Tue, 17 Mar 2026 03:47:42 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6aae585ecf4206013f5facd66b0824e3f54b9c980a0d45e9e1577c4d6d42584`  
		Last Modified: Tue, 17 Mar 2026 03:47:42 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc734ef5eb069ce2722e3c820ceebe1c3f20cf17a9ce08fa6507faf911a37d5a`  
		Last Modified: Tue, 17 Mar 2026 03:47:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:6e3eafc43777eca79d4c728e9a085eadfeee58ee8a639865b045a5e66a4747fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b945616b9a32b5dd635831536dac5fae17031f0b727a2e5bd84dea6119a75aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9819687e061443156e52345ee3d8bab44019725f119bb47c1a6960fd557b3ba7`  
		Last Modified: Tue, 17 Mar 2026 03:47:42 GMT  
		Size: 3.1 MB (3104087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6405c9ccfd2b8e2483a6f5fad408380559d920de4f7ac646e8bb56804e76dbad`  
		Last Modified: Tue, 17 Mar 2026 03:47:42 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:69c1d95fbfc2113311a86e0758e1536e21c8879e06fd42878f99d9f0f5f8c0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239397605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd36a7200c2c8700ffb8b61a1d08f08f17514e5ebde1edd36bfae57ba84a149e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:48:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:48:46 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:48:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 17 Mar 2026 03:48:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:48:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:48:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:48:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:48:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:48:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:48:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:48:46 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:48:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:48:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:48:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:48:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1932d36a9e7464da6605688de46352a2197d6f9418a3a9ff364996d5a28610`  
		Last Modified: Tue, 17 Mar 2026 03:49:11 GMT  
		Size: 199.9 MB (199946976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89332dc8c4ab06d05343f92dc0663ad97c36bd0fc5082246ccb05766115b6157`  
		Last Modified: Tue, 17 Mar 2026 03:49:08 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e81665c8cceda2551614b75f2e8069a7d2f0f02271200fb20a9696d374fda81`  
		Last Modified: Tue, 17 Mar 2026 03:49:07 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8982f481adc7c780238f22afed6279f8252f475847370323b65388806f60e0cf`  
		Last Modified: Tue, 17 Mar 2026 03:49:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:78ed0cc7f09fc5d7f9403dd645956495d12fae5ce3ef81f5e2053b0280cd6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42df649ffc630a73f7a4e598f21cbee77486a2c285302fb533fe6ad8b5c25a7`

```dockerfile
```

-	Layers:
	-	`sha256:8348053a4b0f8f09cfedbb474b1b32bd56f5e96b9d6a4eefa65db29b2442e170`  
		Last Modified: Tue, 17 Mar 2026 03:49:08 GMT  
		Size: 3.1 MB (3103750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40118aa35f1d0288ce46f51d161d413372ae1898696320cd0bb90deec726e335`  
		Last Modified: Tue, 17 Mar 2026 03:49:07 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
