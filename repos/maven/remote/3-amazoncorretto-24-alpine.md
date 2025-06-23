## `maven:3-amazoncorretto-24-alpine`

```console
$ docker pull maven@sha256:00b94de8a9c06ed104afd4f36046ffd8f3287900691c0fb63ce3a2327097260f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-alpine` - linux; amd64

```console
$ docker pull maven@sha256:77e4a686f91bde6f7d65978780724e31fc75d2f0f52175846945de875d4d9a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191561697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c301c7d7ecf9b3f3aec2806de6c3af535f3764a24e5b50953944d1a48e273b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b65aa6e4c59dc2a9ecf9cd2b292e6627aa6a50fa6e96dac665e0d6f6e59c4`  
		Last Modified: Thu, 08 May 2025 17:08:45 GMT  
		Size: 176.6 MB (176603961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d25a0a5c9f7242545a5cf08f38dcea2a987da5ff67af74e32774ce7516ffcfb`  
		Last Modified: Mon, 23 Jun 2025 17:30:52 GMT  
		Size: 2.4 MB (2361039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3969c972a7873589cc8f9d8faeded0b3ddc7b02bd72321d17f75fc45d42113`  
		Last Modified: Mon, 23 Jun 2025 17:30:56 GMT  
		Size: 9.0 MB (8953409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3820dbff7d427aed21790a30c715aa7a80de72c4988f451b6c1195a9c594a4`  
		Last Modified: Mon, 23 Jun 2025 17:30:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1721da3fcbc47b4cf10d86cca1f3734c4a3622e8649e828ee175c48313d6f96`  
		Last Modified: Mon, 23 Jun 2025 17:30:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:26c7e009ae8a4f76c9880aadc9471969d4121781dd6f2b863bc5aecc8662bd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.5 KB (549526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3747955fd7843f82db3aa857f64e0f82cd1fbc48c4fc753820211f87a2592936`

```dockerfile
```

-	Layers:
	-	`sha256:e42aa31fce0a58283fe96dda767487d405992bd28d9450fd90a76ae6ba822dd8`  
		Last Modified: Mon, 23 Jun 2025 20:29:19 GMT  
		Size: 533.1 KB (533121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a826d941de972aea31b2280a678915545860a5a601d6fcfe743c8c80460bd135`  
		Last Modified: Mon, 23 Jun 2025 20:29:20 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a1c9d76778ed19ca1143ce1816cb446156ac9e609656e432027a166e91978f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189643325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cad93dd627a6817bb09bb97c020fd6ecf4b87d28889ad6e2d693970186b280`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49327da051618d500e9ceff8a228ba9990c307f541f032b311e45f439dc87ad`  
		Last Modified: Thu, 08 May 2025 17:37:11 GMT  
		Size: 174.3 MB (174302314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff2bd168716a5cdf0263943b4c92889e502373b9b57d8bf1b73ca96005a5a5`  
		Last Modified: Mon, 23 Jun 2025 17:46:26 GMT  
		Size: 2.4 MB (2393540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1529cea1f9a7ef0e8e7258afb6ecfabdd14f3d93eb9511bb351fb0889dd970`  
		Last Modified: Mon, 23 Jun 2025 17:46:27 GMT  
		Size: 9.0 MB (8953399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28e9c8fb9dbccfc84ff59b77290f68c527dcd061e29104b12ac7a9d4961d06`  
		Last Modified: Mon, 23 Jun 2025 17:46:25 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e456ae0640235a7d191c1372dcabc04d113a4ca290cebcfaffba25ce19f2d9ab`  
		Last Modified: Mon, 23 Jun 2025 17:46:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b09578befd1ac8cfe00ffa01772174831b7da2eaf7d2f76668b52a81bb8034d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.1 KB (549063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a54b039a10619f100f662461e735ad98bdd3c91d7874b70c00ba6d1afe1c09`

```dockerfile
```

-	Layers:
	-	`sha256:50b92beb556466da1bfca1059892d9c2775c01838a9d9dac99c8b05fd944f1fb`  
		Last Modified: Mon, 23 Jun 2025 20:29:23 GMT  
		Size: 532.5 KB (532525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad8a029011bf06d3e3073c36f623aca9c695322adb731802659fbfe0fd34269`  
		Last Modified: Mon, 23 Jun 2025 20:29:24 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json
