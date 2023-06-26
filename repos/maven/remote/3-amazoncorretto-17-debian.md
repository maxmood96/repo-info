## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:e37d84593789baf3dc13db48366e60e41fc526b00a595535276d760ae12ab32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:6b10c02d4da1a156a38b1d39ee28598bdd05f4ddb2f1ce5deb61a9d23109214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236154765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f02e0b4c7712b94688876d197707a9ea3fde7e84789b65357d2373717d99d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Sat, 17 Jun 2023 08:38:16 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
ARG MAVEN_VERSION=3.9.2
# Sat, 17 Jun 2023 08:38:16 GMT
ARG USER_HOME_DIR=/root
# Sat, 17 Jun 2023 08:38:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 17 Jun 2023 08:38:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 17 Jun 2023 08:38:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff58fb9cf885cc3acfc05f456aee63eeffe0e275625d1a06b94e3e81f0f65ec`  
		Last Modified: Tue, 20 Jun 2023 22:45:51 GMT  
		Size: 197.7 MB (197714220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe9d8d5221c9db3712d34f28ed81b7bd5c4db208bb01137141f7f7b22720100`  
		Last Modified: Tue, 20 Jun 2023 22:45:38 GMT  
		Size: 9.3 MB (9314426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae442c898c7b14c8ed4bdc6c7d9213ee0c508c4f818d12dbc7347ad81615bfd`  
		Last Modified: Tue, 20 Jun 2023 22:45:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3133fb1925042e4cac49905c85c70125cf47fb3ddf860d2853e9960759d92448`  
		Last Modified: Tue, 20 Jun 2023 22:45:37 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32218961dac2c6e22a1b3da2e2670c9ba7763a990d246d6732a55e4f3990089`  
		Last Modified: Tue, 20 Jun 2023 22:45:37 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b8e14bbefe5db135cd335bcea2b3ee6da3555519ba5e9945c7a649be17ff8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234504321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff08a879ac66b9deb71fe6858ba95034d77c295bf5d8d0afd10d3141c09254ac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Mon, 26 Jun 2023 13:48:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a1b03ff32c060b3b033954c71607b836248c41a9d1f4a01ea783196ed4ff5`  
		Last Modified: Tue, 20 Jun 2023 23:02:45 GMT  
		Size: 196.0 MB (196022851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8664e08d1ea04e4b4d1530cd5cb88685e6ee215b8fca3e9c49b7a516f99b54`  
		Last Modified: Mon, 26 Jun 2023 21:51:28 GMT  
		Size: 9.3 MB (9327565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d56bdb55324a1e34ee1d804448b57fe5f982c6d3a69fd950dcffb689297e27`  
		Last Modified: Mon, 26 Jun 2023 21:51:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675a692f31ed082c98f65037218a88b9fd5d3edf4dd53d6c2f684ec679029a5b`  
		Last Modified: Mon, 26 Jun 2023 21:51:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce3fad59de1eaee377ef503bfd52c094c1cdf12a8cf512b777ad148342346e2`  
		Last Modified: Mon, 26 Jun 2023 21:51:27 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
