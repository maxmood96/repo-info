## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:3c2903481cd2ef4e6ff31532c5c1812fb002b23e319581ff25eef2911a4b0d26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:f6abf09350571b1955947bf9590ce2b559f1d08679393caebb396f5651fdad03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256214456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26be225132f62568073b199b4b4ebef1e55314c2e28ad3affe38de035dc8bf1c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aa114cc8844dba1a3dfb3881df4864a06cdb8292f746169c172ef813daaf00`  
		Last Modified: Tue, 17 Sep 2024 03:02:53 GMT  
		Size: 217.9 MB (217916493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9606ce1bb3f4f16fd25930a053f038a6245b8e6f767e8783fc44c7881271940a`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a7fd836b1e13cfc42d743e086369e71621c8999ace1a6a52b9161f5ac8a34`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b1d65607fc52393b57d253257cc9a094dd6d82be2b97f5b0fdc8b121b480b4`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:01d641516500de3997e3973f8692232d443a2e5d8b9d1e9d55094aba90325d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61841c4ad24b529bd148c64b96cfba1ea3c7d544261b6001a6d4c96f9ca14f25`

```dockerfile
```

-	Layers:
	-	`sha256:24e77ade90563a37b41c9458c1d6e40cbf129b7bfe3f235168905822747c0236`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 3.0 MB (2981039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fec6f6ad3fae417b619681f17ba0a8026b2c184d618eeb30904a952e99c12c`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:10f05a5395e7bd95f0dd6ba32004585f1942eb78f2623bf263f114bfdebf98e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253959304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d4ca3459cf1e4980c496a1bf9e4ec60b8a614e3f384f0cdad2aa0996f2f0db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043806bcd82c0c583f231518c1d52ce90ecef41b74ed80435eb2a855b72b10be`  
		Last Modified: Tue, 17 Sep 2024 09:49:16 GMT  
		Size: 215.6 MB (215631273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98acb142d0e1d3996ee0f854611a253181f575deb5fb6da186b96282df1ad102`  
		Last Modified: Tue, 17 Sep 2024 09:49:11 GMT  
		Size: 9.2 MB (9170448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8f15dddefe1fd7a0219fd1fe64a130194f92d70aeba41a479e9b97af0c446`  
		Last Modified: Tue, 17 Sep 2024 09:49:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4f2225d12c00c0ac87947a2433880ec38ecdf570edba534eab8cf760a89459`  
		Last Modified: Tue, 17 Sep 2024 09:49:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4fc321da387d743e9ad8427743d09d9567c29b9fe6b9d09374d5b67bd43bd587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51d6bd498ed3aa8c7e54052331dcda2d7b8188343ffe6df8ba1f1f3814689a8`

```dockerfile
```

-	Layers:
	-	`sha256:c8e2e01baff781a38599989a44505e4e9730ea91fa3a51827bf471216c34e1d2`  
		Last Modified: Tue, 17 Sep 2024 09:49:11 GMT  
		Size: 3.0 MB (2980697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a64e14939428a4bd2e2da2d0fc025110e20deee3d07b6c531c6784d2c55656d`  
		Last Modified: Tue, 17 Sep 2024 09:49:11 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json
