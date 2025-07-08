## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:80a9389f0cc2df50e94954dfd87a79d1284a90bfdcdf7015f7e5019fa723ae67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:a73779c645efe653f31ca15945ec08e122315cbeca703946864a2e6555e19287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112888426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8382190cba1e94e35c603e95c519c6bb19845e9572e0b3ab3d4f762480e7eab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc97a198351fe5e4eca17b3f6dcb7e035abe8efa02b3c465b40153d75d5ed5`  
		Last Modified: Mon, 07 Jul 2025 21:04:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd770d9f8cb382e58242b850690e4c82bef833fe24869125b50005e09bee11`  
		Last Modified: Mon, 07 Jul 2025 21:05:00 GMT  
		Size: 14.1 MB (14082832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336b915669f79b3b27fbf8ccf1ac5fb5f04e0b9dc33aa2d572328546cb6c34d`  
		Last Modified: Mon, 07 Jul 2025 21:04:59 GMT  
		Size: 229.6 KB (229641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:14e9517607a1569183557504bb7db8f6788ebd1de166d6413a93aa5bb811f17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f323dbfef22f79b5ae645524c7715ad1da9b13aada0d35eb5ba5aa7a5fddca3`

```dockerfile
```

-	Layers:
	-	`sha256:123c1c8912863a2a0b16096b955665595263c08e0e356f4cb0763d3009a3087a`  
		Last Modified: Mon, 07 Jul 2025 23:32:42 GMT  
		Size: 3.9 MB (3944187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e451220482e8627dd45491adedc6ecb643d8147802a59e081ada34d74f2c1e6b`  
		Last Modified: Mon, 07 Jul 2025 23:32:43 GMT  
		Size: 21.6 KB (21580 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8e184f58f17a08f645236469dc8fed7a5956aba88caae895e02a399018574858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109805311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce52c67e7e422712d5c8751df3058dd173f83612820284e03c6a3f2d187d0873`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2273a973d4e42d06005c749d14c759efa1654bafb23852f9f2fcb8a66bff55`  
		Last Modified: Wed, 02 Jul 2025 14:33:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74beed947c5a6ecccda920d8d678dd40d9b95e79364374698158f8b3540b56f`  
		Last Modified: Tue, 08 Jul 2025 05:21:29 GMT  
		Size: 14.1 MB (14084090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5672ad2df0ff8d2ae87c1da5b601680399f0659b1c442328d721ef1401ce5e59`  
		Last Modified: Tue, 08 Jul 2025 05:21:28 GMT  
		Size: 228.7 KB (228698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:fa584489c50e88d8a30b4132cf74f319959df13e0b70e8aa1dda640bcac8cbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce94cfadf5ca6da0b469b388216d7007502e8de1970600bb394d375ab951f4d`

```dockerfile
```

-	Layers:
	-	`sha256:1829ae21c2cd5d24374207575eac9fe7f658c60ae20f9fab40b0cd7e24b9d91b`  
		Last Modified: Tue, 08 Jul 2025 08:31:30 GMT  
		Size: 3.9 MB (3943868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79543485006717fbc6710719a8d0c0951ca993fb57fcc126d53ccc43fe93461`  
		Last Modified: Tue, 08 Jul 2025 08:31:31 GMT  
		Size: 21.7 KB (21740 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:afe2a0f0c1e29ba6c84c818dd86a83773267ebfbbe30d3f0bad6420950e3e6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119334462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba8997c4483aa4f4ec7b5f9a6b9e013c1395c187b523cbf4aaa194a6f4ec54a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595b1fb797135dd0e29ee3176dc6a26da5fdd960326b5800ab21ad59036a273`  
		Last Modified: Wed, 02 Jul 2025 03:15:14 GMT  
		Size: 17.6 MB (17618409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a568e99dcd14f5fdbe5484f8399d1366fea06ae5e7a31b5388df7ebf7e4231a4`  
		Last Modified: Wed, 02 Jul 2025 03:27:43 GMT  
		Size: 52.9 MB (52915207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b9cf95a8a420c468ac1d4d15756ed31d35584c0ad3d3a6e2997f338a6cfe7`  
		Last Modified: Wed, 02 Jul 2025 03:27:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab66cc17c116efe193a483edf8294c3307c2f35b2351468f826163a9ccac35`  
		Last Modified: Wed, 02 Jul 2025 03:27:40 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db95a539f348070f6f12ed459da8f53dd5d407545c03920f430840be61f8914`  
		Last Modified: Wed, 02 Jul 2025 14:52:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38030252c3ae64998092726cbd95516400755e6c539076165de5161e56ad5286`  
		Last Modified: Tue, 08 Jul 2025 00:13:55 GMT  
		Size: 14.1 MB (14096499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd334abc5c624254a7d664adbfe6ed575e212a80a04ea34843df336a2a5448ed`  
		Last Modified: Tue, 08 Jul 2025 00:13:54 GMT  
		Size: 259.1 KB (259082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:72afdcdf4d26d3b6af7b63748332c4fa5469704d823b659914005723357ab782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72ff978e8192d8040a9ef7e6082465b743d5ace3a2ac92c1754a9bccd38d1d3`

```dockerfile
```

-	Layers:
	-	`sha256:fae9d8c2a7a4628141211590974f491a5b4358bc8713a68de7adf563addde27f`  
		Last Modified: Tue, 08 Jul 2025 02:30:53 GMT  
		Size: 3.9 MB (3948281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc40ee4d20d04cdf26c40e9a4504658c30ca58bb3f54124e2e4e810d26455390`  
		Last Modified: Tue, 08 Jul 2025 02:30:54 GMT  
		Size: 21.6 KB (21638 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:2d404d0dab3e278204e55e52207435d189fec70a35e855a2e54b2fa9b0f0625a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107934948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8697fb5afa282265ced90d3a19dd7a72118fb616f8dabeef5b8264eeb03f8d82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7407b9fdf832fa4e3a41a2319aa3e0d04f31104a25092c677a83bf06472d7`  
		Last Modified: Wed, 02 Jul 2025 04:15:41 GMT  
		Size: 16.1 MB (16144420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0641526ca479ff8922ad5bb33e682cf379c06900f1375d2a8f15b6958a3df`  
		Last Modified: Wed, 02 Jul 2025 04:22:46 GMT  
		Size: 49.5 MB (49471380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41f5a0ae728a429882ab5c991332a394333439b2648d8d5fb9d3fea9bce51e2`  
		Last Modified: Wed, 02 Jul 2025 04:22:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799b5d2340bd756931737c1e9fa84980897b60cc402baf68dd5ca263542fca05`  
		Last Modified: Wed, 02 Jul 2025 04:22:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22f39e8f135a87e01b76fbfb9a01f3039332ff4bbe039d72ce83028db284414`  
		Last Modified: Wed, 02 Jul 2025 07:20:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e524a9d966a1771843409e153e4bb3af0e3ba5333fd4a17b613e9194c5a884`  
		Last Modified: Tue, 08 Jul 2025 05:23:33 GMT  
		Size: 14.1 MB (14083491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584984d7404fc2cca5cc761ec64b027605e3fe9a9b75af4df29670c8a8f4be5`  
		Last Modified: Tue, 08 Jul 2025 05:23:26 GMT  
		Size: 230.8 KB (230840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3d6e3b56b9c2b55569c174540f22797719b5f6491493fdf72136eeefb5afe2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33032ea720033d46be38f66d52e7eb508d18ed2d7dd83af2b2faaf9367bc1c6`

```dockerfile
```

-	Layers:
	-	`sha256:0ff89bb700c999b6050d69ff997162c86d3662707b39066c70603b0b9ee50b29`  
		Last Modified: Tue, 08 Jul 2025 08:31:39 GMT  
		Size: 3.9 MB (3945778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0a054082451d7c932dddec34d6783c6c21608f23a1d8c5a12058056d64c740`  
		Last Modified: Tue, 08 Jul 2025 08:31:39 GMT  
		Size: 21.6 KB (21579 bytes)  
		MIME: application/vnd.in-toto+json
