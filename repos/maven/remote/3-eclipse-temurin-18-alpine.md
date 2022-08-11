## `maven:3-eclipse-temurin-18-alpine`

```console
$ docker pull maven@sha256:baafd1c7906fcab5dae1f43949cadf337a4b576b5a182e066c271d6bdcc96e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-18-alpine` - linux; amd64

```console
$ docker pull maven@sha256:b1642009de1e71691ca7c12c30157cdca056495ef0ab6bd99450a14551849b9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218577592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf7b150256b7db580dbff7bc126aa5309920e0365e54f85fff55b2639bec932`
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
# Thu, 11 Aug 2022 19:26:26 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:26:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:26:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:26:48 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 21:13:19 GMT
RUN apk add --no-cache curl tar bash procps
# Thu, 11 Aug 2022 21:13:19 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 11 Aug 2022 21:13:19 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Aug 2022 21:13:19 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 11 Aug 2022 21:13:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 11 Aug 2022 21:13:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 11 Aug 2022 21:13:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Aug 2022 21:13:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Aug 2022 21:13:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 11 Aug 2022 21:13:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 11 Aug 2022 21:13:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Aug 2022 21:13:21 GMT
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
	-	`sha256:e679a78d83de61b5d0ed95e8ee0bdd2eaa0d7f7c320f381f9c5f66b63a3715f5`  
		Last Modified: Thu, 11 Aug 2022 19:38:17 GMT  
		Size: 192.9 MB (192897589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0855aa0b135a5077a832ca2d50c73d5ea07687225d09966878018473d37aa`  
		Last Modified: Thu, 11 Aug 2022 19:38:03 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabf0640a1bc38c977aa886baa04635ace7fdd1ffb1837441217e35d26d365db`  
		Last Modified: Thu, 11 Aug 2022 21:16:19 GMT  
		Size: 2.1 MB (2083008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db2c3b37814b99dbfb510dd7eb1e968dc0c30b246517efc19edea4388a0db0`  
		Last Modified: Thu, 11 Aug 2022 21:16:19 GMT  
		Size: 8.7 MB (8739481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b360323f5ac777c36e761cdb5b09432b41df3983287efc0fbc46b0c10ad5c5`  
		Last Modified: Thu, 11 Aug 2022 21:16:18 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c028f1adbc7e9d2f86718deeb6a92f55df446e4e3c4d7cb84d34bfb09959f`  
		Last Modified: Thu, 11 Aug 2022 21:16:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
