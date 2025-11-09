## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:911d8977db1e75303a6d1e9a9a761732c0df87ac8db00ab02946523e0aa2c42f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:1801ff18c6a46dcc24c89c8a8da3c03a0c63b6676db548b8d007d01f57e99e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274252971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf57238857cd1f8bfb8c81a56fa5cf451032a449e64505b88cdbd7df82d562a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:24:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:24:26 GMT
ENV LANG=C.UTF-8
# Sat, 08 Nov 2025 19:24:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 08 Nov 2025 19:24:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:26 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:26 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c721f02fa361e05e74331e929f313f6b96d75d3e24b108234672840151bcddf`  
		Last Modified: Sat, 08 Nov 2025 21:37:05 GMT  
		Size: 235.2 MB (235231241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ee30e8227c278049e602561c3803a34bf96cba7f1ac443435b6af2028d78c3`  
		Last Modified: Sat, 08 Nov 2025 19:25:04 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc512271b501293de34aef440cd436027e9fdb080e8a4c6252771bf58850646d`  
		Last Modified: Sat, 08 Nov 2025 19:25:00 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b64b7ca9353a6e8fdfedc70acd6261dbe45997e5714ccd2cc8b7387aae8666`  
		Last Modified: Sat, 08 Nov 2025 19:25:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:4f9dca0893ffbba30634c909341fd5fba96c172edb2ab6df59f15fd1f0bba0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e42107582722f7868c578bd98f023070d684d94646d013754d0daa8a2fb64c`

```dockerfile
```

-	Layers:
	-	`sha256:db0e9effd4d05f81442841d8547b57138a64aa0a0f7a698a3729111aa6394b48`  
		Last Modified: Sat, 08 Nov 2025 21:29:52 GMT  
		Size: 3.1 MB (3112967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49405eac7f7f94bc1a63b31da277726285ef736b28b37edb630bd03e33b3244a`  
		Last Modified: Sat, 08 Nov 2025 21:29:55 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d2d29e02bd3898e1df4cef4f5f30d14a8583df33943c6c29db6c89860bc199a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272353494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531d3bef6bb2bce1c16bf007fde4a21130a2adb90cb7ae2b5fc3a5dd4e8bec82`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:24:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:24:17 GMT
ENV LANG=C.UTF-8
# Sat, 08 Nov 2025 19:24:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 08 Nov 2025 19:24:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:17 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:17 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a8c3d54631be90f2fa2c39f0ccb49158b4af0026e03d3cfb1715a44570c37`  
		Last Modified: Sat, 08 Nov 2025 23:06:30 GMT  
		Size: 233.0 MB (232967586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef61e660d367208e0c0dcd837c6d3ab7bad5f08f1e4831db63434dd3cb0793ca`  
		Last Modified: Sat, 08 Nov 2025 23:06:45 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa413c07a8e672a941555c982270232711c346ad2d51cf54bbc26fc42792be`  
		Last Modified: Sat, 08 Nov 2025 19:24:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0e1d8357fd3d05666834e2ee5b567d076b6fa9d87cce2fa58da826c2309284`  
		Last Modified: Sat, 08 Nov 2025 19:24:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:5739a56109b31fa1e7d5ccc4d5e35069b0d5ea753b2d02ae51c8515c877b9dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5784b95c51902eb40c171cc11bd366f7f0069b40e5d557729de3c72aaeb7ef`

```dockerfile
```

-	Layers:
	-	`sha256:0c03ecd8cd3d0f1cf7387ea9b2e14abe22e117cbab2751ffd265402ed46260d7`  
		Last Modified: Sat, 08 Nov 2025 21:29:59 GMT  
		Size: 3.1 MB (3112627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbc4031ac11d9cf926ac5c1a7c8dd9eb68439115f92c11369ec79d293ba7e93`  
		Last Modified: Sat, 08 Nov 2025 21:30:00 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
