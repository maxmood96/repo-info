## `maven:3-amazoncorretto-17-debian-bookworm`

```console
$ docker pull maven@sha256:244c2834e50925d3fe77a50c48e76a01450106474d442f2f6754a387547ac8c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:aa21c47b28e91f267a408264e0fe3541f5c6125f1eae3c0edc5f27fc1120a5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239010254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b9f695ca7d4b66fc8d44fc3dc07b9380a96b566606eae96148be836149771`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e076bde69144a86726ea42001705debed81d0ed698aef3efcca1ec3f028af27`  
		Last Modified: Mon, 23 Jun 2025 21:00:12 GMT  
		Size: 201.8 MB (201825683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd7b3642c50114e296728e13948378ec9ad08cc3ee58cda0e2bfe1229b270f`  
		Last Modified: Mon, 23 Jun 2025 17:31:23 GMT  
		Size: 9.0 MB (8953407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c19e0191c319210f6b4ffa2fe02babbf4e857f6ea1ff7ce29a7d9c7d3433e8`  
		Last Modified: Mon, 23 Jun 2025 17:31:20 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6703e822bd06ffdf99d30ff8515070195c370d3342ca44a436fd186fe328ca20`  
		Last Modified: Mon, 23 Jun 2025 17:31:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:bdcda1ac5a5e4fba81e1eaa02861d14cb62bc91181373c8185f48c85612d4449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31364f3ee2dc3c0c78c4eed48299b4a16a91d5ba2cb8da3a301b1a8da1741f0c`

```dockerfile
```

-	Layers:
	-	`sha256:3354f5dd8f07b39256828545ffde7e68051f1841fdb8a18b8b059871d2d93924`  
		Last Modified: Mon, 23 Jun 2025 20:28:35 GMT  
		Size: 3.1 MB (3127850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fca3d24e5aa9aad835fe41cd200d162a34aa90379660296cc1d7035215604a9`  
		Last Modified: Mon, 23 Jun 2025 20:28:35 GMT  
		Size: 19.2 KB (19226 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:dc1caeaf76a2da63a0e3c0642a28c693b8aa6d905cc9d6628e19a7d11a56f88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2301a8366ef4ea2a27c89fc3ce7f4ca1ab124caa781eefdeb9d1c82094aca270`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f28245f77d2b0329fcc24b0cb31e2eb2481758d0e56fd44ada64239da54da1`  
		Last Modified: Mon, 23 Jun 2025 21:49:41 GMT  
		Size: 200.2 MB (200197492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0bb5067522d8253f8e54792058bea344f127f7e370bbae260de16ed876dbf9`  
		Last Modified: Mon, 23 Jun 2025 17:43:17 GMT  
		Size: 9.0 MB (8953395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf493bb4ebde9681bafe6dae300a517b588945d9880e0d435713153a426c3eb1`  
		Last Modified: Mon, 23 Jun 2025 17:43:17 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5de1d8005b6faaec80f352e418314d54ac3e6e4ad7bbc98c1658b7b07b316c`  
		Last Modified: Mon, 23 Jun 2025 17:43:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:003eaab759e8510e022a68a7719eeb50dd80f2aeb1095f46a6ab79d0764b39fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b2da5bee7c387a6f9e729a85fc455c299b37bd8ef6e2380388b71d30176d6c`

```dockerfile
```

-	Layers:
	-	`sha256:d24735a8290216d3e6f2a0629063f8c6a473c12c4a0da2b026b7788d46c618ba`  
		Last Modified: Mon, 23 Jun 2025 20:28:40 GMT  
		Size: 3.1 MB (3127510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a14b63871e0142bb4f95b8a2ba33adec40fcd77e7e47eec5ac24a0f1f72c04c`  
		Last Modified: Mon, 23 Jun 2025 20:28:41 GMT  
		Size: 19.4 KB (19395 bytes)  
		MIME: application/vnd.in-toto+json
