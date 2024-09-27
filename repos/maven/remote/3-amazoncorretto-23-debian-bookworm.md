## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:db0ab4a3ff62667c49d646d1e4a2e6fc45f9bef80a057743978f74269ec8badf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:b4b93eabe9e076bf27ef5f17fcd0c7cae362b35d28ad9150d2b7ef45e5d146f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262704203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b501befa9b075c99b6506e06b8bb801e89b53246f9437b4b2b4ce50a80d639fa`
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
	-	`sha256:93909851527573871a94677984658317bbb868a1dddcc09b71798d0c34bea5fd`  
		Last Modified: Fri, 27 Sep 2024 19:57:14 GMT  
		Size: 224.4 MB (224406460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca9fe5fc3816546b9f06e4a8b7ad8009c06d1e2502d0a1c0ac97dd3070a467e`  
		Last Modified: Fri, 27 Sep 2024 19:57:10 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285fd7d3e9ac2f92b8fd07d922780ea03450b89a03baea0d5198712e66210601`  
		Last Modified: Fri, 27 Sep 2024 19:57:10 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba7b4ed20cac97dc52c94f00e359e211a0941ca443eb9479747e46abeac58f`  
		Last Modified: Fri, 27 Sep 2024 19:57:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:d8088cd3af3f1a4a3f395ed1d4cbe7f4ce64c6b7fb4eed3a3e2222fea549b747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8114c87803523834d34df9328b571db60f4ed554833298c6bd1d8ec7c7a26f2`

```dockerfile
```

-	Layers:
	-	`sha256:b77b419f1c68946842f0ed6891d42d02155427499f2570ddf71eabff82df17b8`  
		Last Modified: Fri, 27 Sep 2024 19:57:10 GMT  
		Size: 3.0 MB (2982996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d983015a40f118ca73e5790eaf16f444a76e8fd1b13299a82cdf741e0cfcfac`  
		Last Modified: Fri, 27 Sep 2024 19:57:10 GMT  
		Size: 18.5 KB (18487 bytes)  
		MIME: application/vnd.in-toto+json
