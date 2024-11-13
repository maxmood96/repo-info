## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:5cca294efd41f315ed05e31c88c55fdb9c6e595dd38baceb4a0006a88203759b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:47c8e6994e8cb26a0a2d21b8d281b3719d2a25ef6efa78868b3f797108189c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262730833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae63df601d1edf4243caef17f2e226345f76f2e3bdefd929dce01e2acd2a3eb8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3019c95550ecada875489d4eeb8906f084784d9f764f63b58900c1a9fbcd84`  
		Last Modified: Tue, 12 Nov 2024 02:51:14 GMT  
		Size: 224.4 MB (224431377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd86569007d3a7a919bf21eebc32b30c9eb2b73124eb0f88d758fe5c4d0a893`  
		Last Modified: Tue, 12 Nov 2024 02:51:11 GMT  
		Size: 9.2 MB (9170424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1099b145170055d01116dcd723a533fd454b7eb401f0a2c742040b483bac1`  
		Last Modified: Tue, 12 Nov 2024 02:51:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1b6bd31e32fe64b5f3286f1eb28fb2f36fe1ad75f54af239de61b1b165285f`  
		Last Modified: Tue, 12 Nov 2024 02:51:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:862a6db14e416c297714ee612741a9ca58e171d6943fcbe3a38adb82da78d667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042c0cb68dcc9b8c3aa45aa69371b2e2fc1eed6bf02f67d3042d4ef0542674f`

```dockerfile
```

-	Layers:
	-	`sha256:2376867c6e74f698ba9cc7944215f99ba86f8718d47156db58c3f547319b43ec`  
		Last Modified: Tue, 12 Nov 2024 02:51:11 GMT  
		Size: 3.0 MB (3002493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a4f7b12d9d5314baab5f27ac8e948fe2d6731f7928b6e4e70e61640bf7633e`  
		Last Modified: Tue, 12 Nov 2024 02:51:11 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:97755c602d395f5e39a78060631a5d780d41e1dfe42baf8d1272ec8d1303abc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260279032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f493136fa5217af6fa35cb2e0d7d3aef0bd3a7ada97d3f9f36c1f6a7b8394f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93bbeb12d557a6777d33a4b609213c563f558fcce8ae4300dd997fc90b2658`  
		Last Modified: Wed, 13 Nov 2024 01:48:51 GMT  
		Size: 222.0 MB (221950209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe30c50ed74393131781620eece7b47f2fddbcd125d45ad3e97105cd79cf88e`  
		Last Modified: Wed, 13 Nov 2024 01:48:43 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7f493b3119ec27ac7f23129dfd0bd151e5d98323710b89b5fe56c7587a31b7`  
		Last Modified: Wed, 13 Nov 2024 01:48:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf96d906e6569fa697dc05048f94991b6a79ce3807f1ea8e84d9c4e53c8682`  
		Last Modified: Wed, 13 Nov 2024 01:48:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:2cf3b5eaba1a9e1c40db08f7987b29ce832cb671e3f83a6036961a5b422ff75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6747797bee815af3a9f43df79d31ee3b06d6a36d920faaab9da5bb7f3527092f`

```dockerfile
```

-	Layers:
	-	`sha256:050cd47bc70864803193109be922ae51129b36aca11989eac75605da9f993e78`  
		Last Modified: Wed, 13 Nov 2024 01:48:43 GMT  
		Size: 3.0 MB (3001510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8c0374891d2a0070bf6903cd32adc3979cbff33404b52155c379820aaed474`  
		Last Modified: Wed, 13 Nov 2024 01:48:42 GMT  
		Size: 18.9 KB (18851 bytes)  
		MIME: application/vnd.in-toto+json
