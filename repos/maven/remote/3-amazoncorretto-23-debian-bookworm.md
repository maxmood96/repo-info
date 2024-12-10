## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:3a22c4dccd6f0509a8bf82aab8e614628104659871e7b5a8cc8f3f337ea5436a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:29da3d97b320f8cf5abcee06c7540a5b6da123543b411645fe425eaa921cc849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261644045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8722af39cfd7974db197cf3417ae5d5c7c30814161a5d0ed48772a91edb52d56`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79347c5dfb5b7e191a5f422d3bef6a484f6964a75b11ae6c8fb356d5465d8d5`  
		Last Modified: Mon, 09 Dec 2024 20:31:50 GMT  
		Size: 224.2 MB (224240990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6722fe424e3619e348376ffd1cc75b2627be5d1cacfda4366c48ce9b41edad`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4270152709991d7e116db0878f19955217f0f7d3acd7adc2dd443ec6df179bc`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392805aefd4733a800c2876a2fbff766c1fa6b8e3fccd588787ce4c536b74a4`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:70bfdeabc81a775e298ac138807ebbfec9463b4ec556669d9805ec567e38acb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378881e273445887693e7c8b10a3fb204df4301efcc042840e69090b31fd139a`

```dockerfile
```

-	Layers:
	-	`sha256:2cef979391edf0e810f434439a9c0141f9be41648fff58b8d5cf43eb75dab063`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 3.0 MB (3001245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f3b0757914a1d81b6a17ecdf00f1d421bbdc824bd3ed7b36cabbaea9a560d6`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3cf7b0ace83c6b111af31111b84fdd60a1ade06e5da095edb77b78c1d143e623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258989085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46b67e0c056a894347ffff7c0a2f33ee83d16bfeb994207b2bd3879e5d64ee1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624a9b0b037c5de5c195cc9d12469175d5cafc7832ab7251eb6f46a3baf72f3d`  
		Last Modified: Wed, 04 Dec 2024 01:12:56 GMT  
		Size: 221.8 MB (221758814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d1c2606fb2c41e78845d7ba4316ed835f277287a8633a726368107ffb615f`  
		Last Modified: Wed, 04 Dec 2024 01:12:52 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cbfa5d575c676dcacedb68eb54141bf6a2ca85c6ebbaa95329741084a09f58`  
		Last Modified: Wed, 04 Dec 2024 01:12:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c315b671724c26a33c0a9e3643b83996c36e6a8d7244ac3e0558560851da1dae`  
		Last Modified: Wed, 04 Dec 2024 01:12:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:a370c0cfe89b1d8a6ea1542a0b13c6ff6992e633c07fa2c73913371b1c15bb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2380b444c1cce700fd618f6e799fb25a39e5d31d57007d5fbb708c7280690cde`

```dockerfile
```

-	Layers:
	-	`sha256:d7a5793f2e0eaeea1d4ca1a54e348526c4ace112bf1f84b3d298ac18f7d57dc2`  
		Last Modified: Wed, 04 Dec 2024 01:12:52 GMT  
		Size: 3.0 MB (3000262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc41a68e588d69612e516fa0b203477996ff4f3b7860950e61556fa572b34074`  
		Last Modified: Wed, 04 Dec 2024 01:12:51 GMT  
		Size: 18.9 KB (18851 bytes)  
		MIME: application/vnd.in-toto+json
