## `maven:eclipse-temurin`

```console
$ docker pull maven@sha256:26963f4e0cd5c4988bc31091399d87b7e8bdd2c18bf288547fce7bc9f3b75c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:eclipse-temurin` - linux; amd64

```console
$ docker pull maven@sha256:4581fb4f85bd864f798e43a209ad5a0667912945fbb868f65341cf296a7143c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281259781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f7c6487b33999400e496285443a0619549c0f03370c8def9342ef2b6759e90`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:07:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:07:37 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 05 Apr 2022 23:07:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:07:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:07:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 23:07:53 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 04:57:33 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:57:33 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 04:57:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 04:57:33 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 04:57:34 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 04:57:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 04:57:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 04:57:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 04:57:35 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 04:57:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 04:57:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 04:57:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc7fe67d3007d02e7d89c114454bce7134a61ae03f677ea88b6da10596ee38f`  
		Last Modified: Tue, 05 Apr 2022 23:11:07 GMT  
		Size: 19.8 MB (19771517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1472f44fb5616b69bbb14368cc32e86175698990ec3f89f4994e4111c94ef0`  
		Last Modified: Tue, 05 Apr 2022 23:11:48 GMT  
		Size: 193.0 MB (193011359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5eece4b1de2a688c01d6c542f7d31aa857a5661fd86c1870bb1a2bd7a34e8e`  
		Last Modified: Tue, 05 Apr 2022 23:11:34 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd66d85eefb45773fdfac7aee04c1f8a6d5f2fee08fa7582c731db78748e70f`  
		Last Modified: Wed, 06 Apr 2022 05:01:46 GMT  
		Size: 31.2 MB (31172872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3e1759e76b9c8f89715ac5c27ccd8e191336ece55379a524e16745eee3573f`  
		Last Modified: Wed, 06 Apr 2022 05:01:42 GMT  
		Size: 8.7 MB (8736366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd42e9ea7dd450b07209b41a9ddd8e44d93b56d4546ed713f220d4856a0072c6`  
		Last Modified: Wed, 06 Apr 2022 05:01:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f98edd2598d0c7056500be8e86124a132d8a59b0de46957692ca5295e5d084d`  
		Last Modified: Wed, 06 Apr 2022 05:01:41 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm variant v7

```console
$ docker pull maven@sha256:99d5925090a967c93e9a448450da2d75be8b30ca2283af2edf70964be6b05157
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269341689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e7d9a4d7d972a054b5f4a72081b3310ad37802006f03c0e5305772877f0779`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:06:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:07:43 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 06 Apr 2022 04:08:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:08:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:08:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 04:08:10 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 07:48:14 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 07:48:15 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 07:48:15 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 07:48:15 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 07:48:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 07:48:25 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 07:48:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 07:48:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 07:48:26 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 07:48:26 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 07:48:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 07:48:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7eacdd26b0e96742477eb590629e1cb2d76d02c416494f0a25b3916ba4e7f2`  
		Last Modified: Wed, 06 Apr 2022 04:15:51 GMT  
		Size: 19.2 MB (19193623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733f7bdaeda61835b59182c785edd518f5b87807da5ee28e85a7ed554fda47a6`  
		Last Modified: Wed, 06 Apr 2022 04:18:22 GMT  
		Size: 190.0 MB (190040322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e5d035b95e84c2d0715948ce72e606bca13eefdabbe3ef96539838c987f70`  
		Last Modified: Wed, 06 Apr 2022 04:17:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29b467568197568b6da175e0057422404d5b85061728bc6f7a37890b5b3b751`  
		Last Modified: Wed, 06 Apr 2022 07:52:07 GMT  
		Size: 27.3 MB (27296188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90011d9724474908080a0040f49e998d83f95c02559074480a53d4742709b590`  
		Last Modified: Wed, 06 Apr 2022 07:51:52 GMT  
		Size: 8.7 MB (8736390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802ba6200f6b721ae566137560a6602129d9fc3fedd399c9a185bad8af2a96fa`  
		Last Modified: Wed, 06 Apr 2022 07:51:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d1d94d3f02cfc485bdf0452508d423486d48da996a23cbdd1126a091b2f312`  
		Last Modified: Wed, 06 Apr 2022 07:51:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9951813bea799fe02f3029e0d187abb41423074043a15b00fe68474a0efe6518
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277316901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff4d5ea9432fcfde1751abc1448aede5bce29f8135c36935bafbee4733946ad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:21:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:22:05 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 05 Apr 2022 23:22:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:22:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 23:22:24 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 05:53:44 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:53:45 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 05:53:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 05:53:46 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 05:53:47 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 05:53:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 05:53:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 05:53:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 05:53:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 05:53:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 05:53:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbf60885516768e1cf4d85dfe4d2ef57124a0af5e3fc86767efa1ebeea112ed`  
		Last Modified: Tue, 05 Apr 2022 23:26:50 GMT  
		Size: 20.5 MB (20498028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbb36541a6e8efa67b0bd452475b563c5fc8474a1df77a04f67fc0820715072`  
		Last Modified: Tue, 05 Apr 2022 23:27:42 GMT  
		Size: 189.9 MB (189944713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7ea406feae4a979d12bd18d0630d20c411b0a67cd58113e84dea375014080f`  
		Last Modified: Tue, 05 Apr 2022 23:27:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2652ad24d62592f6a4771fed2a5524970bff8a8a136a13ec0622069cea791e`  
		Last Modified: Wed, 06 Apr 2022 05:59:31 GMT  
		Size: 31.0 MB (30967086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8f5cf214662118fff5a55374a12fb521b0ef45d8a6adeefaa749fc89b7699`  
		Last Modified: Wed, 06 Apr 2022 05:59:27 GMT  
		Size: 8.7 MB (8736337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfce614b73a6820302bc2b43eff812f627aec8c4236dde0d26c5a1453274ef9`  
		Last Modified: Wed, 06 Apr 2022 05:59:26 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbaaf52a0564ab49bbb28bda6426a13e63653b0baf71020b9d598d912cfd7da`  
		Last Modified: Wed, 06 Apr 2022 05:59:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; ppc64le

```console
$ docker pull maven@sha256:e31b0c9911ba085de482eace170f01c727228b5b9c30386d1ee896962690e8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292081624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4abc75089fb5b97d27dff49efe89918cb11d63bbe405bf41ddb7dab8fbefb22`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:53:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 05:01:20 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:03:00 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 06 Apr 2022 05:03:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 05:03:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:03:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 05:04:00 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 08:11:52 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 08:12:05 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 08:12:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 08:12:23 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 08:12:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 08:12:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 08:13:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 08:13:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 08:13:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 08:13:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 08:13:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 08:13:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb55998198cd447fabd7426b9b309f4fe1c7fdb07fc7b6e8098af187e5a9e1f`  
		Last Modified: Wed, 06 Apr 2022 05:10:25 GMT  
		Size: 21.7 MB (21690183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf580d44e5e5c06585c211d5b6a9392665eaa07afdb0b9cac60bc32d7a54579`  
		Last Modified: Wed, 06 Apr 2022 05:11:19 GMT  
		Size: 190.0 MB (189983500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817e47b42fb3e81560be59b8ebf60aca9cbfad2c33d564a1865aa4e1c69f9a88`  
		Last Modified: Wed, 06 Apr 2022 05:10:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f38a03334e1b4d2d0abb48f7755bcbabfdee2f5b63dc5438e48b02bab5b817`  
		Last Modified: Wed, 06 Apr 2022 08:31:41 GMT  
		Size: 38.4 MB (38378393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72a3ccb59f18b7810d41e67ca0c5effb1d111dc000748761798e3fb5778f90`  
		Last Modified: Wed, 06 Apr 2022 08:31:35 GMT  
		Size: 8.7 MB (8736364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abace54cdc1e8898bbf84e2c50918bdddbf00ad11d215336efd33658bb6c4b4c`  
		Last Modified: Wed, 06 Apr 2022 08:31:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cbc07d5b18d2968db13aa32d2574c4d5de91eae42849f15f6139d13f26f2d9`  
		Last Modified: Wed, 06 Apr 2022 08:31:34 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; s390x

```console
$ docker pull maven@sha256:5bd8dd0f9fd1e57e406df82e9e8f0c696f77c6653a6c31b08612cd74e8fb9a69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266174728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b805ca4dca14baa7abc7a55885c7e1106698b8b894231f4b17571538c8ad61`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:42:05 GMT
ADD file:44b5cfe67740a0d7e33d6aa2c83d9918fdb30a0649aa3471e2f668dec1ba7f3a in / 
# Tue, 05 Apr 2022 22:42:07 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:59:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:00:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:01:01 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 05 Apr 2022 23:01:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='302caf29f73481b2b914ba2b89705036010c65eb9bc8d7712b27d6e9bedf6200';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='544936145a4a9b1a316ed3708cd91b3960d5e8e87578bea73ef674ca3047158e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='532d831d6a977e821b7331ecf9ed995e5bbfe76f18a1b00ffa8dbb3a4e2887de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='383ac8ad392036bedab9a08eb55395b95593a6cc268c422a2bab53f0977a4c54';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='288f34e3ba8a4838605636485d0365ce23e57d5f2f68997ac4c2e4c01967cd48';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:01:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:01:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 23:01:17 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 00:11:13 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:11:15 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 00:11:15 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 00:11:16 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 00:11:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 00:11:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 00:11:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 00:11:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 00:11:24 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 00:11:24 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 00:11:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 00:11:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:502c7975d4ed549ab7d6e63b9ea10b0d24c1c3c12a33540d91d6739a0218faec`  
		Last Modified: Tue, 05 Apr 2022 13:17:47 GMT  
		Size: 27.1 MB (27084913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0e34cdc988538abf4cdb8842ac912ad4ebce5760f9a3f3b5407ed8fb65eddd`  
		Last Modified: Tue, 05 Apr 2022 23:03:02 GMT  
		Size: 19.2 MB (19234416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f2a6a03c8f9063225610d30452c924cec2273ba82857a3a27cdab25a02617e`  
		Last Modified: Tue, 05 Apr 2022 23:03:31 GMT  
		Size: 180.4 MB (180427211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8845540ab9ca4dede6140192a1cf40607147cfca02689808c66a646c4b331b7`  
		Last Modified: Tue, 05 Apr 2022 23:03:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bff1c8070fc1463d12700f32144391c419596eb17e5b1b46e4ecb73fd3ba24`  
		Last Modified: Wed, 06 Apr 2022 00:14:44 GMT  
		Size: 30.7 MB (30690452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b83f50a676289385aab661f1a622c677fbc78850c4d49fd4779b565c3f9e0b`  
		Last Modified: Wed, 06 Apr 2022 00:14:40 GMT  
		Size: 8.7 MB (8736365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffb386a55a1a03721e779f7f0c6351edd224d55bd95c45e2a48ddf77de61a10`  
		Last Modified: Wed, 06 Apr 2022 00:14:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d4588ff871143efe25d2b08f770691c27150c0156681eae18f473f8230f4`  
		Last Modified: Wed, 06 Apr 2022 00:14:40 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
