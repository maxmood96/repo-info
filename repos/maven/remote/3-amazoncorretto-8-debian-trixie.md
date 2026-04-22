## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:ac2bc7a4faf135968615e0b918c2adeb2ecf51061ba54050b2cd42c13d08797e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:fe623d489b631970220bca2e1975744973f04adc8d6a8ffa6c83e192e7689248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167695586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a7505d84af6951acb814b45fe32888a521634b0ad61556df6011edd5afddfb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:13:00 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:01 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0472cd9181b3dc018b814cfa2f1413177dbe0d1b02e7b1b4572538044fee72`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 128.6 MB (128606743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8956a339ebfbd8d1441c66297ef04aa33abeb09f90455f812f894ad1cb1814`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ad8817a05c2c1c98d8646db0c1c98fe5aa9d4fd7f6a338ebe5d518884b6f7`  
		Last Modified: Tue, 21 Apr 2026 18:13:14 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70ca3f246ba77687cf7a96742d9c6f7c452ec00eefe4ba54c3e11db625e57d2`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:d41055a1ca265bca40881658fed1d0608590b28a79b83b6725f09e8edef20a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0498b35aad1436d3a23096747939c9e051974f27ef68628d5a3e0fcad913dc8c`

```dockerfile
```

-	Layers:
	-	`sha256:320d2647c3827a945eb2381f30ed27070f1319e51074da5df55b28d0470fa394`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 3.0 MB (2982093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e067bf879cacea778bc3617ef8d377cd1bb3e44ef8f1dea957775014208c2f01`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5959d0c5e11c5687d9bce047c70e5c2085d6406eb7cb5051d0437139604a3c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148847813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a83991784b30f2361225d88b1d4c768a7c838f1cfb92ef6e9430d6a56f8ac7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:26:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:26:26 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:26:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 22 Apr 2026 02:26:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:26:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:26:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:26:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:26:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:26:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:26:26 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:26:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:26:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:26:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acedbe8b514ebbcb82ffbb2a0202bff0cd09e8bcc4387ca7f319903eee04c508`  
		Last Modified: Wed, 22 Apr 2026 02:26:44 GMT  
		Size: 109.4 MB (109390961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c57991fdc79d5e692764e23897e69b9a2fbf7f46b296fe1157e2150ab569f`  
		Last Modified: Wed, 22 Apr 2026 02:26:42 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab60df66ab1288f8f1bc8edd461d5568b0b12237bfd7f23bcc4f3a9815cecec`  
		Last Modified: Wed, 22 Apr 2026 02:26:41 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5949065148cc7ef44a450ed7825ea4733b19f59e14ec297298bde7dded40f0`  
		Last Modified: Wed, 22 Apr 2026 02:26:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:fd0fc2d0c0a512ffa6ca64039fdf6d5d25bf0f71d83bc155e8d66c2c08cb7833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0850f0fa7fb830077ebc7d59342b2d84c906d1ece3f242459fe0bab44b83ade`

```dockerfile
```

-	Layers:
	-	`sha256:12396e2fdffdf1eddc450b226b2ae54e4353e158bf3da22a7fda33a10befa248`  
		Last Modified: Wed, 22 Apr 2026 02:26:42 GMT  
		Size: 3.0 MB (2964914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e142fa3924f73515c47a9726cf62a1636d8294836092f58d8fe29b6b8303a98a`  
		Last Modified: Wed, 22 Apr 2026 02:26:41 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json
