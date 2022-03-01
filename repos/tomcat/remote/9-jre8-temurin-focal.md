## `tomcat:9-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:785656b0e74a9a68c80a1f2db9d7ce4f8eef62ec986955b3d12f13fd2918a68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:43c129ceffd2649b3315a2ae074eeb2e596b2cb2162c6c4c8fea3ed7d647803a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107816491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dad56cd3f44ab8ede7931f1b9dd8534a97607ee9256891a85a1a03e745126a`
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
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Thu, 10 Feb 2022 20:19:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Feb 2022 20:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 20:19:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 10 Feb 2022 21:17:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 10 Feb 2022 21:17:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 21:17:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 10 Feb 2022 21:17:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 10 Feb 2022 21:17:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 21:17:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 21:21:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 10 Feb 2022 21:21:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Mar 2022 04:27:11 GMT
ENV TOMCAT_VERSION=9.0.59
# Tue, 01 Mar 2022 04:27:11 GMT
ENV TOMCAT_SHA512=74902b522abda04afb2be24d7410d4d93966d20fd07dde8f03bb281cdc714866f648babe1ff1ae85d663774779235f1cb9d701d5ce8884052f1f5efca7b62c68
# Tue, 01 Mar 2022 04:27:11 GMT
COPY dir:099915500da34d132285b3132cb8656481e156c9c845ec916c04360e12621070 in /usr/local/tomcat 
# Tue, 01 Mar 2022 04:27:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 04:27:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 04:27:16 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 04:27:17 GMT
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
	-	`sha256:210d9ab9b0e3a9edf152ba91a933a7e226a46353252eff007c7cf12dc3ff0582`  
		Last Modified: Thu, 10 Feb 2022 20:22:42 GMT  
		Size: 41.8 MB (41773827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb67723dccddf1cdad900703a1bb0f364b464c158b43d6cd0ada47e28b12b905`  
		Last Modified: Thu, 10 Feb 2022 20:22:37 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c053de7a580bf9cc1b9ab2673bd4ce0815de087c605256b8087cc4ce2559f27`  
		Last Modified: Thu, 10 Feb 2022 21:38:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f128c90e42d4d53e185a4fcb50fd218a6807e0b16690e779c06a237e0926753f`  
		Last Modified: Tue, 01 Mar 2022 05:22:40 GMT  
		Size: 12.2 MB (12211486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ceaa1ca11bafde33f84f0fb20b21c162170b0c66d3df18f8f9867b2672de2`  
		Last Modified: Tue, 01 Mar 2022 05:22:39 GMT  
		Size: 452.0 KB (451957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa615801114ac0647762d81faeadb0eae359da35658587fbef6ebb89f6fefc0`  
		Last Modified: Tue, 01 Mar 2022 05:22:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:ef93fc4f87b7be5b770635c2d5dc6d6a2c77de26915932401f7fbdfa78d42ca2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99238288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d683323a2797a1f24c9ce98d51480969927d198cae77e0446ccba49fb0843a`
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
# Thu, 10 Feb 2022 19:57:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Thu, 10 Feb 2022 19:58:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Feb 2022 19:58:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 19:58:53 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 10 Feb 2022 20:47:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 10 Feb 2022 20:47:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 20:47:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 10 Feb 2022 20:47:43 GMT
WORKDIR /usr/local/tomcat
# Thu, 10 Feb 2022 20:47:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 20:47:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 20:53:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 10 Feb 2022 20:53:31 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Mar 2022 05:44:26 GMT
ENV TOMCAT_VERSION=9.0.59
# Tue, 01 Mar 2022 05:44:26 GMT
ENV TOMCAT_SHA512=74902b522abda04afb2be24d7410d4d93966d20fd07dde8f03bb281cdc714866f648babe1ff1ae85d663774779235f1cb9d701d5ce8884052f1f5efca7b62c68
# Tue, 01 Mar 2022 05:44:29 GMT
COPY dir:6aeb37a9ccbc0e294dfc63333c953e7b8420c8fd131f5d5a6a5345027ed3278a in /usr/local/tomcat 
# Tue, 01 Mar 2022 05:44:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 05:44:42 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 05:44:43 GMT
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
	-	`sha256:82be717ebc5131faabd34c939bae692265aa21bf66c90dc3fe6d9dd1d7600756`  
		Last Modified: Thu, 10 Feb 2022 20:04:36 GMT  
		Size: 39.5 MB (39514060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8555afefe7fe8ba7a160318f4f0a04699bd0301bd42cd267cc0f2001f97c0cb0`  
		Last Modified: Thu, 10 Feb 2022 20:04:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73de8c848872780775779a19d1ff024f7e7eff01b6d53efa80120399cee85159`  
		Last Modified: Thu, 10 Feb 2022 21:15:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b378f0c817bd6dd94ef82cba3070941439a35611f8cb1887118c6c5d18352d`  
		Last Modified: Tue, 01 Mar 2022 06:16:00 GMT  
		Size: 12.2 MB (12159415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258be9f617d5522260b7059b67fcd40bd81252adab0b6fb1312f78ae3ed07015`  
		Last Modified: Tue, 01 Mar 2022 06:15:55 GMT  
		Size: 429.5 KB (429539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a28273b56903d3959a676f9dc7408eaa3255eaa784d4dda3472d2d3d7be40f1`  
		Last Modified: Tue, 01 Mar 2022 06:15:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:03d02882c0f47753c7e8116af9549417acc2fb09e4603a6bc08f5e61ea48accb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105181058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f084f60c2ac72ad3805da60571b31b4ee5cb029847e18e64da1f320b95e775d`
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
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Thu, 10 Feb 2022 19:40:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Feb 2022 19:40:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 19:40:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 10 Feb 2022 20:38:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 10 Feb 2022 20:38:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 20:38:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 10 Feb 2022 20:38:45 GMT
WORKDIR /usr/local/tomcat
# Thu, 10 Feb 2022 20:38:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 20:38:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 20:45:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 10 Feb 2022 20:45:03 GMT
ENV TOMCAT_MAJOR=9
# Thu, 10 Feb 2022 20:45:04 GMT
ENV TOMCAT_VERSION=9.0.58
# Thu, 10 Feb 2022 20:45:05 GMT
ENV TOMCAT_SHA512=33c030a312a0a087deeb06fff921d13a23789e152d30620f33a368e7a2244c762fcf9acd55f3b90f08560704ba45bc2be820bccf2058b0cf5801a7b124f9056d
# Thu, 10 Feb 2022 20:45:07 GMT
COPY dir:bb8bf259dab6fa5092c0b7071a4acc3d1fe7102bf872e5afc8a70084a14178dc in /usr/local/tomcat 
# Thu, 10 Feb 2022 20:45:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Feb 2022 20:45:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 10 Feb 2022 20:45:16 GMT
EXPOSE 8080
# Thu, 10 Feb 2022 20:45:17 GMT
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
	-	`sha256:70231d33174139d5a5af841cef765f0c2f53a6d827a2e1377479e4145cd342c9`  
		Last Modified: Thu, 10 Feb 2022 19:44:14 GMT  
		Size: 40.8 MB (40769834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db5b84fb44a991ff546b0be2b3fdae11254fc8b2a7fbcf858cb3dee3cccb22a`  
		Last Modified: Thu, 10 Feb 2022 19:44:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576cb187dc4e62638320b97d20acdd95ffd5c072d4fad160b8c6f510e694bc45`  
		Last Modified: Thu, 10 Feb 2022 21:13:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db42aee40f10c80781e80ae2455c7dc064e0e85e66eecd863dda0b4f00e3b9d`  
		Last Modified: Thu, 10 Feb 2022 21:17:04 GMT  
		Size: 12.3 MB (12263775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e39ea4ce13ff73e7c7ac55dcd3661626d959e71b3308cedd5d1c6b4e6e80244`  
		Last Modified: Thu, 10 Feb 2022 21:17:02 GMT  
		Size: 214.8 KB (214815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f38ef48090e215e0f8c795e2da07589c2306381a5c92c2578e00c39919c4f228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113823242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c4b1859bb547e02065def1c1e90bcd9a45e4b8f65a7b7ecaeb3b2fa04c6ef1`
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
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Thu, 10 Feb 2022 20:17:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Feb 2022 20:18:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 20:18:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 10 Feb 2022 21:10:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 10 Feb 2022 21:10:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Feb 2022 21:10:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 10 Feb 2022 21:10:29 GMT
WORKDIR /usr/local/tomcat
# Thu, 10 Feb 2022 21:10:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 21:10:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 10 Feb 2022 21:21:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 10 Feb 2022 21:21:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 01 Mar 2022 04:25:31 GMT
ENV TOMCAT_VERSION=9.0.59
# Tue, 01 Mar 2022 04:25:33 GMT
ENV TOMCAT_SHA512=74902b522abda04afb2be24d7410d4d93966d20fd07dde8f03bb281cdc714866f648babe1ff1ae85d663774779235f1cb9d701d5ce8884052f1f5efca7b62c68
# Tue, 01 Mar 2022 04:25:35 GMT
COPY dir:ca1e33f266f678831bfdc9dd7618a52207898f71af4091b6de8fa65e6378273c in /usr/local/tomcat 
# Tue, 01 Mar 2022 04:25:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 04:25:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 01 Mar 2022 04:25:59 GMT
EXPOSE 8080
# Tue, 01 Mar 2022 04:26:01 GMT
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
	-	`sha256:3e3fa1d775e129e1f9e684662aa301cca80c1439b23f0d17c6117e73ed710457`  
		Last Modified: Thu, 10 Feb 2022 20:23:52 GMT  
		Size: 41.2 MB (41162346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67891daefaca5525d234d82f300ecc946818261b7d7e6e28478d1927b210ad28`  
		Last Modified: Thu, 10 Feb 2022 20:23:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1865118cbc0c6729e4f9fdd13141030ce4a4bc70a64d49315ca80dd98ab1f0be`  
		Last Modified: Thu, 10 Feb 2022 21:42:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e547810a2c06e01a179bfd51b1fb27dee9361f0bc754aa1f0107aa4880a8bbfc`  
		Last Modified: Tue, 01 Mar 2022 04:55:26 GMT  
		Size: 12.3 MB (12254711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aec1fa114f6db7de55aa5a77ff0ce00ac0edf85b24e02e354f5c95bd0c6aee1`  
		Last Modified: Tue, 01 Mar 2022 04:55:25 GMT  
		Size: 477.7 KB (477733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987c8cc987dabc41f8083ade445446ac8cf1e94eca77c356d89924cbc698a2d`  
		Last Modified: Tue, 01 Mar 2022 04:55:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
