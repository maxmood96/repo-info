## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:e3a3be8fd0213eedb90a0d7d4d63ca2b2bb2a548dea93d428587d39a37b2a2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c83defd2b744b92cb54090b9e217074a4dfdc8365e09b12d1a5ab9446b6ed5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116358159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdb20f28a64a85a068d53420ce6f18e58be1eb432972bbc6d1c1422d78c7d98`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:25 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:25 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:25 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:30:22 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:30:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:30:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:30:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:30:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:30:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:30:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:30:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:30:22 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:30:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:30:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:30:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:30:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6833e8b5869e0f48dfb0827fe8ce0f2ec7bc4abc9a375d40ddca18d755ab20`  
		Last Modified: Wed, 28 Jan 2026 02:43:38 GMT  
		Size: 100.8 MB (100776920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519963fe7904ecf1cb5d914969ea368c648dbee20551ae3baa2860acdac6a335`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 2.4 MB (2406146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3bb763e6371fc16e63e187d3e0bfb9dc9882aaa1f77414616e93e1e077d18`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1685927e507b7a9dd41ad2e41824f9419b1ee9b95a296c45fff2464a92b131eb`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8615e356adb930133c6e9b5fad5767010d41b03f221ec44a2718deea2e1de9ee`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:1053b7cd430778b542e9cc3f345405cea86ea734e5eac98c8957c82a5e2e2b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 KB (408619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc00500ed4092774b8164bd029e5aefd75140dced61d9143a468d4c4290247f8`

```dockerfile
```

-	Layers:
	-	`sha256:3055cb4e36cf5e59147e993f018f3e691411962371e7e89d6f9bee4f6bbde3d7`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 392.3 KB (392266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6671f198e144f60db05cea63062b60a0c677aa95ce6673a1f9e325a7e0d4aa03`  
		Last Modified: Tue, 17 Feb 2026 22:30:30 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6bbbde273e81d05cc5bf28512c2c2436abc19e0e0aa7afe0b5555bd59916e4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116522815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a9859c7fe8ec44b30464d507dd2c7d3e9997027a0f3a116a99048bc505b965`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:37 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:44:37 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:37 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:18:39 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:18:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:39 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:39 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de2205b433b6497cae9348f3c144e29b2543b5f31a88ac9bd1041c4ca96f43`  
		Last Modified: Wed, 28 Jan 2026 02:44:51 GMT  
		Size: 100.6 MB (100563666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc9e7ac8e2bf1045f0c33f3e3b85694882f0d618ccfff68b2ae24a6a933e13`  
		Last Modified: Tue, 17 Feb 2026 22:18:46 GMT  
		Size: 2.4 MB (2448767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2867c4aecbc07139eed22329bfed342d4b06bf77b619128fab18ea6ce198588a`  
		Last Modified: Tue, 17 Feb 2026 22:18:47 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb38251a76fab882252b6d54fefc1def48ff003a4fc9217d9a74c4010373a6d1`  
		Last Modified: Tue, 17 Feb 2026 22:18:46 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513ddcdf921a063a860b0fe3a93e9c56d7969ce571181ccd7d1f619c725a664`  
		Last Modified: Tue, 17 Feb 2026 22:18:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:a905656c707eb7d558b848f878b6c0f6a466f38ff866a0d49f34ae8e3d8bb0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2df5f697e172ae0566fa5cd601566000e7269b50afcc9e736a098431f18e432`

```dockerfile
```

-	Layers:
	-	`sha256:a002d5809979131833aa7267e7db370cdf97b1c032558d71541601d0d018841a`  
		Last Modified: Tue, 17 Feb 2026 22:18:46 GMT  
		Size: 391.7 KB (391736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3b7c72ebb2fbb603cb8cc3f85a7766373bd6ce96bc9814128c9b7a786998f`  
		Last Modified: Tue, 17 Feb 2026 22:18:46 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
