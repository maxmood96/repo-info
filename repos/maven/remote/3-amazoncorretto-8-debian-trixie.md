## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:94f464e260d02c584a09b1fc50667e3c8b2c05d9e3ac7a5923a76b9d51236166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:1e1e56f6dcf24c0e4a81660e8ba53fd03e31cf85f903e8de8d4b67622cf16aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164681932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6219a0dd02c59b7dbb5505146554fae9c294fd1f34c00a72b0c61a9332784bd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:12:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:12:23 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 30 Dec 2025 01:12:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:12:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:12:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:12:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:12:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:12:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:12:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:12:23 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:12:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:12:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:12:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:12:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc42266d882bf4f396ae5e993a62c10024018e6b7d260a0d031cfced5d817889`  
		Last Modified: Tue, 30 Dec 2025 01:13:02 GMT  
		Size: 125.6 MB (125592121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b768f622d5c0714593963a2dcc24e87e4fd94bcaff03440caba037926d6f77`  
		Last Modified: Tue, 30 Dec 2025 01:12:53 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b1522e10911f8f1bf96718fff31262c536a73e236677854c9fef80a10a27ec`  
		Last Modified: Tue, 30 Dec 2025 01:12:46 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee0c6a6e4928cc485670d4c2c6a6f16662586d7898eaeb35a7d6d90aa49478`  
		Last Modified: Tue, 30 Dec 2025 01:12:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:534e533498eb8494a023857ad2f1e42c6c5896c1439f95ea7512c8dad8aa9bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532d6d60bcec4c9d6b4e554ac0a04a714f4c62c886c0e51df71f0f8bd61c7de3`

```dockerfile
```

-	Layers:
	-	`sha256:b87f5fde1fdbb5836bc16fbdff371111e0d8bf2908341ade0dbcc4a218a6ddaf`  
		Last Modified: Tue, 30 Dec 2025 03:29:18 GMT  
		Size: 3.0 MB (2981969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2f297aa56e57fd596f0ca8f6e05ef783db7afe096bd23260b27a7a53f27500`  
		Last Modified: Tue, 30 Dec 2025 03:29:18 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:92e8b8e2f562e14195db6ae29c3c611c1d3bf44b4e87a21f2e9a1f2ee2592092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149018729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924d84028856157ba66742aa7f6f07fc41f8247c56b90c64df53cc9fcccd2e6f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:13:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:13:28 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:13:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 30 Dec 2025 01:13:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:13:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:13:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:13:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:13:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:13:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:13:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:13:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:13:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:13:29 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:13:29 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:13:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:13:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:13:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9e491b883c366d0c5339458f16cf94e3c9e662e615eeb9e8fbf9114ffb18b`  
		Last Modified: Tue, 30 Dec 2025 01:22:07 GMT  
		Size: 109.6 MB (109566809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cbd90aff23df3c40884e76e1e3e6f21e21e905104ab4d1003e010574984276`  
		Last Modified: Tue, 30 Dec 2025 01:13:54 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c694d7cdbfa5a4999975f013f008412d0161de96085e04448d86b237ffe6b3`  
		Last Modified: Tue, 30 Dec 2025 01:13:52 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8997092c092b1c170ce672215a9d900938fc344f7fb35a7763956f95b0b158c0`  
		Last Modified: Tue, 30 Dec 2025 01:13:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:aefa3d4cf7a80eb2cf98961f28f2214b4bdc8cdf56d88f5f82d87c229383f0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d35e331a319304f573dfa9607807b128dc26d3138e3bcc0c331d3fff7c06671`

```dockerfile
```

-	Layers:
	-	`sha256:b1e04f4fba915b5f8119302c33b4ffd1ebf248f642ac44f729615ef103df015c`  
		Last Modified: Tue, 30 Dec 2025 03:29:23 GMT  
		Size: 3.0 MB (2964790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e2782c69ec5ca81ca7d7af1156b2b05460aa208933efbd420091722ffcde145`  
		Last Modified: Tue, 30 Dec 2025 03:29:24 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
