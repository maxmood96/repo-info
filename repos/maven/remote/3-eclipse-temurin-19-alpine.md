## `maven:3-eclipse-temurin-19-alpine`

```console
$ docker pull maven@sha256:805fd2873fce63c3ba6ceb52d2597b1ef2f6aab60738d44791ec2c7fe7ece7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-19-alpine` - linux; amd64

```console
$ docker pull maven@sha256:72e002a270bd45b36e608fe66c7d54ff6bda47d573c8e08aa1b5a49a4bf9b505
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226941239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb744ead0301336193c88418e638b951b8eb57b4b036104758051fcd771eb80`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Feb 2023 05:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:24:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 11 Feb 2023 05:24:09 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 05:26:26 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Sat, 11 Feb 2023 05:26:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2d971400ad2db25ad43ea6fa2058b269c0236e3977986dcdee2097da301beb2';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:26:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 05:26:51 GMT
CMD ["jshell"]
# Thu, 16 Feb 2023 00:25:49 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:25:49 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:25:49 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:25:49 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:25:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:25:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:25:57 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && apk add --no-cache bash procps curl tar gnupg   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && apk del gnupg   && mvn --version
# Thu, 16 Feb 2023 00:25:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:25:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:25:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:25:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55337210c571172bc884a7dfb6dc597adab6b6ef741c06ca3200884ffc4b2b`  
		Last Modified: Sat, 11 Feb 2023 05:28:55 GMT  
		Size: 12.0 MB (12020168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179e78b7ac3beb399f002d9c566af29327c2fd2ac6956665f64f53aecf8d1119`  
		Last Modified: Sat, 11 Feb 2023 05:31:21 GMT  
		Size: 200.3 MB (200308729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ece7618d1e8c49aa5ff521f5133d9ab5bd61543cfe7493b40e99d10a2ec5d6`  
		Last Modified: Sat, 11 Feb 2023 05:31:05 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5714a9632ceb5fe0af961df6764e1e00348c675fb0675932b0e598957f99853b`  
		Last Modified: Thu, 16 Feb 2023 00:35:12 GMT  
		Size: 11.2 MB (11236507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140ff26b469457c4528cb170c1e20a3691c4b05a7417fbe7d9a69cd2ae42c485`  
		Last Modified: Thu, 16 Feb 2023 00:35:11 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c136b9e1717c2c7cd22076a48836305ced83603823847a7e59186f386bfe6d7`  
		Last Modified: Thu, 16 Feb 2023 00:35:11 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
