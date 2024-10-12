## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:0321a8e45e9b4cdafd7357ca22695fa4ad9890946dea8af234abf3ea31f533c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:7fc479750cea575dc323bd8fa2eed516824742d105b74d860b34475645f1883d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262704349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299cec1fdb8c0889abbda7e9cc54dc4b321eb44115a6309722f0307f26b60cb1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9232b3e64efd7d2e5c5c0f46f97dd02315c21197adb389d876546c72a7eca0`  
		Last Modified: Sat, 12 Oct 2024 01:55:51 GMT  
		Size: 224.4 MB (224406612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b63e03c4ee348c2056dbe7f81211aff173fa0dc65b0eafee2c8946fec5ac50a`  
		Last Modified: Sat, 12 Oct 2024 01:55:45 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e6fb399761ea72d430d3229aee1442166f0fafb6e8b46e04c5284cf9df72af`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97a28303929d640f8f446e8542d9776de5f5b1a4e9e41e83bd59a1682d7cc7`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:f24ba588d87f4b342e8e09acaa8c47e5bfe5e3231492fd348a6ab31cb4e02bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4421629ae9b711b62264c8d3451e5aea086ced32ba858cf9f8d81ee635ef140d`

```dockerfile
```

-	Layers:
	-	`sha256:fb1a10b58e27e21259c9c1e4e2b016d0c41d9b1f66fcde0fca90f4130767cc04`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 3.0 MB (2982996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed35257f3cf3416cf4b212c6dbd34c07e8be449681f0b043b3647ef565e13798`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:547cf27a2fe7f165dde57fc8b547ccae013ec44c6a11a1faf46d1cf636956462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260252290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4541cde5d2cbdc682f73d89b423252b550bbebadc34a438d01f72935dfa8850`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d4aa6f8f9b7998e499edf2cf42b7d16fc8198849ae2e0b6c7d8e779b69e5f`  
		Last Modified: Wed, 02 Oct 2024 07:09:04 GMT  
		Size: 221.9 MB (221924461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30da3086ba3bde18b513afd08dff476f3f388a86a70329a443f08959abf070af`  
		Last Modified: Wed, 02 Oct 2024 07:08:59 GMT  
		Size: 9.2 MB (9170425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9a779bf1f3f6ef93cc23d92fbadb37f9fadbc3ace1009508a062266b45d19`  
		Last Modified: Wed, 02 Oct 2024 07:08:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1aaa04d5191c60b49574cfd4ffc2626023355154d208a5e30f89c0f323f79`  
		Last Modified: Wed, 02 Oct 2024 07:08:58 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:deda90ce3a3a1cfdd1147449c7ac1b0c457a99205c21b9916a740415c562e416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3000699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3071543858ce04cf089ac572095356cf25fd797f96a6c562c0bc671e308b602b`

```dockerfile
```

-	Layers:
	-	`sha256:0a653792a2e0a9abfdc9864022dcc80fbf118c78a8b4f447ca28e2ac4baacabb`  
		Last Modified: Wed, 02 Oct 2024 07:08:59 GMT  
		Size: 3.0 MB (2982013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8b426912094dcb43b4e82de0a54b93088304ec2a69f854e0d2999518076f88`  
		Last Modified: Wed, 02 Oct 2024 07:08:58 GMT  
		Size: 18.7 KB (18686 bytes)  
		MIME: application/vnd.in-toto+json
