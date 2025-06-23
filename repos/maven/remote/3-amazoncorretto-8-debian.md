## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:8a47fb022cf75b49d221168dfab20f6093ac22e2ebf44805b58de21a52139ca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:e7764e395dc4a25ab9f4c21c2516af78424a38c5b4b7287caebfe47f3e06b317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163409335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7890a36d7e9dac9227d0422eaee20ab392d13c9182d00de85bfc550dda320e7d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:f2e1bba336de1001a688901ecb735f138e47099a9233ef369066d10f1c7ef083`  
		Last Modified: Mon, 23 Jun 2025 17:31:30 GMT  
		Size: 126.2 MB (126224771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6a36ac672673bdd6d637b6ad51d9f81c16eac3ec034d97a114fd41c4616b07`  
		Last Modified: Mon, 23 Jun 2025 17:31:24 GMT  
		Size: 9.0 MB (8953401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5440c3840999453fb37b6668bcf082e8fefdeceace397fe2d661aa17efb6d732`  
		Last Modified: Mon, 23 Jun 2025 17:31:23 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f5225e62dd54e6bdf1a87997acdc710afda51a40203b17e8f1746f0631874d`  
		Last Modified: Mon, 23 Jun 2025 17:31:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:0aa1e94a3c622cdbfcf22a183ef336b45e83d31a2aec2f8fb6a6b6e7015d436d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b64ea618045ea1b2429b7f0f91cd947a587e38325230073b07ca823b19d2cd`

```dockerfile
```

-	Layers:
	-	`sha256:ecaef10efffe767fc68221e3600e06e55166c98df75ece539c84a7a865bc32d4`  
		Last Modified: Mon, 23 Jun 2025 20:29:48 GMT  
		Size: 3.0 MB (3006492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4cfb07e38593df7a75996ea9ada12dc39d8237982fdc69e2a49844ff4d13732`  
		Last Modified: Mon, 23 Jun 2025 20:29:49 GMT  
		Size: 19.2 KB (19233 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bf716915ad1937e278517e2d7697ca55c7997e7af06dc79513070793d8733000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147033864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f8b7a725717f269eda480e6c16defaf0c051f31aa2bb71f20e05d588aa0b5f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:2b4c72fdac57941b77dd965c37fd94e0820ce625a9cc4b6a14a99ea43a003bfa`  
		Last Modified: Mon, 23 Jun 2025 17:47:55 GMT  
		Size: 110.0 MB (110001774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1411ee9966a8f56dab064a51370076e879f09cba2b1e87cdd979e0352326fa5`  
		Last Modified: Mon, 23 Jun 2025 17:47:47 GMT  
		Size: 9.0 MB (8953378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a233e038678b5a1a2f276bf9e1f2304ef9646a7ae2131c4b5a7003419863cbd`  
		Last Modified: Mon, 23 Jun 2025 17:47:46 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf59ce8f2342f78aee33ea0bded90ed9041a78d7d90dab10bb6ff070b0bd48d`  
		Last Modified: Mon, 23 Jun 2025 17:47:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:3e24f1220f526c16cf23e9e28f91b34cfe3aaf492fc31a8c684a4f9e17f658b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3008713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4a326f711ccf98f0daec2b8637486688ea9657a3e3dc4c092b3a91899314e9`

```dockerfile
```

-	Layers:
	-	`sha256:e2ee5b99cd1dc2dee9360eb425ef4975c4b4a6bd0d465988fdc53383cec3638a`  
		Last Modified: Mon, 23 Jun 2025 20:29:54 GMT  
		Size: 3.0 MB (2989310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05629a91cd579fc7fa29d0472ecdcec3aa13e8393c14f2527f8d9b8e00e98cb1`  
		Last Modified: Mon, 23 Jun 2025 20:29:55 GMT  
		Size: 19.4 KB (19403 bytes)  
		MIME: application/vnd.in-toto+json
