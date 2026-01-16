## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:405f5ed266fde405307607eef8e289a0a32dd83837eda1a4d7f87a2b8d6a4048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:6d328c0a791bcaf712c04c873f38782beef9ce4814df9ef7f9a7676938e778ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163841675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37518ed58c1562e7d41d8e4024574bea737df68db278c6a71988ca7371cbc953`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 02:44:13 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 02:44:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:44:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:44:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:44:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:44:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:44:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:44:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:44:13 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:44:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:44:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:44:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:44:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb28ef838e56c6ab8cebd0401045d8e34acac54687290ae5630028b628a943b9`  
		Last Modified: Sun, 21 Dec 2025 02:50:38 GMT  
		Size: 148.4 MB (148351194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b78a2047404a81fad9c8ec2b142c689c29f3b8af0786088eb686d7b4fbf28ab`  
		Last Modified: Fri, 16 Jan 2026 02:44:28 GMT  
		Size: 2.4 MB (2374737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9139b37d5e678d21dc295f65b59b4df59b0e0fae30ecd21ffe1c4af0bcd45586`  
		Last Modified: Fri, 16 Jan 2026 02:44:21 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4bb78f3980449c781355f12ae99d62b32e893906771642776910d1dac571c`  
		Last Modified: Fri, 16 Jan 2026 02:44:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068146a8dffb6738e0de5e629e55933946de1d0ee1c0a1f9d953565a2e2b41d`  
		Last Modified: Fri, 16 Jan 2026 02:44:28 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:159f7fa41c5abbc7d8022df17df7e8090d1dd2b6cccdb2781b163a825f7fa43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5531fd83e67e78a9d325209ad3e7df095c7ad884eb460fc0eafe09592a144c1`

```dockerfile
```

-	Layers:
	-	`sha256:fbf1ff7664642f2f5e49eea8f2830b145008de29a2ce7c679087d566415a949d`  
		Last Modified: Fri, 16 Jan 2026 03:28:58 GMT  
		Size: 726.6 KB (726627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6290a6559f7f92969a80de5b4b1afa5b3f27da56a44d09e1a50aa349afe9563b`  
		Last Modified: Fri, 16 Jan 2026 03:28:59 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:592492cb38277819196e8f3114c3bf117171337db50aaedc8aab2c088e093f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162566644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c862452bf5edfc8b26f25b319de31c30aa511028968a51df7c5beb37199c45aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 17 Dec 2025 20:07:04 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 17 Dec 2025 20:07:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:07:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:07:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:07:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:07:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:07:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:07:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:07:04 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:07:04 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:07:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:07:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:07:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c010ce05bd9b6d74dd876e5f1bce365f86d6b710a28f124ed8d1ad6dcd32407`  
		Last Modified: Sat, 20 Dec 2025 23:35:40 GMT  
		Size: 146.7 MB (146709717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb172d6224b3ccf07efba001f166d2b7a178bfc735eef19ba4e2673fa6bcf3f2`  
		Last Modified: Wed, 17 Dec 2025 20:07:19 GMT  
		Size: 2.4 MB (2405579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c97129019aa90fe49866ec85a6e4cc2841940147c8e0e7180a80d4bf7326fa2`  
		Last Modified: Wed, 17 Dec 2025 20:07:20 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a901fb6972640aa3773ee0b05d741c09a463a6b80b6ddbc3d6c2d3c59360ed6d`  
		Last Modified: Wed, 17 Dec 2025 20:07:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b021daa91822ce7ceb439805038a944307c223dcde02330f58746c9d896d7`  
		Last Modified: Wed, 17 Dec 2025 20:07:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:72ce79bfa5fdc05973d4aeb0a4289aabf431afc93f3042063229db1e8032e11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 KB (742529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67e1a8506f0281091207c77da20dabbf2d89167bd9c60a94d16acb31b7be068`

```dockerfile
```

-	Layers:
	-	`sha256:f519f5f907f2d6ed40009299a0e8232953e225cbe0d650a5dfde142aa1c96fac`  
		Last Modified: Wed, 17 Dec 2025 21:28:46 GMT  
		Size: 726.0 KB (726034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb6379c8bf4d89debced57eb595440b44cfc91f52443884c567ed83bf1105fab`  
		Last Modified: Wed, 17 Dec 2025 21:28:47 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
