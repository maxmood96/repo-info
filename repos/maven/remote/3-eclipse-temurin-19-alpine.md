## `maven:3-eclipse-temurin-19-alpine`

```console
$ docker pull maven@sha256:47157deb2309605147103e036b5f44ad907422f1506a3e16d630d22abc2d1f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-19-alpine` - linux; amd64

```console
$ docker pull maven@sha256:f4c8a5004a6b06baca1ec03a511edefec8c433cc6449cbb869df1913ba686dd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225964302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bacd934265a402aa8c29c65fa07acbebdccb28a52f1a7f0f9dad7987d9a6c9e`
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
# Sat, 12 Nov 2022 05:14:15 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Sat, 12 Nov 2022 05:14:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76cfcdf47cdf24331b51939fd2840fd387cf62471da99e4718e2e42b486a9270';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:14:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 12 Nov 2022 05:14:38 GMT
CMD ["jshell"]
# Sat, 12 Nov 2022 10:21:54 GMT
RUN apk add --no-cache curl tar bash procps
# Sat, 12 Nov 2022 10:21:54 GMT
ARG MAVEN_VERSION=3.8.6
# Sat, 12 Nov 2022 10:21:54 GMT
ARG USER_HOME_DIR=/root
# Sat, 12 Nov 2022 10:21:54 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Sat, 12 Nov 2022 10:21:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Sat, 12 Nov 2022 10:21:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 12 Nov 2022 10:21:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 12 Nov 2022 10:21:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 12 Nov 2022 10:21:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 12 Nov 2022 10:21:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 12 Nov 2022 10:21:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 12 Nov 2022 10:21:57 GMT
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
	-	`sha256:f334dab74d0be632884d565506362427e88b3b8eda99949b482e665eb16228db`  
		Last Modified: Sat, 12 Nov 2022 05:19:12 GMT  
		Size: 200.3 MB (200303572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8636564591f925d6b7ffa028b7dfbfbf6a7350dc9a5aeb52d0597856e2c40a0`  
		Last Modified: Sat, 12 Nov 2022 05:18:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f80cba4fb02c4f0fecd611ed1f066f53a8e911506ed61ce13b0ced0c92992`  
		Last Modified: Sat, 12 Nov 2022 10:24:31 GMT  
		Size: 2.1 MB (2082951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99c5b8a5782a1b0064da84de10f93c248cf053ab10286817dc737cd020bc7b3`  
		Last Modified: Sat, 12 Nov 2022 10:24:30 GMT  
		Size: 8.7 MB (8739491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90965283138cc066d49945b73b4e7ee5fbc3d1938494910b60b61afe43706781`  
		Last Modified: Sat, 12 Nov 2022 10:24:30 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed081b77614521144a6fffd584e063b31f733812e6ff04b4e85aece30c6d2e7`  
		Last Modified: Sat, 12 Nov 2022 10:24:30 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
