## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:e5fdba163319ce0eb2623bd3bc872a379a80656014c60bce9f4fcf46a85d88bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:ac5182bac645bf8a2c596807036a16799bf61b6fd820233f5cafb56cf03e9321
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220480006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c30bc9cda8122a04bfd4b600e3e4d802b9f39a80e37db93a56a07aa97453d21`
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
# Sat, 11 Feb 2023 05:24:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Sat, 11 Feb 2023 05:25:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='42722bdbee99ad1430d6e88f17608909f26b57ab7761fb6b87ff4dbf6a8928bc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:25:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 05:25:09 GMT
CMD ["jshell"]
# Thu, 16 Feb 2023 00:23:53 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:23:53 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:23:53 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:23:53 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:23:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:23:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:24:01 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && apk add --no-cache bash procps curl tar gnupg   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && apk del gnupg   && mvn --version
# Thu, 16 Feb 2023 00:24:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:24:01 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:24:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:24:01 GMT
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
	-	`sha256:6d03da69ccb08c4958a36e793b113c5b369bba00fe02fbd44813e7254955a3ae`  
		Last Modified: Sat, 11 Feb 2023 05:29:47 GMT  
		Size: 193.8 MB (193847503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464e02814e9be35e5bcf9cd2a3706b80431c3cb33e59f4f274b8a71b2c4021a0`  
		Last Modified: Sat, 11 Feb 2023 05:29:33 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d193a37223514aae18e84775065d9fbb611e9395a980a72c9c9ac94d8fa2e393`  
		Last Modified: Thu, 16 Feb 2023 00:33:18 GMT  
		Size: 11.2 MB (11236500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5501ee135160b0c081032b17e67295dd2557648ef0c7c90896191dfaa45e1c`  
		Last Modified: Thu, 16 Feb 2023 00:33:17 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbbb781ed7fb81d4a82c95bf9c65cd226b68ca403e5290c348a5f307979a71`  
		Last Modified: Thu, 16 Feb 2023 00:33:17 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
