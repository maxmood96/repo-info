## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:b774d4d714d83c57b9918ee4d9156bf6916a6dfbb6965fcb58b59fb3a70375fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:2f1db9412d7788c57b45b29cb1dc30c2ef95627cc0ecc9d65b89300b53d8fc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266204513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04526c7dbe0b20ea0acc2e08eea84ee800290398dfa434ea3521210b8871c95`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 20:59:52 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:13:02 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:02 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf47845a53ed0b749b91c5909d15a7e3ddbf06e0df083152731ada748999747`  
		Last Modified: Wed, 15 Apr 2026 21:00:16 GMT  
		Size: 201.7 MB (201688621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70409554840c2edcf0954df1630c3b4c3e21635e746107fdf405bcd92b06bc13`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 25.5 MB (25469710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcffdac590acaac0db93eb2e10da584a5d6506b2b8988a15a15a1168c6184d3`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf164c57313f98b9418dee0dd5bafed6b4dc6d019c566da33c4a93f840d1df`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef4ecf23a834f5c6bfc528b44e2456da69c2efc2e6013d2d7816c5bce68f7`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:e5cfa9ceb8e4373021b6ac911db313a09a7d6878464c00a6561b623734a6547d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a9a0742a0d1ffbb811ed9730e6edca75172a68d0c77841d7c181dd33b8b3eb`

```dockerfile
```

-	Layers:
	-	`sha256:ac94c9e1d45bbd007b72a098498d13a7a2a5213639c00e1a9f4e5d3e7cb07826`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 4.3 MB (4320525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e080e102488b05c4a297e7bd03a91f4457438781cc8634fbfb4b986869e031`  
		Last Modified: Tue, 21 Apr 2026 18:13:14 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e7d1874e6f191e69a0cd1a9a44b4d61ff3a891e6404ae41636bae07b97ac9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264143974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af65774c400e4cb7823936d2e75fbab887eaaa45bff4802ed1ab5bb3be45fc3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:10:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:10:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:10:22 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:12:54 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:54 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a8f8eb950b8df62b380d202232755f6cea307b6d9f219ce4ddbf734668703b`  
		Last Modified: Wed, 15 Apr 2026 21:10:49 GMT  
		Size: 200.4 MB (200421498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ce2d46f413815379ec644af54fbaa461337cbb22c6b73045fbed87a5f51f1`  
		Last Modified: Tue, 21 Apr 2026 18:13:08 GMT  
		Size: 25.5 MB (25533432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74799e79e88d9d718f8ff788fdd3d80e49c24dc28d8b9ff4451773c6cf8ca35`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ea50219b41e3291d316fdab983cc3f00b66914dca29fc7e52e13f3db2fe761`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888da7f11e5c2658deff8602623aa92f21510e4f42b21033acc2482a638d6ab8`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:197ac97fcfe4afc12eb402e540622a70b61455ed9fc46f00a8af3ca4605f6009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4341844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2618446b7c259377230cf08a1fc81e7cb8ffbca9d7f9e28b8807adb9bb2b62`

```dockerfile
```

-	Layers:
	-	`sha256:04012aa99a20d7bbc40ed840be7b6b53fa7f9bebb4cb51de08aba0497da363bc`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 4.3 MB (4327047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94959fd272fc283c84476fcc27674ba108cf273ebaeca3d79159184a5ba348b9`  
		Last Modified: Tue, 21 Apr 2026 18:13:06 GMT  
		Size: 14.8 KB (14797 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:3ce9d0d4e62382bc36a1361525be82e698852d42ae766ac073c3dd69829465c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276170295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b254a81618a38f100dc1495e78a5fc653510f683560d08cd9601ddd2e869aa5c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:39:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:39:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 23:39:27 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 05:44:42 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b43296de0f963940b474717cf13b2a268c304a4808244ab9097b562dd519a4f`  
		Last Modified: Wed, 15 Apr 2026 23:40:10 GMT  
		Size: 202.5 MB (202547397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6f1dfe9e7601e43c0c576a592711f9636dd95752073c296ad8d8ce8964dc1`  
		Last Modified: Thu, 16 Apr 2026 05:45:24 GMT  
		Size: 30.0 MB (29995462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a96e33236a565f4505fb31e7147c6de4a642f0aee497fe5f075504454b2a9e`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5ddddf560ad8dfe70ce29379852dc828fba4aeafa0a924455009fe2da5cd8`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d780068099df1a3582cb625252026de1be0275530a6ae7c5d4fc161216bd4220`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:ae012fc87f0c7e18bf3b864342aac913c664a9899d08606981e8a6717b334ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a1dd8e18c44b880977aa10390332580d63a1e79732ebcaa73e02415fe0863d`

```dockerfile
```

-	Layers:
	-	`sha256:9f159d36b8ad70af70c1a30eb3c63d7170d93ec1ab4ebf3b7e32018fe6eb2729`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 4.3 MB (4320954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368c298f94f374d73d110d4a9ac01d7746076060096b030672f76edf2a56cacd`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 14.7 KB (14715 bytes)  
		MIME: application/vnd.in-toto+json
