## `tomcat:jre11-temurin`

```console
$ docker pull tomcat@sha256:107e2659efb33b9bf7324e916e1b559b5a35b076454f0db89f6b654bd5eb4a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:4e5c9e512e0a406d1454579ef2d463add860b521983ba0eef98fb7cdc996b30a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109639703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5200c990c848acb619b5723ec722644e3f16d7526d3914407893b2a2977adbf3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:59:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 14:15:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 14:15:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 14:15:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 14:15:02 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 14:15:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:15:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:15:03 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 14:15:03 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 14:19:34 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 14:19:34 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 14:19:35 GMT
COPY dir:67e8dea18373c939f371de050e0af37febd9b7dc23955004bbe1def60f03cd7d in /usr/local/tomcat 
# Wed, 02 Feb 2022 14:19:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 14:19:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 14:19:41 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 14:19:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585a8f8fd99d708129717ae5fdac2d9fe803a5fee3291ff479f8dc04db42494`  
		Last Modified: Wed, 02 Feb 2022 03:03:11 GMT  
		Size: 43.2 MB (43230362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f03a4fb8d3d6c8106ee5f1bef091485bf8ae217d5c0a0b0e09f5c0e1a442f`  
		Last Modified: Wed, 02 Feb 2022 03:03:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e93d49756c3feac98aa2a87536a96b8e541e3401a0bfd0917c0a55d07440dd2`  
		Last Modified: Wed, 02 Feb 2022 14:52:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8b3b3692a06fafbbb7923b09d579f2f079a2bdb1060fa40f23e4720cbfaa00`  
		Last Modified: Wed, 02 Feb 2022 14:55:22 GMT  
		Size: 12.6 MB (12578152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c937fc2dbaf8f8384b8c69a62b5edbff09994bcc76f2c1bd3f1d53d1ce5b8`  
		Last Modified: Wed, 02 Feb 2022 14:55:21 GMT  
		Size: 452.0 KB (451967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066b7a51578c22048cfec3b7cf4c703d5f2c65b3343ebf13a721fc53e6ee365b`  
		Last Modified: Wed, 02 Feb 2022 14:55:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:1f1a744b8bcfdc99599797e37d1e5025172c50d295a9493b0356ba530e92f783
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101941688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2222e66fe75862ca8c16438cae408e6179f3965df023d580f04c2df2783f4af`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:48:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:48:04 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:49:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:49:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:52:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 05:52:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:52:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 05:52:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 05:52:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 05:52:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 05:52:22 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 05:52:22 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 05:59:42 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 05:59:43 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 05:59:45 GMT
COPY dir:817f89af51a9f15a0dc02364f41e35bc0b4b98b5aa9217e98921ddd9f097a29b in /usr/local/tomcat 
# Wed, 02 Feb 2022 06:00:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:00:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 06:00:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 06:00:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca45b223849013a5db7d5850e0832f4aac669b33c69f09d9d74f6d6ae56a91d8`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 23.1 MB (23072061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605123915fece369da5778c9391348661f9ac3f37a8d4e3663c9c282ef486789`  
		Last Modified: Wed, 02 Feb 2022 02:55:57 GMT  
		Size: 41.9 MB (41850725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b512710f7691986f4b2e05d64e27b40ab28ad601c130c9d986ca42d03dcb2`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5c2949c704bcc8fdcd00153ae2529f5a1386b958db959e4bbff6bf4de3f35`  
		Last Modified: Wed, 02 Feb 2022 06:29:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253e80147a4aa9b71494c8dccd779e26a17fceec89fc8052dcf8f65bfc071d6d`  
		Last Modified: Wed, 02 Feb 2022 06:32:59 GMT  
		Size: 12.5 MB (12527176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba33df55fb67fab924555e9ae4544830f614c0c2679b75754a34f799eee396b`  
		Last Modified: Wed, 02 Feb 2022 06:32:55 GMT  
		Size: 428.5 KB (428514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1764a02cc20dd113200a97beef23621a31fb6c9c625c89a2b353149ae2564593`  
		Last Modified: Wed, 02 Feb 2022 06:32:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:31ac5b8ce2db23e7a5f6c0ab6ff3c5138c6fa5b97ae8972a1bd769fda88e165d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3cb7c9c71f71dcae63568fe281215ad0783e138feb1863a876dfd6ca00f0aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:34 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:03:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:03:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 07:30:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 07:30:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 07:30:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 07:30:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 07:30:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:30:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:30:30 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 07:30:31 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 07:35:39 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 07:35:40 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 07:35:42 GMT
COPY dir:655297da92eb8a2a7d89a55dbcc83eb612eebbd38a5ec26f015d4e4317797d38 in /usr/local/tomcat 
# Wed, 02 Feb 2022 07:35:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 07:35:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 07:35:52 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 07:35:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6151ca955d4b7fb01dfd3c4470cc07f8484a7de594e6028377da2392b0b9d`  
		Last Modified: Wed, 02 Feb 2022 05:07:49 GMT  
		Size: 41.6 MB (41572184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5b05b981cfd36cda3c95e6c1b623132675dfd8e918bc928fb89bffc419f28`  
		Last Modified: Wed, 02 Feb 2022 05:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93888403ca11519785f17d02b1fab7f8903cc68f7ea400a407817fca0469eb8`  
		Last Modified: Wed, 02 Feb 2022 08:13:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bde3ba1829bee73a9e7f27224620589edcd43bf79eed058f47b0f77cf9148`  
		Last Modified: Wed, 02 Feb 2022 08:17:21 GMT  
		Size: 12.6 MB (12593594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2135f52e10e071563f4a957649ec135a64764f58203b248cea6f9ff438655335`  
		Last Modified: Wed, 02 Feb 2022 08:17:20 GMT  
		Size: 214.8 KB (214813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3d7015c65e03a8042d6504b6212e61021aebd391681f0a2e1f4cb9d472b414e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111664191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da5cfb561c0a316466563467cd506c4055a76c442a591c60d17047cfe7d9527`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:51:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:51:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:41:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 08:41:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:41:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 08:41:48 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 08:41:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 08:41:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 08:41:59 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 08:42:04 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 08:56:08 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 08:56:11 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 08:56:14 GMT
COPY dir:77aef7df356f70bac9fef91ffc48f96f5a0c41881b63462d89e83dea9cfda80f in /usr/local/tomcat 
# Wed, 02 Feb 2022 08:56:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 08:57:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 08:57:14 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 08:57:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ac27cb36bb8dd24defb16aca611d9a310ff50291b151fb1179fbb18e234e7`  
		Last Modified: Wed, 02 Feb 2022 05:58:45 GMT  
		Size: 38.6 MB (38641073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68febafb066e63efbfcc3c94c15fa0fdf31cc82e9682488ffc94ebe35434214a`  
		Last Modified: Wed, 02 Feb 2022 05:58:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bdbdd25dc34959a07fdfcfeb5f3e0c004d17f0b567b69a471e5d8f3e326e1c`  
		Last Modified: Wed, 02 Feb 2022 10:06:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0dfbbca21702c8fd9d74950d70418c7d724285cc99c107cf8346e2e79fe24b`  
		Last Modified: Wed, 02 Feb 2022 10:08:47 GMT  
		Size: 12.6 MB (12616917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6478485934df840d94fe4b6ae06116493487f8c8030087f71c48b635af1ed0c3`  
		Last Modified: Wed, 02 Feb 2022 10:08:45 GMT  
		Size: 477.7 KB (477749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74acc2189ba3648017972b3861a114145787d0f34e443ef1fe284a0af565223`  
		Last Modified: Wed, 02 Feb 2022 10:08:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:dab5505ab30f3eed5c282ee50d8447a539643a0963b186a90e076fa3406717c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101936876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a84da123b636c58f10e52728bccc9ddb61f55c33a50e0ac530ac9c8d254e63`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:22:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:23:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:23:16 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:23:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:23:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:23:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 03:48:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 03:48:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 03:48:51 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 03:48:51 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 03:48:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 03:48:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 03:48:51 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 03:48:51 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 03:57:11 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 03:57:11 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 03:57:12 GMT
COPY dir:644547c73bd7563d5f6893b9fee7e02b6fec9fb151d33a3b2f893464fcb61db9 in /usr/local/tomcat 
# Wed, 02 Feb 2022 03:57:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:57:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 03:57:19 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:57:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6f03368f8ab26f1db664cfc3332680df5d0a5a30115c89be2b6a6a1205c806`  
		Last Modified: Wed, 02 Feb 2022 02:26:22 GMT  
		Size: 24.4 MB (24446542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce1e4dbe7bbc1660306e1a6590ef71dca05ea74e4830731b98fd380333338a`  
		Last Modified: Wed, 02 Feb 2022 02:26:44 GMT  
		Size: 37.3 MB (37329092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c4b1e6c9a96f163f0bd7dbb802fb56046a3a19914592fce4a242ee037ad5f`  
		Last Modified: Wed, 02 Feb 2022 02:26:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788dd3b58c47fdea43d88c43ac7540cd31366d3f05c3ca6395f68b2ca6c00f9`  
		Last Modified: Wed, 02 Feb 2022 04:33:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb49c0d3e8f971b8ee8f4c9f6dd9623a6a1af022c570041ca051c8c2349c66d`  
		Last Modified: Wed, 02 Feb 2022 04:34:44 GMT  
		Size: 12.6 MB (12588330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef3ef2fceab6e09998daa5a3a488d980bf1229bc55e2a56c7dbf3a9e3507be4`  
		Last Modified: Wed, 02 Feb 2022 04:34:43 GMT  
		Size: 453.7 KB (453713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ade8b06ccb18c97e6128ccff940e955c82e2eca10dae3eab120bcd4349be3d`  
		Last Modified: Wed, 02 Feb 2022 04:34:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
