## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:fbce371aa5a02231020ddee160999378621d610c1fe9a8209ed29439dc90e022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:74ea209e2fec182f041de37031b2d9292bce0c9b99122cf485258a74ecd31518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164050205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9ec90414f18e40374502f9da0c720576489685dc6ebdcf55844d8bc6f8d755`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:53 GMT
ARG version=17.0.19.10.1
# Wed, 10 Jun 2026 20:15:53 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:53 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:31:27 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:31:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:31:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:31:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:31:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:31:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:31:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:31:27 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:31:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:31:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:31:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c90a3d6425ebf27ae605c6f85d643cfc2a5abeccd203ca236c44adaed9485`  
		Last Modified: Wed, 10 Jun 2026 20:16:11 GMT  
		Size: 148.6 MB (148606896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ee9a5b01d89158aa65740b7a13f050d3beed8f04d5b5c094d6e39dae75c83c`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 2.2 MB (2215575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f5889dea6744c2dd0ea0d5e63ca9e86de9e4d702354e09254853124c08d8e`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 9.4 MB (9359972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f591ebd92791257b7aabb37b291feb51ddb36aa7b28e9cfd38e057101e9aeb`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a253635cd542786280d8013d39a73fb881ed1699ad8635a81aa1ee551d51bf8`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:2feb7576d10f36c84b7ef41b4ddef7db7229c6654539d6b1a78c6a5a0fc72c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c8192143a5fd744e7ad3abec41a5701c337ab035883a47e4d78edc978fe02`

```dockerfile
```

-	Layers:
	-	`sha256:9bb77a8d92d426d6a862da608011349bdaddca90cb13778bc2887fccb324402c`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 728.4 KB (728426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8dac72d7f144eab38216a22e48a25bc57e1fcfce6aaab5c578c35aefc588a91`  
		Last Modified: Wed, 10 Jun 2026 20:31:35 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4b6d1cd1ca66c297b3816bd215b7ad87b46e0aba574d9ac13ce33c73e4d37923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162772581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15215c902c48e38fea3c70e19553ce33bca4b9dcf36892edb29006b44654f515`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:34 GMT
ARG version=17.0.19.10.1
# Wed, 10 Jun 2026 20:15:34 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:34 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:31:23 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:31:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:31:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:31:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:31:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:31:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:31:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:31:24 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:31:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:31:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:31:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2292cc84ef6bd7f474f47adf298c1d2f809f51ecbab69da7b8984f449d56a90`  
		Last Modified: Wed, 10 Jun 2026 20:15:52 GMT  
		Size: 147.0 MB (146953532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cee91633f8ee4663fd83e8ddda9ea9af2d98075e23adab5d02b9986a851d21`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 2.3 MB (2255738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18df176ca615143d9cff09111c79edaecfd8601b222fdacb1b28f4d16ec49dc`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6c6f789501450d58fe6736c672fc86bd81e39173c9092b53ca491f2af5bb57`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127aeb780b38266ef36a7f4e0af49582a10c9a2b41054a207ca9a2c08d3b8d6b`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b77bee1431c57d1f40f2bbcaef9c6e7abe4ad7067986210b8bf2073615584dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.8 KB (741842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64d435f0a20a50cf74c7acabeae0f62bb2f71f4999cd27a557cc8855e5ad415`

```dockerfile
```

-	Layers:
	-	`sha256:1665d47e324ba7fc87475e265cbc93fbd8d274486bd3e35ded2c234d152d6f7f`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 727.2 KB (727183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b1b536c7d925d47ad5583514b2f24618a036fd83264f034dba9a8b5f538fd2`  
		Last Modified: Wed, 10 Jun 2026 20:31:32 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
