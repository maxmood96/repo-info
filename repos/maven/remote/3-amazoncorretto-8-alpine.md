## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:325f952bded44981324e162b39f27ef00fa96a57b8d1701a68d0133ef9711915
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4729c3b174953a5eeaa2bd2c755a17cfad65cf31c33bdb4a9ab408811c126a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116235688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e33b5595534990a94eac4b04487ba2c210fff9028ff9ef08e23386ae6e13ec`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 02:47:01 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 02:47:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:47:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:47:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:47:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:47:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:47:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:47:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:47:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:47:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:47:01 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:47:01 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:47:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:47:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:47:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92574770f6746e0040e247649931c248a47ee8d6ac55cf021609a6a99672a25`  
		Last Modified: Tue, 21 Oct 2025 23:26:15 GMT  
		Size: 100.8 MB (100757885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c6936f18d1278b560125a44eab6cbbbee56921e9ce3a6a5a4b14f7f4fa69d`  
		Last Modified: Fri, 16 Jan 2026 02:47:15 GMT  
		Size: 2.4 MB (2362076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91ebbba4cfb439164b93f428d6c46f4febcbc718f97e9430903afab984b5299`  
		Last Modified: Fri, 16 Jan 2026 02:47:09 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbb347838ea512ecff3aa4532865ee54b591cfa2d6309c670ede7166380170`  
		Last Modified: Fri, 16 Jan 2026 02:47:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a149a191299fcdbcba7192263f7842f20b9f93b76efb335a1208e8a7601131e6`  
		Last Modified: Fri, 16 Jan 2026 02:47:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:17fcb89049e4f34c1c38d6b16f5fa9fcafcd66f579035a2a35200af91de1b61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 KB (407520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456a07dc38bb6842ef8e1e6b5495a91c97f2aa32edfa285c3699069a6896a34`

```dockerfile
```

-	Layers:
	-	`sha256:6fcc274ff57498bccef2fbd3e822e47c3a4dc07e986c2d46a89686e3c8157163`  
		Last Modified: Fri, 16 Jan 2026 02:47:09 GMT  
		Size: 391.2 KB (391167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8947870e59c50450cd41926c16defe0fe09cf11ca42fa68fc56be2dc5f82c2`  
		Last Modified: Fri, 16 Jan 2026 02:47:09 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c05c97c1465e8a5d93ed3bc7f419343c4268dd6f6f9e67f645474c8cbad2327a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116377795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e16ab73c8e279e9bcc5b031ea20fb48914a2ad0e164f530f651c4d1894312`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 03:33:25 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 03:33:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:33:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:33:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:33:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:33:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:33:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:33:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:33:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:33:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:33:25 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:33:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:33:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:33:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:33:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2744539f18ab260f7f42fe25f3c1d2ed1c04d685e18106e294c21f0dc1975c3f`  
		Last Modified: Tue, 21 Oct 2025 21:49:01 GMT  
		Size: 100.5 MB (100533297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59c2c383026dc88b19e9ecfc26cef63eba96895e5a1cb8ec526f42ee161bd0c`  
		Last Modified: Fri, 16 Jan 2026 03:33:33 GMT  
		Size: 2.4 MB (2393147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45dd7444cd5a39ae4d746e8c46efa6aad15040ccd91f27e3999133f2520d5eb`  
		Last Modified: Fri, 16 Jan 2026 03:33:38 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fcedf2d8a7eaa517932464cb76a90fdfd2be132ae76864e691d75a9333e99b`  
		Last Modified: Fri, 16 Jan 2026 03:33:37 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb092a28b043696dabf36a68336b05d5e0c6fa0f76708838d65f6ea8bc4689c`  
		Last Modified: Fri, 16 Jan 2026 03:33:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7f44acb33d709aaebd2623191b05df48b6b9bf50742ffd5f99fb658f9726d9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 KB (407773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640f0fcda52f02ab3c2dfd2fb63543ad06c98c8c83aada29e13abf405c06b9e3`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c3d9b49027ffd53ff76080d2e36c901f828d5bece6bff9bf654d1d56f562d`  
		Last Modified: Fri, 16 Jan 2026 06:29:16 GMT  
		Size: 391.3 KB (391287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299f78af6b4ae54e97652a9709b33d523a0ee94c72029ce37d87bf525f25f5d3`  
		Last Modified: Fri, 16 Jan 2026 06:29:16 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
