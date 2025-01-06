## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:fb26c294353f2d40475c07ca6ee7850bd083e5dcf07b8b48d3a391d72aa1a467
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:44357e7c1584fc1f52d09712dd83774d84d75f7173bc8a152e46f39d351e2ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261644051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb745bd7ff4626e5c188140d1c8139916f28546f02a7af97660fcd6fd447b2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 07 Dec 2024 17:04:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 07 Dec 2024 17:04:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 07 Dec 2024 17:04:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 07 Dec 2024 17:04:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe81f2c5a3de75f2c37e63f206b358357374f8ea56f7a24775d1037d527523`  
		Size: 224.2 MB (224240995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a53a8e763a560a15e208073d78cd3bf290b589b77065df2db5988414f9fa1a`  
		Last Modified: Tue, 24 Dec 2024 22:38:59 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0483291349ac15c314fc9e17ad4e80015fe2d669c3531e4e821d5812a3ab59`  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dce5d06bbdee8522c0f53f27e58849e8ef88a6fed3225d64946db4eb4b7042`  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:ba9186af9a0faf594fce6a1693e0471537e010b1959b08f2deea76f2eb99088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7228406bd1bb92b265b86e0e3d6ceb201d2e308bfede069d774f35a79526211`

```dockerfile
```

-	Layers:
	-	`sha256:606357f34696756672c900c6d3272ac2ecb3525ce82beda37fd82b08a93a1206`  
		Last Modified: Tue, 24 Dec 2024 22:39:02 GMT  
		Size: 3.0 MB (2997007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58b3efa7c5d98b2fa128b2c86227e73b4bfdcec3b3ca6f8683643e4eb888e56`  
		Last Modified: Tue, 24 Dec 2024 22:39:01 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6b7708f6e3cea8e5e91dda1e3fb08d959b2bce4d571b9ce23c4fb150d10559aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258988932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd50d29f62162ec6f5d66eb1ba469e41c62aa0c686d544f93041d11f7dde065`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 07 Dec 2024 17:04:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 07 Dec 2024 17:04:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 07 Dec 2024 17:04:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 07 Dec 2024 17:04:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2be63af51cb44e2d7e17ccc19aacc27061c7d9b29b4cf89c6a5bbcb7a0eb63f`  
		Last Modified: Wed, 25 Dec 2024 07:46:22 GMT  
		Size: 221.8 MB (221758729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14249ca97659ac8b53330cde3a4d334162f6cf9d2530574ab4ca1dbb4bd64a9`  
		Last Modified: Wed, 25 Dec 2024 07:46:18 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4f0267adcb7f3499d3f377c983d569569218ed6cb1fcc3d0c44a472100642`  
		Last Modified: Wed, 25 Dec 2024 07:46:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c9a97f6814f224ccadd9093718b8d9ce0c3b35ed5bbcbc0ba57caa0466e455`  
		Last Modified: Wed, 25 Dec 2024 07:46:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:b5f15e66c2645de71e3cb1ffbe9cd022856b75745e1f0c834722a8ebe6f44379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6283a058a0b6e748eed2541029eddace850b273749f0e244b8d6ae34382573`

```dockerfile
```

-	Layers:
	-	`sha256:d3b8721d574bde59754c20eefaa2b918626c3309f1e522b473485cf9970a13c4`  
		Last Modified: Wed, 25 Dec 2024 07:46:18 GMT  
		Size: 3.0 MB (2996027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a878d593c4a74b2e18d117cdc557c8368799df81dbe9abdf778ca067d787da`  
		Last Modified: Wed, 25 Dec 2024 07:46:17 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json
