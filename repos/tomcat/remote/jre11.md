## `tomcat:jre11`

```console
$ docker pull tomcat@sha256:e5b8c636ade4240f890ca3694de87cc744074e805c955d06d062f235f777fbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:jre11` - linux; amd64

```console
$ docker pull tomcat@sha256:dbcb6a876492db8619719d6491502779d70fc8300a2858901f7c3bfd7815576d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102174267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c666fc81f35518dd166b8fa1cbe5216906cf9781a72e27b7c12d6596e76a2e34`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:44:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:45:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:45:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 08:06:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 08:06:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 08:06:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 08:06:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 08:06:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 08:06:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 08:06:49 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 16 Mar 2023 08:06:49 GMT
ENV TOMCAT_MAJOR=10
# Thu, 16 Mar 2023 08:06:49 GMT
ENV TOMCAT_VERSION=10.1.7
# Thu, 16 Mar 2023 08:06:49 GMT
ENV TOMCAT_SHA512=41997f90baf86af6dc0396cbf66941f801e0ae9ad1b57475661d10e648c55559491e85468af2df3ee457be3fcae12b74537ce19a9a28e34030b98e8bb38dbd35
# Thu, 16 Mar 2023 08:06:49 GMT
COPY dir:c0d9179c38ba163740e9b193c6e6f38ffcf934bf8b039ceea25873e792c3f464 in /usr/local/tomcat 
# Thu, 16 Mar 2023 08:06:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 08:06:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 08:06:55 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 08:06:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cabe75b440d785eb2f20422368c248b28fd9c219a5d5db5aacb7de3d43f02c`  
		Last Modified: Thu, 16 Mar 2023 02:50:26 GMT  
		Size: 12.4 MB (12432056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3fc5460b4b76e852651fec42e4cde1337c4bf503657efbe5521f379b19748a`  
		Last Modified: Thu, 16 Mar 2023 02:52:30 GMT  
		Size: 46.6 MB (46635547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a8054900958099c4da9d407d5b7d023cf76df2b891f916546c0ddb7e26a697`  
		Last Modified: Thu, 16 Mar 2023 02:52:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28433e65ef6c711796f104c155386ec51d210e29e92ed4d7859db73e3c2cb719`  
		Last Modified: Thu, 16 Mar 2023 08:23:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47339eb3be463ddde1986266f048711df62bc92e2f708ad4037843f6d356da1`  
		Last Modified: Thu, 16 Mar 2023 08:23:14 GMT  
		Size: 12.2 MB (12222088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cf7844a68706036edbd599198bf24489a4869341897f3658bd55b836dcc571`  
		Last Modified: Thu, 16 Mar 2023 08:23:14 GMT  
		Size: 454.2 KB (454154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a625c405aa74eed1ab6fbd5b3d99f906bf3f321c6fcd814d548de053394476ae`  
		Last Modified: Thu, 16 Mar 2023 08:23:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:51395e9324d8707cef29b486132e2e0779fa2d9798486c658b7c6c53f4e55679
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96488404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200bec70b3a0cf1378d08be501607a1d9a8509a377426cc2eab735094c2791b0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:27 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:51:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 04:51:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:51:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 04:51:29 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 04:51:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 04:51:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 04:51:29 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 16 Mar 2023 04:51:29 GMT
ENV TOMCAT_MAJOR=10
# Thu, 16 Mar 2023 04:51:30 GMT
ENV TOMCAT_VERSION=10.1.7
# Thu, 16 Mar 2023 04:51:30 GMT
ENV TOMCAT_SHA512=41997f90baf86af6dc0396cbf66941f801e0ae9ad1b57475661d10e648c55559491e85468af2df3ee457be3fcae12b74537ce19a9a28e34030b98e8bb38dbd35
# Mon, 27 Mar 2023 22:34:18 GMT
COPY dir:ba4ae34ec844460b5c40b080b41753bae69c653c2dfdaf0bf41893a695aa0632 in /usr/local/tomcat 
# Mon, 27 Mar 2023 22:34:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 Mar 2023 22:34:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 Mar 2023 22:34:23 GMT
EXPOSE 8080
# Mon, 27 Mar 2023 22:34:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b83e8d8bd4412b60218836b5d4d212005df6c871a65bcb85878921aa8488f85`  
		Last Modified: Thu, 16 Mar 2023 02:53:35 GMT  
		Size: 12.0 MB (11993795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed608ed3f55006cc7e32db8cd1287a7eaf65b43b8ab758b360fe1715f51d0417`  
		Last Modified: Thu, 16 Mar 2023 02:55:43 GMT  
		Size: 44.8 MB (44842869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba3b2b8258fdd75034cbc115918adfdaf2ca84301e9234ba755da3724b45c3f`  
		Last Modified: Thu, 16 Mar 2023 02:55:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e091440ca618f3efb0b23dd066ee027634e1eb1137ff05008667165b3ae317ee`  
		Last Modified: Thu, 16 Mar 2023 05:13:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba910c8f1262687eb3289b88152e1c71ca34b0ca41f3a7f407c9dce121529d7e`  
		Last Modified: Mon, 27 Mar 2023 22:47:14 GMT  
		Size: 12.2 MB (12197546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb00e62941f184ea94dfb7f8d801d7e0626b09a5821956a605c8a531b9adfc30`  
		Last Modified: Mon, 27 Mar 2023 22:47:13 GMT  
		Size: 428.3 KB (428336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c6facf65783c67bd58633b8cf37cdf835f718d2dd9ef093be3084ce50ef4b7`  
		Last Modified: Mon, 27 Mar 2023 22:47:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3a27e0a9b04287b1f0c6e78e30232a40d6bbed7e2898670cbe637310380f988f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98432400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460fc0f448a741a52e36e7929f54691f699762b000cadbf0d5bf761d44bfce03`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:41 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:27:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 06:27:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:27:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 06:27:32 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 06:27:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 06:27:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 06:27:33 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 16 Mar 2023 06:27:33 GMT
ENV TOMCAT_MAJOR=10
# Thu, 16 Mar 2023 06:27:33 GMT
ENV TOMCAT_VERSION=10.1.7
# Thu, 16 Mar 2023 06:27:33 GMT
ENV TOMCAT_SHA512=41997f90baf86af6dc0396cbf66941f801e0ae9ad1b57475661d10e648c55559491e85468af2df3ee457be3fcae12b74537ce19a9a28e34030b98e8bb38dbd35
# Thu, 16 Mar 2023 06:27:33 GMT
COPY dir:ef4e88cd471e77cca77d60fca933f08641c5714272d0f6db068953a566921b6a in /usr/local/tomcat 
# Thu, 16 Mar 2023 06:27:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:27:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 06:27:38 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 06:27:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35794a35c4aa2299e9a7a69f4eafa7f96eb1832e2a04b3d85773522111018ca6`  
		Last Modified: Thu, 16 Mar 2023 01:58:19 GMT  
		Size: 12.4 MB (12389767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26126947450108b9349ce5c70904451e6ada86d51dde32223e9d9de1e567f89f`  
		Last Modified: Thu, 16 Mar 2023 02:00:06 GMT  
		Size: 45.0 MB (44977990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a873c16c3848ad12697e893cb753bb353c55c7d09fbbcdb67983aafbbd885b`  
		Last Modified: Thu, 16 Mar 2023 02:00:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c171da1e14cae24bb7b0a542326df4c310966690ef3395e8a77f7387a3638df0`  
		Last Modified: Thu, 16 Mar 2023 06:42:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c89ea27adb5688d70074e4e7ccbf9450bb52b646f4da160c2819c52e4d9d0`  
		Last Modified: Thu, 16 Mar 2023 06:42:15 GMT  
		Size: 12.2 MB (12223376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc62ad0a3b26aff2122d8fed46fbafb9299c49d56d9ac637ff9b69e0ca9f8450`  
		Last Modified: Thu, 16 Mar 2023 06:42:14 GMT  
		Size: 453.3 KB (453254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a127f3b1d4755016301fa211be3a92575a1439365514fbcda56c683fb336d7e3`  
		Last Modified: Thu, 16 Mar 2023 06:42:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3e65b19c3e1977e6faa6b76c48db3f31b34f400808edeec801d27555047b8fd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103742906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8452b96fec00916b7ebac84a2218423523b0e83a8e7ad40c4911fe9c484e1d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 03:58:08 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:00:07 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 04:01:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:01:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 09:24:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 09:24:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 09:24:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 09:24:36 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 09:24:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 09:24:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 09:24:37 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 16 Mar 2023 09:24:37 GMT
ENV TOMCAT_MAJOR=10
# Thu, 16 Mar 2023 09:24:38 GMT
ENV TOMCAT_VERSION=10.1.7
# Thu, 16 Mar 2023 09:24:38 GMT
ENV TOMCAT_SHA512=41997f90baf86af6dc0396cbf66941f801e0ae9ad1b57475661d10e648c55559491e85468af2df3ee457be3fcae12b74537ce19a9a28e34030b98e8bb38dbd35
# Thu, 16 Mar 2023 09:24:39 GMT
COPY dir:db351f4d4618cf97636631ce373b522d2236ff932707a379586899ef84f1d7ed in /usr/local/tomcat 
# Thu, 16 Mar 2023 09:24:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 09:24:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 09:24:53 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 09:24:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768433d99449ed12b4278d9faff20cb5980bb6dfe32e7041786360e04de407a8`  
		Last Modified: Thu, 16 Mar 2023 04:10:24 GMT  
		Size: 13.2 MB (13246071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b2ea203970ddc2b645bc9386cb02af22d03c206a2bdb326f1fabfb13cbc017`  
		Last Modified: Thu, 16 Mar 2023 04:13:12 GMT  
		Size: 42.1 MB (42062798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5598ed127b7ac92688ecd7841152854d4fbada9c9599be723d8913243cd098f2`  
		Last Modified: Thu, 16 Mar 2023 04:13:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee899d87f8699095b6eb900c167f20754ac982ad58a4800697c0b4d66872a50`  
		Last Modified: Thu, 16 Mar 2023 10:01:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fa5e3af74ceccd7604499611a9b3159542bd444b1d9365b865630f1a7665f1`  
		Last Modified: Thu, 16 Mar 2023 10:01:08 GMT  
		Size: 12.2 MB (12236344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbea80fc626399c42515d4d620af01bd9944b510df851307904dacdea7b5505`  
		Last Modified: Thu, 16 Mar 2023 10:01:07 GMT  
		Size: 485.5 KB (485504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f5f64ec3850b8d25af5be3788deb9573231e2ae27abbd8dc4567b3aa6e207`  
		Last Modified: Thu, 16 Mar 2023 10:01:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11` - linux; s390x

```console
$ docker pull tomcat@sha256:cd83b5e68546721b797eccc6dd880ad9b9c2f4188acdbd827ed575a80a09653a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94345582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f95152a1790e603d8b1786fb236bfca6784a7d334435bca9ef111066ccb2a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:06:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:06:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:07:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:07:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 18:48:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 16 Mar 2023 18:48:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 18:48:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 16 Mar 2023 18:48:08 GMT
WORKDIR /usr/local/tomcat
# Thu, 16 Mar 2023 18:48:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 18:48:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 16 Mar 2023 18:48:08 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 16 Mar 2023 18:48:09 GMT
ENV TOMCAT_MAJOR=10
# Thu, 16 Mar 2023 18:48:09 GMT
ENV TOMCAT_VERSION=10.1.7
# Thu, 16 Mar 2023 18:48:09 GMT
ENV TOMCAT_SHA512=41997f90baf86af6dc0396cbf66941f801e0ae9ad1b57475661d10e648c55559491e85468af2df3ee457be3fcae12b74537ce19a9a28e34030b98e8bb38dbd35
# Thu, 16 Mar 2023 18:48:09 GMT
COPY dir:80d4187f028523422978811ed47fc0c98e614feb1eb5b6599a229c4b91b67611 in /usr/local/tomcat 
# Thu, 16 Mar 2023 18:48:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 18:48:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 16 Mar 2023 18:48:14 GMT
EXPOSE 8080
# Thu, 16 Mar 2023 18:48:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca8e6a758f1e7f20fc71ee8d9721f9f05f92db0f3b311442735ae54dcc2f50`  
		Last Modified: Thu, 16 Mar 2023 02:12:17 GMT  
		Size: 12.5 MB (12480726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c30b8fd9b81f1a0978a226d50571c20b0db4295b7d14ffce2ca9e3286e36bfb`  
		Last Modified: Thu, 16 Mar 2023 02:13:01 GMT  
		Size: 40.5 MB (40535255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af32d4496558ffd79e4bd85656929843f99e8f020f1bea4a584fc53b1cc11a4`  
		Last Modified: Thu, 16 Mar 2023 02:12:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9bf368479127f5c3ca6529593b9ca7bed092eba334b38f8c9c346d04635970`  
		Last Modified: Thu, 16 Mar 2023 19:01:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637a5548d1156b2ceb4dcadf82a7898636dd2c5bf05212032c04b9ec5ff575b`  
		Last Modified: Thu, 16 Mar 2023 19:01:31 GMT  
		Size: 12.2 MB (12225850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a37ce45400f8abe58938b7c8314515cf5436b05ad76c8f7a8c97dd177c226`  
		Last Modified: Thu, 16 Mar 2023 19:01:30 GMT  
		Size: 455.7 KB (455693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e638215a1791410bc1a9b8e2f26af7e199a44a94664300d893dd023498bf1a8`  
		Last Modified: Thu, 16 Mar 2023 19:01:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
