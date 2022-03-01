## `tomcat:10-jre17-temurin`

```console
$ docker pull tomcat@sha256:63ac63a00128e3b5552c020e345cecfac6c4874ca45c8805b70fa220695d6469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:680c982c568a876a6b5f814bc20b4f0d3860c215c2487716b50547a3ec6b38fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117185177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bc6f4bf4624e694bab02c153ff9ff615c889305e516b013f1cf54306a1411c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:59:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:15 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 03:00:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 03:00:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 03:00:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 14:10:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 14:10:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 14:10:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 14:10:49 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 14:10:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:10:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:10:49 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 14:10:49 GMT
ENV TOMCAT_MAJOR=10
# Tue, 01 Mar 2022 03:59:27 GMT
ENV TOMCAT_VERSION=10.0.17
# Tue, 01 Mar 2022 03:59:27 GMT
ENV TOMCAT_SHA512=c9a8894ddedb9a4966abb8698a029c00dda2603acb798bbf11a99cf585c2e5db967bee006689ea148b819fa11d1d8fe1e799ceb09243e70b1310ca18ada1f17f
# Tue, 01 Mar 2022 03:59:27 GMT
COPY dir:286e69ac5b68294aae6ecafd81fa8fb17f93971c9659faff9361632673a67086 in /usr/local/tomcat 
# Tue, 01 Mar 2022 03:59:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:59:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 03:59:33 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 03:59:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2670b5a474c24f63b09c71ff7444033a3440b5ad3d67eb1aca9e315ff31cab`  
		Last Modified: Wed, 02 Feb 2022 03:03:28 GMT  
		Size: 28.6 MB (28562645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e611274c024d487db529c6ddfa66754cf85a719f4ccdfed0d79be7d3190635`  
		Last Modified: Wed, 02 Feb 2022 03:04:30 GMT  
		Size: 47.0 MB (47038135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0759d1e7778de250f85491cc1d3ecb35d7da1b1a9b30b92fb7a67bdc92c45b`  
		Last Modified: Wed, 02 Feb 2022 03:04:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7597025425468d470ad7cdf7a5b036c4addf0ca3f917fd4afb1c6ddacef50c6`  
		Last Modified: Wed, 02 Feb 2022 14:51:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fafe4cfe21ba4112cc2c45f3568fb0eb37f4537ea33c7ac8e892862c394b3c`  
		Last Modified: Tue, 01 Mar 2022 05:03:04 GMT  
		Size: 12.6 MB (12564991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fea031938bc0d8298d2c907b009b2c1b9afb0527395442d541182cac1ff09b`  
		Last Modified: Tue, 01 Mar 2022 05:03:03 GMT  
		Size: 454.8 KB (454848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fc071a8a1fc969108acf872b8a8c9ed568e159a91b788dfc67d2754895dc2f`  
		Last Modified: Tue, 01 Mar 2022 05:03:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:33524f794c607b2bc5e5ec7eb8aa2f66d8475a46997f110610f82b5ba3f830a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108989454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd081b9a80d199322fc0a9f20f26eb3df613b12e0d1fed5abaf0d08a18794376`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:50:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:51:08 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 02:52:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:52:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:52:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:47:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 05:47:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:47:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 05:47:45 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 05:47:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 05:47:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 05:47:47 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 05:47:47 GMT
ENV TOMCAT_MAJOR=10
# Tue, 01 Mar 2022 05:28:51 GMT
ENV TOMCAT_VERSION=10.0.17
# Tue, 01 Mar 2022 05:28:52 GMT
ENV TOMCAT_SHA512=c9a8894ddedb9a4966abb8698a029c00dda2603acb798bbf11a99cf585c2e5db967bee006689ea148b819fa11d1d8fe1e799ceb09243e70b1310ca18ada1f17f
# Tue, 01 Mar 2022 05:28:54 GMT
COPY dir:c8bb7fb7f52a05211e715c34a67ff143f2eaaa6a2a0f15c4327178c0102a8f20 in /usr/local/tomcat 
# Tue, 01 Mar 2022 05:29:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:29:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 05:29:09 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 05:29:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c0154b8e60d06ef2e654b6fc885e6b2f15bdad4767412580dc35e38d769ec3`  
		Last Modified: Wed, 02 Feb 2022 02:56:28 GMT  
		Size: 27.4 MB (27368116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff007141150849b952660ce9278a8a846e72acb7a1a921e80f8e636e2f227724`  
		Last Modified: Wed, 02 Feb 2022 02:59:34 GMT  
		Size: 44.6 MB (44611502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ea4f82163adfaa156777ff287d052e29bef4e855060f0ccccf1e6d6e47dea2`  
		Last Modified: Wed, 02 Feb 2022 02:59:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5893b55c282cbfa45c796ecfe25e05c68f76da426cc92541898b491047ff589`  
		Last Modified: Wed, 02 Feb 2022 06:27:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab179b48884700524801abc048a7fd7f9999ed7727647dfcd9959940e3739a0`  
		Last Modified: Tue, 01 Mar 2022 06:08:49 GMT  
		Size: 12.5 MB (12515339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a05caf182405704cdb9a9d4725d367bcf6b711e9655424f910aa8c9311462ab`  
		Last Modified: Tue, 01 Mar 2022 06:08:45 GMT  
		Size: 431.3 KB (431285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af27266814af2d822b8d8789cacc229feced844d3f3bbeb9ec1a707596a1ad6`  
		Last Modified: Tue, 01 Mar 2022 06:08:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:69c6780fed67f1824b790dcdbcd46a4e46986b6d16c67791d2a090847d29aa5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114842551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6860f80630151a775cd462d99324b168bc4064f6a894fad595585e6a221dfd2f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 05:04:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:04:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:04:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 07:26:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 07:26:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 07:26:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 07:27:00 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 07:27:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:27:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:27:03 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 07:27:04 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 07:32:25 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 07:32:25 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 07:32:27 GMT
COPY dir:78d79d58788274fe0b2fe2ab38e7d48e2ae96896bd9d8b11d2accc80ff5ab6f6 in /usr/local/tomcat 
# Wed, 02 Feb 2022 07:32:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 07:32:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 07:32:36 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 07:32:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30d06458f35ec294f2441fb9f45188c88e217201cc30e2baee1a00f165107e`  
		Last Modified: Wed, 02 Feb 2022 05:08:05 GMT  
		Size: 29.4 MB (29377028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc72d389931c7b928c60a7b2b2691027da87695493e75cf58643f307fa4541d8`  
		Last Modified: Wed, 02 Feb 2022 05:09:19 GMT  
		Size: 45.5 MB (45484455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438d76301c760d1eb30210325dfc70548af077610fa49a0806b7060aa631b48c`  
		Last Modified: Wed, 02 Feb 2022 05:09:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067f26c276100ff9f120c16b02bc45c051335294bf81e0eb58129fb75db89c80`  
		Last Modified: Wed, 02 Feb 2022 08:11:57 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f18ebbaf9653b4ff92183b3c135b95e7fa849d06875c8a2371e9b3bb3988c5`  
		Last Modified: Wed, 02 Feb 2022 08:15:01 GMT  
		Size: 12.6 MB (12593751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58a3a0aec53fa5ec7f74f713c7237d5be99c6bcd5e36e0539300ed223972c8d`  
		Last Modified: Wed, 02 Feb 2022 08:15:00 GMT  
		Size: 217.4 KB (217412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:05f7a948d20c5499319e5865e745089bfde3ba3a812d739f07cd2da4eb1d49d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123118700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2df952b4fcec23a55dc2995a9e79051071657dbb2232a93e16fbdec8c695924`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:53:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:54:08 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 05:55:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:55:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:30:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 08:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:30:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 08:30:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 08:30:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 08:30:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 08:30:25 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 08:30:29 GMT
ENV TOMCAT_MAJOR=10
# Tue, 01 Mar 2022 03:57:34 GMT
ENV TOMCAT_VERSION=10.0.17
# Tue, 01 Mar 2022 03:57:35 GMT
ENV TOMCAT_SHA512=c9a8894ddedb9a4966abb8698a029c00dda2603acb798bbf11a99cf585c2e5db967bee006689ea148b819fa11d1d8fe1e799ceb09243e70b1310ca18ada1f17f
# Tue, 01 Mar 2022 03:57:36 GMT
COPY dir:81654d2fd290076fc591959b9d58040c3421a4a085c942e1cc594613f9893ad8 in /usr/local/tomcat 
# Tue, 01 Mar 2022 03:57:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:57:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 03:58:01 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 03:58:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c242a0abcf4a94e7bba5e39dfb42cf960cfe7f925cd1228e0fd07cd876ae719f`  
		Last Modified: Wed, 02 Feb 2022 05:59:05 GMT  
		Size: 31.1 MB (31123952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65986e91f8e38daef1c3d1a5c114482f2ffe98efe58f6b9d76a747816e6b389a`  
		Last Modified: Wed, 02 Feb 2022 06:00:23 GMT  
		Size: 45.6 MB (45621111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa899de57b4b17bed89df46194df87fdf0562f722d37ec5b12ff51f824cf471`  
		Last Modified: Wed, 02 Feb 2022 06:00:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94e02d78ad4867e25501b45f899163a2120a55e880ae6dfaf246a3ef501a86`  
		Last Modified: Wed, 02 Feb 2022 10:04:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c23d2fe2d97c9cbf7e04d71f2f82e25621cff8639152794e83421374d935fdf`  
		Last Modified: Tue, 01 Mar 2022 04:49:02 GMT  
		Size: 12.6 MB (12608500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31212ea6e4c20e5a7b6278a1c6ef5e9014fdef0d832ef2f9d71ae0e89895ccbe`  
		Last Modified: Tue, 01 Mar 2022 04:49:01 GMT  
		Size: 480.0 KB (479958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad050a3df42d0b5a72d0769828759a62ea7d4ed9346d1953259d05dd285230b7`  
		Last Modified: Tue, 01 Mar 2022 04:49:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:76508d9eb41cdd360f47a61eae47877eca7d6fc1b3bee0b4312b87004a806771
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111713124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1e2fad427bfe87a29a196bd515edba3ef70450e0ee143271898fbc442057e8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:22:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:24:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:24:41 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 02 Feb 2022 02:25:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:25:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:25:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 03:45:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 03:45:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 03:45:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 03:45:04 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 03:45:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 03:45:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 03:45:05 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 03:45:05 GMT
ENV TOMCAT_MAJOR=10
# Tue, 01 Mar 2022 02:39:41 GMT
ENV TOMCAT_VERSION=10.0.17
# Tue, 01 Mar 2022 02:39:41 GMT
ENV TOMCAT_SHA512=c9a8894ddedb9a4966abb8698a029c00dda2603acb798bbf11a99cf585c2e5db967bee006689ea148b819fa11d1d8fe1e799ceb09243e70b1310ca18ada1f17f
# Tue, 01 Mar 2022 02:39:41 GMT
COPY dir:39d188972f9046c8f85da54bce9a8c68d7c8aad160d53fcbece9cfec034a0b40 in /usr/local/tomcat 
# Tue, 01 Mar 2022 02:39:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:39:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 02:39:48 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 02:39:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1759c477ed4396a58633b60f32e9ec18132879182ced16e097eccef500139a18`  
		Last Modified: Wed, 02 Feb 2022 02:26:54 GMT  
		Size: 27.9 MB (27942553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a793c5a86122ed874e470618f12f60a3dc9560eda3eacfb240b1f7c373a16e89`  
		Last Modified: Wed, 02 Feb 2022 02:27:41 GMT  
		Size: 43.6 MB (43616377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd679e903c849b6dca91e8ec0e2f84979078c4daa049415debd58ba76a07d4`  
		Last Modified: Wed, 02 Feb 2022 02:27:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adf4e898740d6e5a6704bf43b2093eefc650fcc4c739a4745cac5f8250e29b`  
		Last Modified: Wed, 02 Feb 2022 04:32:23 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439db4001a698d35b731a084850abc2520b4c9e4cbe94b4b28d34ef7da896f79`  
		Last Modified: Tue, 01 Mar 2022 03:08:34 GMT  
		Size: 12.6 MB (12578552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce038d91f1e87ef983d10194e88bb191ff1a0c5ae9859b224d153772cb28660`  
		Last Modified: Tue, 01 Mar 2022 03:08:34 GMT  
		Size: 456.4 KB (456444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f369ae5379f4aba67b16dda59480e1e3091c85881e5d7393521b918607134f0`  
		Last Modified: Tue, 01 Mar 2022 03:08:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
