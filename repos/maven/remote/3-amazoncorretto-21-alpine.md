## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:def1cec279ce56cc4579fd4e6ce33a8e5d7d4d40aac4f032c2dfa6ab8a437080
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:0e996b318b8efc78b8061a9d39e3cb27485c249503b057cbe28ed364b9c7d164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177280487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914e56a2b1d69ee2ec31ea2d0fd2112cfa246e85108542270b389f45e5f2fc15`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:16:00 GMT
ARG version=21.0.11.10.1
# Wed, 10 Jun 2026 20:16:00 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:16:00 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:31:08 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:31:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:31:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:31:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:31:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:31:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:31:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:31:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:31:09 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:31:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:31:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:31:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc9a6faa2a5c3ad02ee7fbee1ee4905d83e7a8c14a80b040c24ed551a179ea`  
		Last Modified: Wed, 10 Jun 2026 20:16:19 GMT  
		Size: 161.8 MB (161837176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88b0e09af39dd495e62274ed51385588c871df15f9397e09b84ea5bb342895`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 2.2 MB (2215590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda909fbc7bf8258bee6b61000f9abebc1454d9fc25d087b224e61f52c6d28c5`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 9.4 MB (9359959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d69c78db1d115da123b1da46aa5eb8700eff9aea8b1cb55b43d68cba4cf1d48`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be62c6a67eab1fcbc6b6ddfe9dd29b07206cab5a105dc965e4d74f2798d47b4`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:9964529d0fe84e4253935813324bc301ba658c94e6e43205e78bf789648f4d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c8d1bfb0766d4d67d506500c2cdff656ac5892979378ed5f449d2a51e7ee2b`

```dockerfile
```

-	Layers:
	-	`sha256:8f2ca50aa0a527eb53cdd7e3bb82959b8791e5ccc31552c1dd39c1aedab3dd54`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 728.3 KB (728329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047e48e8a3d7b4e3fc194a22a9df2368634dfad756b386c32e8956b3cf27aad9`  
		Last Modified: Wed, 10 Jun 2026 20:31:16 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ef1f524c39ee5d70bb60844aef3cd2ca14f732f735150505931ec06979d6e8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175660764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee5d206cf1f3a0d9cb215a4046d40897205196e6ea73310b25bceb72c6a41b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:43 GMT
ARG version=21.0.11.10.1
# Wed, 10 Jun 2026 20:15:43 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:30:55 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:30:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:30:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:30:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:30:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:30:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:30:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:30:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:30:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:30:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:30:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:30:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:30:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccee2a88b4e1c8439d74b52d439b0fdd63cd2de8c80f2b4059e6c0c0eab83015`  
		Last Modified: Wed, 10 Jun 2026 20:16:02 GMT  
		Size: 159.8 MB (159841708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b50c96c84948fea7979c563530ca20c1df144a5216d14d73da70294499ca39`  
		Last Modified: Wed, 10 Jun 2026 20:31:02 GMT  
		Size: 2.3 MB (2255745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5a077c13952a94aaedb4d13e6bf138ce20718b194229af704a1d91bdb983f9`  
		Last Modified: Wed, 10 Jun 2026 20:31:03 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5026e7e9db2d0f03408549c11084b6f22aee0e7ea99cf103c721ea77349d87`  
		Last Modified: Wed, 10 Jun 2026 20:31:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720d47031b2b5649cc7d8da34491d38ecb510b08181ab5b2a15af276a4bb697`  
		Last Modified: Wed, 10 Jun 2026 20:31:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b446d54accfbc56d659793e0dd4c13c2783570d16cce03b1001da6fd72190d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.7 KB (741745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84184556ca359ff35798067f59979fd4cd485fa85c74bec93cc47749ddad0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a0a00d11604cb241f028a4992287a63b9e60f2622d4b17ea94cab9b5ae32fc4a`  
		Last Modified: Wed, 10 Jun 2026 20:31:02 GMT  
		Size: 727.1 KB (727086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca02eeca7d73afefb1d7d2a7a6e91d0537c6dad54e283f7f44f6dc195a41ad8`  
		Last Modified: Wed, 10 Jun 2026 20:31:02 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
