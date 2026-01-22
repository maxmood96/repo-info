## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:d7e3e517debd6a82c9effed47931ad46d0231078b228fb39ed01e5359fab253c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:f3569588a2a3bbac20d41899eb282a3aad88e75a9b2852bff99ab7eae346591f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163960630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a71a6509d91c03ab899eee524cf2b9f9c6a241ea718402eaba012b47222d8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:43 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:43 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:43 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:16:46 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 21 Jan 2026 19:16:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:16:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:16:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:16:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:16:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:16:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:16:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:16:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:16:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:16:47 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:16:47 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:16:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:16:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:16:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9893ff21f339b1dac915f0c4f4babba1b9eea3f0737be3f8bc2cf8e11d24c0c`  
		Last Modified: Wed, 21 Jan 2026 19:18:33 GMT  
		Size: 148.4 MB (148367172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd2d1c9c7cb397420ff405a1298d77794a84ee17cb5cb7acd69be2381a7b893`  
		Last Modified: Wed, 21 Jan 2026 19:17:18 GMT  
		Size: 2.4 MB (2420067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcf445d96efe8deb5350eede491e813fa73cf0577480e7cc778efb5c3d84c2a`  
		Last Modified: Wed, 21 Jan 2026 19:19:26 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93b3a48646d4111a25fa5ac84b3566f06100fe4b10946cf97a2de517a350864`  
		Last Modified: Wed, 21 Jan 2026 19:19:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912eadfa6c9a47f291641c7c47ebfd52331f3878f7657debfae26fc3c6bef1dc`  
		Last Modified: Wed, 21 Jan 2026 21:28:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8504ded099dbe0952e0787604554d017349c08a365ba4a272a207e709efd55ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73427eb554ad576571dadbcfd68ffe1ea8ab4a54936dce16baae4f3bd86da37`

```dockerfile
```

-	Layers:
	-	`sha256:c597c5916853ea63ce7f2b50a8a0e3d0244181c338dba0a7496b3b1cb591b2a5`  
		Last Modified: Wed, 21 Jan 2026 21:30:22 GMT  
		Size: 727.7 KB (727724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3cb596cf6ffd2150c5090fba8ce12d76ffa3ac29c82dd16a64d729925d2727`  
		Last Modified: Wed, 21 Jan 2026 19:16:54 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b71cd9aae2eb936b88435a93e0edbb03aed722e0e2cde68cbbe0a527d13165c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162682909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9f7605d5651e9743b12b8fcd70861bb83c2a891daf00fae4f8272bcbdfeff3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:59 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:59 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:59 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:21:32 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d87d09c2d3f260e5b0cfb420b36d5fd6729f2919f45b00056a792a16bba98`  
		Last Modified: Wed, 21 Jan 2026 19:19:15 GMT  
		Size: 146.7 MB (146712782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e9b42062843ec3a6a0a9ccb49996961e1fa0c21fa0d990755eb527f3c9c94`  
		Last Modified: Wed, 21 Jan 2026 19:22:02 GMT  
		Size: 2.5 MB (2461098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a17fe90d7519a14c3da3f8e9a3f973e4c46241082de91b482bb982a8b39af8`  
		Last Modified: Wed, 21 Jan 2026 19:21:41 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08a49a0f6a8e5eb3450f6b233d473fbd84a84e97543dae8e25187ab4632d869`  
		Last Modified: Wed, 21 Jan 2026 22:06:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3482c6a612092caac5a725bce28f60582b3f0e9b27c0a3a5e78b12417b19e`  
		Last Modified: Wed, 21 Jan 2026 19:21:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:35457e4cd82c2127a29602454ba6be5567f1fd31ae5873db18904094d5bbcf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd0cb08f61ee1fd4b6d937a39bfc67c9a1baad7334604d9719af39af3369bd9`

```dockerfile
```

-	Layers:
	-	`sha256:704d8c8621677e1d60da07f662b0e7cc39cddd1224e9457c949f2c8a96e0a459`  
		Last Modified: Wed, 21 Jan 2026 21:28:28 GMT  
		Size: 726.5 KB (726481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895e676083fc5c8deae00d7e0c88df6c844f25b60e501fb9ab44b1da5f92305c`  
		Last Modified: Wed, 21 Jan 2026 21:28:26 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
