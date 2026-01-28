## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:7f2c2bcb1ddac56ffed207824e82b518650ea828ce351f20a7b040cdf57df60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:281c70e90da3a6dcf6308cd067a36179b3bf5a50bd7b13287d35e0a426ddfc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177183731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1431185b0a4ed417cfedbffb779eda624a969d769854c6c336fb19d5724bba8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:15 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:15 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:21:29 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 21 Jan 2026 19:21:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:30 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:30 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3b5bdb09ad91d86c575799ac71f0f8e4cf37a35be2c5430890f6cad8a53919`  
		Last Modified: Wed, 21 Jan 2026 19:01:34 GMT  
		Size: 161.6 MB (161590231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f79db4f9de011b4f71262cf3cf18d2c5e294ec048dfadfe75d8729c294351f`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 2.4 MB (2420108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffccab8019f2ec8374f94e8c90ec4b285e85e127fcfe4170c6c617d3f500626`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f84ed7a41fbb66e845585171386a6ea8e9097f30e43b6a8f66ad5350d54ff7`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce7e1641b89ea5a5d13be13f203c159b4795e2ec602e091f21055c55495ba0d`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8eb353e873cae6adb28613cda8da18274adaae9a159bb0e6a6af0df499e47a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.0 KB (743989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc275408a3300fdeca6030d4bfe6e0e04b939c8edc0ba5acfa57e5236d27a1f`

```dockerfile
```

-	Layers:
	-	`sha256:d0a043fe3bb5d139bb7314a5d16bc8d42f5aa3278e5c548f76a834dc55c0acf2`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 727.6 KB (727627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fba91fd8bb9b4d7e0fcbc899e1e102e97032d778a805ad8760f308cac252e55`  
		Last Modified: Wed, 21 Jan 2026 19:21:37 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bfc01f798db9febc1c3b79875dc7565a09a406c592a25394b9036890805be903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175587116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c296a716b4423bc04d266a8b8533a3db0587a9b2292ad0c166cd3dbd015b3430`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:51:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:52:49 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:52:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:52:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:52:49 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:52:49 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:52:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:52:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:52:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b075c73c3fb61a2595fbd83c3d77b387659de25ba9b2d1de05f9d24ee5f70`  
		Last Modified: Wed, 28 Jan 2026 02:52:06 GMT  
		Size: 159.6 MB (159615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861fd32947bc07175251647cff721170b995234d50cf800605f4e84a84b699ab`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 2.5 MB (2461152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8130488f70a2df6337b6da28336e3c773c8c5ce3293c7e58471dbf92839d3e3d`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0359cda9a8505701c20da4a71d88c33437f081622e6e92d1ca74a016c84e6c7e`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c41eea70931c77162fc3ab501a35da3185695e05df2ef3ecff3e577ee801ba`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3fe4f2d760e14439f40626e0eaea945a5bb47ada4d304f385e2b86803117a4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786fdc1784d091c13426f8e898d9233bacab25d6283d0506f225abcb61e6c686`

```dockerfile
```

-	Layers:
	-	`sha256:7824c26519bfda2143b15d560bab2aceb4551f8f23412a7cb67ea077858a673e`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 726.4 KB (726384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb093424a4254dcd40cbb2a9682221e559848e569ab084a2c378dd86cfb0505b`  
		Last Modified: Wed, 28 Jan 2026 04:52:55 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
