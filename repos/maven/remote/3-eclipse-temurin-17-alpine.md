## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:19f96627b75c126f0b00b78e35be1c3960693169d44dbdd446ee44d05801eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:e88c1a981319789d0c00cd508af67a9c46524f177ecc66ca37c107d4c371d23b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217398009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eb1ff95822b90d8ce030e4c84841472273a6a6c144d6cebdcd3e8926dc1d6b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:12:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 12 Nov 2022 05:12:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:12:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 12 Nov 2022 05:12:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 12 Nov 2022 05:13:30 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Sat, 12 Nov 2022 05:13:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cb154396ff3bfb6a9082e3640c564643d31ecae1792fab0956149ed5258ad84b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:13:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 12 Nov 2022 05:13:51 GMT
CMD ["jshell"]
# Sat, 12 Nov 2022 10:21:43 GMT
RUN apk add --no-cache curl tar bash procps
# Sat, 12 Nov 2022 10:21:43 GMT
ARG MAVEN_VERSION=3.8.6
# Sat, 12 Nov 2022 10:21:43 GMT
ARG USER_HOME_DIR=/root
# Sat, 12 Nov 2022 10:21:44 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Sat, 12 Nov 2022 10:21:44 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Sat, 12 Nov 2022 10:21:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 12 Nov 2022 10:21:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 12 Nov 2022 10:21:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 12 Nov 2022 10:21:46 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 12 Nov 2022 10:21:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 12 Nov 2022 10:21:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 12 Nov 2022 10:21:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9822f87bb1185b1d8f81aa09fc8a20796bb3db4c90da28c6177e0fd8a3d8d3`  
		Last Modified: Sat, 12 Nov 2022 05:16:37 GMT  
		Size: 12.0 MB (12030631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dd5a4c9d9b66950c491bf46b0fa319e048043eee4d4f74a473b0f27cd70589`  
		Last Modified: Sat, 12 Nov 2022 05:18:22 GMT  
		Size: 191.7 MB (191737252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5b1b0a2ab2f3efa0b93fa43b3aa8d8ea84d62cf5dc6bd850464f5c14e2cef3`  
		Last Modified: Sat, 12 Nov 2022 05:18:07 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f04de8afabc2a277ac17b3bbd19d22eda77072c26a3dd28baacacbac5e0466`  
		Last Modified: Sat, 12 Nov 2022 10:24:11 GMT  
		Size: 2.1 MB (2082956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f664fe065d03e0dafbdca5e0c3205cff3de6c65e55c05c262de6d6a522dddb`  
		Last Modified: Sat, 12 Nov 2022 10:24:16 GMT  
		Size: 8.7 MB (8739507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cfd72b03912a4646b67532a114910445a31b20547a97fb6425d220a170bdab`  
		Last Modified: Sat, 12 Nov 2022 10:24:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e62530645c19dc223e66c7df318f22d2f02c1ec4164302a419c592a58ec51ae`  
		Last Modified: Sat, 12 Nov 2022 10:24:10 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
