## `maven:3-amazoncorretto-17-debian-bookworm`

```console
$ docker pull maven@sha256:978243d921dee59c9f4bda444977c5ae62f1cb871722567021096acdfeb700d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:da05eb6bdab1ba0891a79b5796403c6700f9cd63a843c5c3df13d4193cd53540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239119087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e4a5330baec48a31cf908707f56ea5b46b3f53b4b1ecf2a230507b353ddfab`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b390284a4387681e87ce263b488bea26910cfac3dc53444484bf39cc9a43a3`  
		Last Modified: Tue, 04 Feb 2025 06:15:40 GMT  
		Size: 201.7 MB (201735316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ee4a6269af379593ff21196e045be427a935d1f0c1602f6ff7aaeae96f727`  
		Last Modified: Tue, 04 Feb 2025 06:15:37 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8668a365c754b55f21177a16391a064dc535e8b27095c4c3079c1b8660dbe2`  
		Last Modified: Tue, 04 Feb 2025 06:15:37 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941f1b182e3dcc5aa81bbe3e1d0ccce7a61ab54f4f29b038fd5541c5e50cf66`  
		Last Modified: Tue, 04 Feb 2025 06:15:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:b74e32217cfc46e34d581e920c417ff0a91b7be059b24e08015776f14792a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf5a41795fe61c53334e47fa205672adf69c156ec897ba2ee120174a47b6dcd`

```dockerfile
```

-	Layers:
	-	`sha256:6e0be41fe2636769d1494d6fe4388ad85e1cde5c10014a0aa56071bcbbd38fee`  
		Last Modified: Tue, 04 Feb 2025 06:15:37 GMT  
		Size: 3.0 MB (2995161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beaaf9d12ace8a89fb0f32639afdffa2cf7e33307ac1470712d96c5ae9ee331e`  
		Last Modified: Tue, 04 Feb 2025 06:15:37 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2c7bc078fcd3a4e69858cd6fd90955f9a50024f2b12101d46b3f8e14b62b3f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237314036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58154b1c71a408611c67848159d262e9e352d36ffd85f62d8f3c480dc344726d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca08cc713a07357de9827bdbedf69aaa897e0aa62b377fef581dadc8c23f329`  
		Last Modified: Mon, 27 Jan 2025 20:21:21 GMT  
		Size: 200.1 MB (200101545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768e88ffa56a66565ac3313533a8aa250f14e3325790ebe1e5d40cc45dd317a3`  
		Last Modified: Mon, 27 Jan 2025 20:21:17 GMT  
		Size: 9.2 MB (9170424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd51b47c15f062e9e67dca9eb3d5d5fdc3fd3fed94e108e9e3948322378b9c4`  
		Last Modified: Mon, 27 Jan 2025 20:21:17 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a3e6507e3f1cebc09f1278b7a503edc071f485978d6ed91e58db3b8036e1a`  
		Last Modified: Mon, 27 Jan 2025 20:21:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:828e5ed203d6f8495d7559190bb4656ab5b764777430e39d62211f297c3eb8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e2d8c563d164c25986f63e6c3fe083a01ff1df3e9ce95ce78468170096cdba`

```dockerfile
```

-	Layers:
	-	`sha256:c09017cec1fcfcbecdaf2b3a714ee6264115e2a53c93736e72c9ec1b8b46c414`  
		Last Modified: Fri, 31 Jan 2025 06:40:20 GMT  
		Size: 3.0 MB (2994821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea102d676710557ce1805e83c211944c3a0b3442f78ce592c79f224b99d9951`  
		Last Modified: Fri, 31 Jan 2025 06:40:20 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json
