## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:54bbf6a80a9a0de147c5c604462887af0d003e3b5cbe4f533a9ed9738027fd26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:b4c03d03f8e8e1eb6c142f4c69bdc12024f885aa231c45ca2f6e60dfec97ecf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256214314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cac060fed3ac86f56c15390505f50ad39d2fe18ca4bb8ed6bc7a78b1585bac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f823089ba086ee91e5f1b602075c0df15c4c4125c8cfaf661cab2a744b504bd`  
		Last Modified: Sat, 12 Oct 2024 01:55:49 GMT  
		Size: 217.9 MB (217916577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf830762736e16241b7f53cd3c0f07ba0f06f0c6facea76959c0468c4523a64`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
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

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:033b23b70742ddd0c3c07e0ef14f8ae4a1065850babd3a0a39f7874192bb6792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c0da2944d5b1a6e3612f7a78aa08781be9b58441e79b27dd04ee593e8a2d41`

```dockerfile
```

-	Layers:
	-	`sha256:d8ee1a1e6636558c7413a79f0df275b065ad802795d1ce96bff0d3e655584002`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 3.0 MB (2981052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839aa84fd64ce13f5ad334c693d160fa54847d59470f6c12e8e65363dfde9584`  
		Last Modified: Sat, 12 Oct 2024 01:55:46 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:46d42b786fbcef688f50ae18bd65c81aaa4a15b918193fab8aac608102205aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253959076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37de65ad89d7c6e9dbfb77153d03a12b28a0f1a4220364c4e87bf53e157f53b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1efa49225c805c289d110df760fb867733005d90c62f6f20e6a8748f20d1a2b`  
		Last Modified: Sat, 12 Oct 2024 07:18:30 GMT  
		Size: 215.6 MB (215631241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f469993ad7737c4dc10d6b3e50553c5c91f4ea8b2e5cc6196d64a49d3c50f1`  
		Last Modified: Sat, 12 Oct 2024 07:18:31 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e50c26ea92f657e73dd20629902efc9b5a5ec801e71e11960867a01162d78d8`  
		Last Modified: Sat, 12 Oct 2024 07:18:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9278681c69d5845bf1a4e0027dbc5eeabd77c7c08c2fbb55c1da05d15ee3317`  
		Last Modified: Sat, 12 Oct 2024 07:18:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4ee14edf05ee8981eb56511cb7ea4038fa1a335e7545006c19aa740ac6749e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a7cac4350c9b5aa35c981132d0834f8d69363ad2902fdeb050d8c00e961f8`

```dockerfile
```

-	Layers:
	-	`sha256:1a4678d38130c76e7bff3e19a329c2b9557143f10a9c84bff5be6864d85060b2`  
		Last Modified: Wed, 16 Oct 2024 07:28:58 GMT  
		Size: 3.0 MB (2980710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9ad5e0def68334b274eb85173b908c406279fdde84e98cd1461958acb195a0`  
		Last Modified: Wed, 16 Oct 2024 07:28:58 GMT  
		Size: 18.7 KB (18719 bytes)  
		MIME: application/vnd.in-toto+json
