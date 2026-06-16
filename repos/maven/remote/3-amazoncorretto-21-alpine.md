## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:455a57f42314bc26fd953f63dca57f0e8740ba935a3af7189ddfc756a4bc64a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:9a8aaf4886975d9c31a71fcc28a4fdd7af439a28f8125e0daf196cabe6f1663b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177260184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e572c28b36de9404fd24c6b03602a6c7dd810df794f5f0710ca970d84ef4e825`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:27 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:19:27 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:27 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:23:00 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:23:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:23:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:23:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:23:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:23:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:23:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:23:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:23:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:23:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:23:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:23:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:23:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989fc81d937729a00dafca55dbd23dc5a68a72a2a59d2f999819aa71fc5c941f`  
		Last Modified: Tue, 16 Jun 2026 00:19:47 GMT  
		Size: 161.8 MB (161837219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0424397d2aa70cd982986bad6390da414fa4d6f5286a1f715c071ad0b9b20637`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 2.2 MB (2215598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee60fb05bd4499a85e1ad72fdb174bd931e7db3023b4dbc0b82c167fd53c4304`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4483247676137535a5e9ac9d1d2107f56f28b845715122409f478f693ec2299`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261705ee7bcdce476cb3c125f1f3d63e1a56aa03c561bd7bb9e3eafce2883888`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:9f07a1c4ee15beb285124bf138f88098b1529e18c829a7b2b4bb7297f2b5853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ffb88f523bc4b455b4fc923a05f16b226484689e7a0e9cbd4edb654e3326fb`

```dockerfile
```

-	Layers:
	-	`sha256:34406fb3ee7b38239ea38f8601984a99404f4be1abb070b7762845f8d9451e81`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 728.3 KB (728329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbc9480ef4f98a828e4da154b82d0422109977f46b5debf316e6b1a7a7e2bbb`  
		Last Modified: Tue, 16 Jun 2026 01:23:08 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1882b4bcbb3780b05297052cd23764e5450bfa997546719cb23620024d6ab8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175641509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c8decdc090b21a7f24562c20e57c535292bdbe8806de85d43eaac7a6e1c3fc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:35 GMT
ARG version=21.0.11.10.1
# Tue, 16 Jun 2026 00:17:35 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:25:14 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:25:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:25:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:25:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:25:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:25:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:25:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:25:14 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:25:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:25:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:25:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77b0e734531ffce2dd53a41d8efbea96cb25eff325d8480cac6ef130b7bb81`  
		Last Modified: Tue, 16 Jun 2026 00:17:54 GMT  
		Size: 159.8 MB (159841745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328b6491802c9b2438cdf2d090cc1d195644371c62fd47933bf3472c8d64f5f7`  
		Last Modified: Tue, 16 Jun 2026 01:25:21 GMT  
		Size: 2.3 MB (2255759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9179be0ee180463198c29aabd6237a4ca992605392a8342941cdef4cf42b737`  
		Last Modified: Tue, 16 Jun 2026 01:25:22 GMT  
		Size: 9.4 MB (9359961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4884b96fb6c246c876f07938a3379e5c4673b86247742cfa88b8452d735b1f`  
		Last Modified: Tue, 16 Jun 2026 01:25:21 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2e6d5ef04e5764a32e93c3c46a55bedc7bf75b9e2e325356f75c5993d8150b`  
		Last Modified: Tue, 16 Jun 2026 01:25:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c2728a08c0e9387d46c469286edd20e75dfb136894ad568886522a2b6c29994e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.7 KB (741745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a5dee522fde89884215c07924420dc7e78f8f0080434561ea58cc3f2484dcd`

```dockerfile
```

-	Layers:
	-	`sha256:cb21b61a6008a3b9a1c42d8266a2fd2693dc0ce4fe4e72d3581c5d60e0daeb64`  
		Last Modified: Tue, 16 Jun 2026 01:25:21 GMT  
		Size: 727.1 KB (727086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7fc64de6b6d087258bdbc1e3239f97bdd89116eb64847168c7a9106db6e2a2`  
		Last Modified: Tue, 16 Jun 2026 01:25:21 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
