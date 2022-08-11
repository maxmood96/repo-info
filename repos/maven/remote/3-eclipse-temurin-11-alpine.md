## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:ce6d48ec630f197d6d47ffa9292c71c82f1ab8dbdcea54b78c592552abb9a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:9fae05116a9c9a0149f1c7ef19dd547d45214b4edb90877dde4eb665575977f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219133457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e79979edcdd9e28361bb85e8dbfd51c142cdacc3f5de30785a084283142790`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 19:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:19:40 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 11 Aug 2022 19:22:05 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 11 Aug 2022 19:22:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32a93bd824cf34ccdde0881699a41a12722b4d8ff1d57294b2add2102432759b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:22:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:22:21 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 21:11:56 GMT
RUN apk add --no-cache curl tar bash procps
# Thu, 11 Aug 2022 21:11:56 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 11 Aug 2022 21:11:56 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Aug 2022 21:11:56 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 11 Aug 2022 21:11:56 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 11 Aug 2022 21:11:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 11 Aug 2022 21:11:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Aug 2022 21:11:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Aug 2022 21:11:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 11 Aug 2022 21:11:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 11 Aug 2022 21:11:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Aug 2022 21:11:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107abfa4a9656cc98051eebaf02de090526191f4d53ab3733605b34f84513224`  
		Last Modified: Thu, 11 Aug 2022 19:29:52 GMT  
		Size: 12.1 MB (12050073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c470bb6c75a97511cd4a515fd90f0d7502e6717113972f191c1a4f5dc892d5`  
		Last Modified: Thu, 11 Aug 2022 19:32:30 GMT  
		Size: 193.5 MB (193453440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d6d5d99e5b9142e729582ebacd318dedcb54f270e2386f0a8c1c0a3194b28b`  
		Last Modified: Thu, 11 Aug 2022 19:32:16 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51b20e278aac02ccf72ea9b530c6d7c6094306b2b1556799b28f1175b901a2b`  
		Last Modified: Thu, 11 Aug 2022 21:15:47 GMT  
		Size: 2.1 MB (2083009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3d6fd570d5c02cae48b9c02aa7b0c54b2f8ab1bd0c5df4afea013b88893`  
		Last Modified: Thu, 11 Aug 2022 21:15:47 GMT  
		Size: 8.7 MB (8739495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35757c08d78186c22a196f85a8666d94395ddd824e79944a421ac8ddb9a47942`  
		Last Modified: Thu, 11 Aug 2022 21:15:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2490a8e568e3e74bac9b20710f6a818a78c0153ee526467455cfdc09cc36da8a`  
		Last Modified: Thu, 11 Aug 2022 21:15:46 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
