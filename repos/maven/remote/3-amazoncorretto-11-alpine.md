## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:964c680f56ad8342ad629ae929025d700e97be4e20a75d2fe878a9926fa96393
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:1fcdbc3d070ce430f2872ec0876fb09c1e326b12af0a334167bd5824326c982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157029210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fffcf2075287effc3d78b15b7572712fef95273ddb25d0067a139bf328344a9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=11.0.26.4.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c93c1fd4a4c93d3667aeda52b1c7f44ac5911026f0995e47a7e8f21147bae5`  
		Last Modified: Thu, 23 Jan 2025 18:27:11 GMT  
		Size: 141.9 MB (141911792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35de3b872842f1f02b2b64660086fc1a58dbbe42779ba839153775bdc149afbe`  
		Last Modified: Thu, 23 Jan 2025 19:27:03 GMT  
		Size: 2.3 MB (2319683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9c6d499c325977cc8f44d6938c1a5b55552e96c9c957fa0646dad3e96f36a`  
		Last Modified: Thu, 23 Jan 2025 19:27:03 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d28d479f20e34add6bb7d5f86b290039d9b8c0de9107ff4ffd8bfb78339577`  
		Last Modified: Thu, 23 Jan 2025 19:27:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7114f66af2245ffa012f9f3a98a34d7328c616020511270b27d3f13481a6999`  
		Last Modified: Thu, 23 Jan 2025 19:27:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3da7c5cf0065b2f13f56ad0cad25361b38dcfa9d7b4eec29e713b52e00f546b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 KB (538632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af72cd0821cc61fdc527d81ace100d1de5fe56a56e95f1967fd757461a19b3f6`

```dockerfile
```

-	Layers:
	-	`sha256:3e59122638bc5cd3c5b948b2d92a9e05dca1f7de4f2a0a0449d3abb4c6c544a5`  
		Last Modified: Thu, 23 Jan 2025 19:27:03 GMT  
		Size: 522.2 KB (522235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:169ba494e52afdca32d0b2ef75e092232bea29e9969013fae0e3bae12b0e9619`  
		Last Modified: Thu, 23 Jan 2025 19:27:02 GMT  
		Size: 16.4 KB (16397 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2d2ba2ccf957adaeb3e7b57247715f4f751a049e70797e2cce19a0cf66fc9b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155681066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7d8d8ed93e7e06451ddaafac6a9ef602f273003284ad3d5b55891b2868e0be`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=11.0.26.4.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97df340b6260232b1135514dea309917ad91b4b2de7be5cd024bc6a5e22b99f9`  
		Last Modified: Thu, 23 Jan 2025 18:41:00 GMT  
		Size: 140.0 MB (140035031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9c21f8663bdb3591b74a2b55e458640e68c2955d0f5c3aace3e13ef06f52af`  
		Last Modified: Thu, 23 Jan 2025 19:55:32 GMT  
		Size: 2.4 MB (2383794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4230f971778b8c22f23275acb943d02346fe039601e76f71d361683cb805053`  
		Last Modified: Thu, 23 Jan 2025 19:55:32 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb360ddef364a5698b77edb343e8b9231b42476d8222c2601df583fda612c0e`  
		Last Modified: Thu, 23 Jan 2025 19:55:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3990b04e1c6967713ee5879c9ade805246bc295f884ff5c2409b9755a4d41`  
		Last Modified: Thu, 23 Jan 2025 19:55:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cf107be8ae2e8d46e439b9cab3cf9322b9e76a1240785243d5f2a7e7bbf0a224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.8 KB (538810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f342c5abdebe2971ac31e7dec4fa9cb79a41e9264d0b9516158e82263ddad7f1`

```dockerfile
```

-	Layers:
	-	`sha256:43516a1673fc38b3e03b7bfb8fafbebd7ac9c13c23cadf4808256c50a6e10884`  
		Last Modified: Thu, 23 Jan 2025 19:55:32 GMT  
		Size: 522.3 KB (522279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd8cfec3fea75cb7f04dbcce6619d9286cd39c3e36b84a4a1b85a6dcd57dcb0`  
		Last Modified: Thu, 23 Jan 2025 19:55:32 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
