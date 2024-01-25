<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spark`

-	[`spark:3.4.1`](#spark341)
-	[`spark:3.4.1-python3`](#spark341-python3)
-	[`spark:3.4.1-r`](#spark341-r)
-	[`spark:3.4.1-scala`](#spark341-scala)
-	[`spark:3.4.1-scala2.12-java11-python3-r-ubuntu`](#spark341-scala212-java11-python3-r-ubuntu)
-	[`spark:3.4.1-scala2.12-java11-python3-ubuntu`](#spark341-scala212-java11-python3-ubuntu)
-	[`spark:3.4.1-scala2.12-java11-r-ubuntu`](#spark341-scala212-java11-r-ubuntu)
-	[`spark:3.4.1-scala2.12-java11-ubuntu`](#spark341-scala212-java11-ubuntu)
-	[`spark:3.5.0`](#spark350)
-	[`spark:3.5.0-java17`](#spark350-java17)
-	[`spark:3.5.0-java17-python3`](#spark350-java17-python3)
-	[`spark:3.5.0-java17-r`](#spark350-java17-r)
-	[`spark:3.5.0-java17-scala`](#spark350-java17-scala)
-	[`spark:3.5.0-python3`](#spark350-python3)
-	[`spark:3.5.0-r`](#spark350-r)
-	[`spark:3.5.0-scala`](#spark350-scala)
-	[`spark:3.5.0-scala2.12-java11-python3-r-ubuntu`](#spark350-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.0-scala2.12-java11-python3-ubuntu`](#spark350-scala212-java11-python3-ubuntu)
-	[`spark:3.5.0-scala2.12-java11-r-ubuntu`](#spark350-scala212-java11-r-ubuntu)
-	[`spark:3.5.0-scala2.12-java11-ubuntu`](#spark350-scala212-java11-ubuntu)
-	[`spark:3.5.0-scala2.12-java17-python3-r-ubuntu`](#spark350-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.0-scala2.12-java17-python3-ubuntu`](#spark350-scala212-java17-python3-ubuntu)
-	[`spark:3.5.0-scala2.12-java17-r-ubuntu`](#spark350-scala212-java17-r-ubuntu)
-	[`spark:3.5.0-scala2.12-java17-ubuntu`](#spark350-scala212-java17-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.4.1`

```console
$ docker pull spark@sha256:6f47825b37da97567f6ec83f6317f0a4b5e766463bfe4c4149600f2e4c5c4cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1` - linux; amd64

```console
$ docker pull spark@sha256:6f58646cca1b88e60bcd6007bd9a054f94ca08aea2050049e0dea71e17e10807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529098024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365a3ec92518f282fd5ecae94051ee9d2c99484e02661b79f85ac355071dd69`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:43:03 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaf65b9252788d9b9ead6b55da68be73c2ae1b5c610a33fcf26a553617da526`  
		Last Modified: Thu, 25 Jan 2024 02:50:09 GMT  
		Size: 94.6 MB (94598212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:95d37e4001a4739fb916b73c0bed855c2d12aae823db8164abb7dea362af23bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.6 MB (518579544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f328e09cc165c7b5f904ca14baa4fc52cbf2ce5bf1365e112a397879d0c980`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:06:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:45 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf1fcd4884909c8e6aec405e419663a33af03c04295731bef951dc19eb127dd`  
		Last Modified: Thu, 25 Jan 2024 01:12:34 GMT  
		Size: 87.6 MB (87555777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-python3`

```console
$ docker pull spark@sha256:6f47825b37da97567f6ec83f6317f0a4b5e766463bfe4c4149600f2e4c5c4cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:6f58646cca1b88e60bcd6007bd9a054f94ca08aea2050049e0dea71e17e10807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529098024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365a3ec92518f282fd5ecae94051ee9d2c99484e02661b79f85ac355071dd69`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:43:03 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaf65b9252788d9b9ead6b55da68be73c2ae1b5c610a33fcf26a553617da526`  
		Last Modified: Thu, 25 Jan 2024 02:50:09 GMT  
		Size: 94.6 MB (94598212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:95d37e4001a4739fb916b73c0bed855c2d12aae823db8164abb7dea362af23bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.6 MB (518579544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f328e09cc165c7b5f904ca14baa4fc52cbf2ce5bf1365e112a397879d0c980`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:06:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:45 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf1fcd4884909c8e6aec405e419663a33af03c04295731bef951dc19eb127dd`  
		Last Modified: Thu, 25 Jan 2024 01:12:34 GMT  
		Size: 87.6 MB (87555777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-r`

```console
$ docker pull spark@sha256:06b1ed097bda82220c77ce395215d44dec158c4dc411b378b42f0b5d2c140485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-r` - linux; amd64

```console
$ docker pull spark@sha256:5a6b61e0a06b19f1d2fd5db9fd2896e2340c6c08289ef60fcc28ecb9b0ec50f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666790964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8326378b1b3666339f0ddcf3dfb9b01210d24d5c2a3b035dedf532c6684ad291`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:43:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:43:54 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:43:54 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf60c3ef845faee43dd7549d845639e85109d23f84a9f56b1d007a81734fefa`  
		Last Modified: Thu, 25 Jan 2024 02:50:48 GMT  
		Size: 232.3 MB (232291152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:75f3ac6add93096fa74bb1c730f1dabcb85a9fb496939f62867e22bb73654a23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.5 MB (644530552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142840d2fe4c36cda4cd6b15e5f9776c679fc738cee51975b19a8977fea6175b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:07:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:07:24 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:07:24 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1edfd38b08a46a9050e63c0c872071e86acc901dc4ce52bace28e43207086`  
		Last Modified: Thu, 25 Jan 2024 01:13:04 GMT  
		Size: 213.5 MB (213506785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala`

```console
$ docker pull spark@sha256:c762e6760f3f69eaf954c6243d64c8f58c6f8df0484d4d47cf182b202c39f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:bb78077a9efa4e78776194d8165c341316bf2ab8bc7dbedaae0c2269f048994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434499812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07176d48b1f2b42c08824ea23d55c76375bd9bdcaabf0ba592e564cf727eb02`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:6ab82cc94d42a562d43d1cba9196efdb7873af1765ebf36da4a4a60942730e03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431023767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d403ba7a3fd1fc77800263282a7fbeaa18322e28eb20520d26a64f56695668d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:7f242d2782f23b4924c15d1453b715567545d91cf7db144c9a1fed2658ffc09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:353b4f3e49a77b440109266f7cc157a5ce6d4e59d13bfd91b09488e4ba360642
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.4 MB (688398790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ee539c67605578ace4dfc3a1164d0cbb00d4d09222da55adfe1abd63496fcd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:39:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:39:43 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:39:43 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4c865895e37d7ca4be8b83f23b423aed9a95a16614a50830ae22814f8c3b2`  
		Last Modified: Thu, 25 Jan 2024 02:47:24 GMT  
		Size: 253.9 MB (253898978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8c5551b7ab86a8010222e15a37db780bb675c3009bf30d354d0852950c9f059d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.2 MB (666162154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59443b5f2b8445bd293a49664360393cfc24e1fa726c131fc9978e694477add3`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:03:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:04:02 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:04:02 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8330a39e5e7948da14d6f9b35b0e9130360fd48e926c163bb9bbe3345d582acc`  
		Last Modified: Thu, 25 Jan 2024 01:10:19 GMT  
		Size: 235.1 MB (235138387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:6f47825b37da97567f6ec83f6317f0a4b5e766463bfe4c4149600f2e4c5c4cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6f58646cca1b88e60bcd6007bd9a054f94ca08aea2050049e0dea71e17e10807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529098024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365a3ec92518f282fd5ecae94051ee9d2c99484e02661b79f85ac355071dd69`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:43:03 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaf65b9252788d9b9ead6b55da68be73c2ae1b5c610a33fcf26a553617da526`  
		Last Modified: Thu, 25 Jan 2024 02:50:09 GMT  
		Size: 94.6 MB (94598212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:95d37e4001a4739fb916b73c0bed855c2d12aae823db8164abb7dea362af23bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.6 MB (518579544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f328e09cc165c7b5f904ca14baa4fc52cbf2ce5bf1365e112a397879d0c980`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:06:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:45 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf1fcd4884909c8e6aec405e419663a33af03c04295731bef951dc19eb127dd`  
		Last Modified: Thu, 25 Jan 2024 01:12:34 GMT  
		Size: 87.6 MB (87555777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:06b1ed097bda82220c77ce395215d44dec158c4dc411b378b42f0b5d2c140485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5a6b61e0a06b19f1d2fd5db9fd2896e2340c6c08289ef60fcc28ecb9b0ec50f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666790964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8326378b1b3666339f0ddcf3dfb9b01210d24d5c2a3b035dedf532c6684ad291`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:38:51 GMT
USER root
# Thu, 25 Jan 2024 02:43:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:43:54 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:43:54 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf60c3ef845faee43dd7549d845639e85109d23f84a9f56b1d007a81734fefa`  
		Last Modified: Thu, 25 Jan 2024 02:50:48 GMT  
		Size: 232.3 MB (232291152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:75f3ac6add93096fa74bb1c730f1dabcb85a9fb496939f62867e22bb73654a23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.5 MB (644530552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142840d2fe4c36cda4cd6b15e5f9776c679fc738cee51975b19a8977fea6175b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 01:03:19 GMT
USER root
# Thu, 25 Jan 2024 01:07:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:07:24 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:07:24 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c1edfd38b08a46a9050e63c0c872071e86acc901dc4ce52bace28e43207086`  
		Last Modified: Thu, 25 Jan 2024 01:13:04 GMT  
		Size: 213.5 MB (213506785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:c762e6760f3f69eaf954c6243d64c8f58c6f8df0484d4d47cf182b202c39f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bb78077a9efa4e78776194d8165c341316bf2ab8bc7dbedaae0c2269f048994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434499812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07176d48b1f2b42c08824ea23d55c76375bd9bdcaabf0ba592e564cf727eb02`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:41 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 02:38:38 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:38:38 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 02:38:38 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:38:38 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:38:39 GMT
USER spark
# Thu, 25 Jan 2024 02:38:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b68ff5c607c0e42b063ccee3e4f0b70ba283c0c6105a98f7a30a433d359d4`  
		Last Modified: Thu, 25 Jan 2024 02:46:44 GMT  
		Size: 317.9 MB (317886734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6a8b91c026ff55dcf7da2d9f1a5876da623050207bd4c02939ba4021e3b06`  
		Last Modified: Thu, 25 Jan 2024 02:46:30 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:6ab82cc94d42a562d43d1cba9196efdb7873af1765ebf36da4a4a60942730e03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431023767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d403ba7a3fd1fc77800263282a7fbeaa18322e28eb20520d26a64f56695668d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 25 Jan 2024 01:03:07 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 01:03:09 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Thu, 25 Jan 2024 01:03:09 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 01:03:09 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 01:03:09 GMT
USER spark
# Thu, 25 Jan 2024 01:03:09 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2b2b356ad07a09798d5408498b82288a5523bc39004573759fbf14be4b6dd3`  
		Last Modified: Thu, 25 Jan 2024 01:09:49 GMT  
		Size: 317.9 MB (317886724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc910b48cc4993333f8aabdbd5aaa70c414e205f658295b603677db155e44f2`  
		Last Modified: Thu, 25 Jan 2024 01:09:33 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0`

```console
$ docker pull spark@sha256:123d96ebbb186077777ee5a768adb7e7ed1885751eb5aec5ce02ccee694d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0` - linux; amd64

```console
$ docker pull spark@sha256:93b81276df3a527c057ca320a6a2f371c66f888bdf02b0250961dca80c5d09e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.6 MB (535639659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba4497951c56d65a7352c7fc37b44aca144fed4b3cfc46808f6dada764e84e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:41:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:35 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03b81ac697d5c5a0e5ecbd44f54c955933863e6a7c9ed4025dbfbe77c62a84`  
		Last Modified: Thu, 25 Jan 2024 02:49:00 GMT  
		Size: 94.6 MB (94598166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f86c482b14d0dd567c7ca0fb7effcef2ed33f73b2a62042cc7ac7c1f71aab1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525121370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a481c4cc7ca88b66b9faf097044e149908f85dade0579667a6209ec19ce4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:05:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:46 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2234875069a59c9bf7a6dfb1f7f91c3973761e66ef6cf49388c2e3b9e57d0b97`  
		Last Modified: Thu, 25 Jan 2024 01:11:40 GMT  
		Size: 87.6 MB (87555864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17`

```console
$ docker pull spark@sha256:3090856e384024bb81ca9cd6a59a7c5c0013c516875f852f73de93e78c6b6612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17` - linux; amd64

```console
$ docker pull spark@sha256:aceeb22325a6ff8fdcdf436334c3002ea17d80e312d3eab180bb3fcf85777731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558563499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aff4a5810b474a03899adf88da05835a4d23541eeb5a017f039e254d6a9bf9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:40:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:40:10 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafd0723e0fc237476ead4a09f1852528ee50ec615c28e1cbf1b00984f3683d`  
		Last Modified: Thu, 25 Jan 2024 02:47:46 GMT  
		Size: 114.0 MB (113964290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e8b8a8c04131943156b9264dfcfdab415765ddb0c24898d7a2fa96092e8aa153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551597379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e7811fee5323f017aed5e08e5205f4ed978e25c64797ac3355b3c6d878f74a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:04:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:04:26 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525e30c91f3e504a6952036ea4874a7f48f14a7a070a8d9ec8d0d7244f66599`  
		Last Modified: Thu, 25 Jan 2024 01:10:38 GMT  
		Size: 108.5 MB (108527909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-python3`

```console
$ docker pull spark@sha256:3090856e384024bb81ca9cd6a59a7c5c0013c516875f852f73de93e78c6b6612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:aceeb22325a6ff8fdcdf436334c3002ea17d80e312d3eab180bb3fcf85777731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558563499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aff4a5810b474a03899adf88da05835a4d23541eeb5a017f039e254d6a9bf9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:40:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:40:10 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafd0723e0fc237476ead4a09f1852528ee50ec615c28e1cbf1b00984f3683d`  
		Last Modified: Thu, 25 Jan 2024 02:47:46 GMT  
		Size: 114.0 MB (113964290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e8b8a8c04131943156b9264dfcfdab415765ddb0c24898d7a2fa96092e8aa153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551597379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e7811fee5323f017aed5e08e5205f4ed978e25c64797ac3355b3c6d878f74a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:04:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:04:26 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525e30c91f3e504a6952036ea4874a7f48f14a7a070a8d9ec8d0d7244f66599`  
		Last Modified: Thu, 25 Jan 2024 01:10:38 GMT  
		Size: 108.5 MB (108527909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-r`

```console
$ docker pull spark@sha256:9a9d610ca8940f76b73dc20e6f3ad103d320141bc3d3c07e3869b2f6c19fb43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:a624eb28ad1a4ef3e0c18c6d03969e695089c3c4102f3aec95ec32a7a89a560b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763375242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2cd73ba2a1f579629860dffd5b32642cca6e32de753eb670888015e030750`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:41:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:05 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:41:05 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4c634d4206a4ace1d9cf177dff1a9149df35701f64b3880cd3898a8237649`  
		Last Modified: Thu, 25 Jan 2024 02:48:37 GMT  
		Size: 318.8 MB (318776033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:214a9a9f0229e7a26abac8d685623a7b2e5f07633637ec8b71bdb6b808be7d86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.0 MB (744978937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe475ba68f7386d2d8d6459ce500d92a8da4802ea06b3d094101862464819453`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:05:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:18 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:05:18 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3006529901d4b7accf97a0ab30853c76a519fc786406d8ba57606d45e0890c8b`  
		Last Modified: Thu, 25 Jan 2024 01:11:20 GMT  
		Size: 301.9 MB (301909467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-scala`

```console
$ docker pull spark@sha256:a408b9a33abc9e78c6b688e065847ad0c9f655e49a9a111d3da55e46729d7e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:8c4087734b10d78d2b80cfaa33aedc13b5cce195ccb2d7eca7718dfb3cc2bb5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444599209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e2f57465edcf6f0e77f185356917abb1f2b9f5a287d41327816110b95e93ce`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:77dd3beb6497b6c19476035ce41d5281891067ddaac2b3d4076ab468cc326f68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.1 MB (443069470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee99f5d6475532e4c13571b32b6d44bc84164c9a6d991cb96c2343bc7536509`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-python3`

```console
$ docker pull spark@sha256:123d96ebbb186077777ee5a768adb7e7ed1885751eb5aec5ce02ccee694d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-python3` - linux; amd64

```console
$ docker pull spark@sha256:93b81276df3a527c057ca320a6a2f371c66f888bdf02b0250961dca80c5d09e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.6 MB (535639659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba4497951c56d65a7352c7fc37b44aca144fed4b3cfc46808f6dada764e84e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:41:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:35 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03b81ac697d5c5a0e5ecbd44f54c955933863e6a7c9ed4025dbfbe77c62a84`  
		Last Modified: Thu, 25 Jan 2024 02:49:00 GMT  
		Size: 94.6 MB (94598166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f86c482b14d0dd567c7ca0fb7effcef2ed33f73b2a62042cc7ac7c1f71aab1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525121370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a481c4cc7ca88b66b9faf097044e149908f85dade0579667a6209ec19ce4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:05:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:46 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2234875069a59c9bf7a6dfb1f7f91c3973761e66ef6cf49388c2e3b9e57d0b97`  
		Last Modified: Thu, 25 Jan 2024 01:11:40 GMT  
		Size: 87.6 MB (87555864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-r`

```console
$ docker pull spark@sha256:d0538b8724d255fb581be15b6052fe60ed416902abb478ce5a51cc77fe806012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-r` - linux; amd64

```console
$ docker pull spark@sha256:11ae1a653525f2bc647252ae748638bd33486ece60ee8d4c6d3aebcf02181243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.3 MB (673332676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94366a276cfb07548758b841bdfc7c2e3eade9b32ad4cfdeb882d782823c8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:42:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:42:29 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:42:29 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340527fa69c46048963b7e474423a04f8a7820f9dd84264e2b679001fde3770`  
		Last Modified: Thu, 25 Jan 2024 02:49:43 GMT  
		Size: 232.3 MB (232291183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:da719cfd5edf7833755316c985250dd6c212a905c644c4ec3f1b2ff8a2a1566b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651072477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56402184ced3231482f9147752c2c464c0525571441c1449edbb43eb1e0823d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:06:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:23 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:06:24 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70e9ef23be8ba509b5e0a95421570245d3eab75ec12cef236f9ffea4cc87d0e`  
		Last Modified: Thu, 25 Jan 2024 01:12:13 GMT  
		Size: 213.5 MB (213506971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala`

```console
$ docker pull spark@sha256:1d9b6d7857fa8685a8156668a207b667a0f40e2d1d5d3627ae8521c12318f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala` - linux; amd64

```console
$ docker pull spark@sha256:e90d02425a76e48f9ac3c8bb4391799d851db5802f3c88d53264a5d4d542b227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.0 MB (441041493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c306473efd48fe73b60c75f719b488f4cc574778c9dd85b8e0f247762ec9b0a6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8ee5d1e2c20192f71a30bb3a4d59caa00044a29a339406ba97ff86e5cc76df57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.6 MB (437565506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8919cf2556b77a25147f65a7a00df910ef38872d1dac662958b15f8f50821347`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:03b11e9e23791210ad9c2c5ed9435771dcd8b2b272e02ac85ceeb9d457c06952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:24ad883b697a5fa7cd62b445a39e159c6ec7de92e2ef8cd3b0a2ac14ecbfb3d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.9 MB (694940297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa616fd1f5d4321b38b2354da5e0f71898d9af3013149f70d2f8cec47b5f2c6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:37:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:37:25 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:37:25 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d54cbe9b76b35107bdb1077c8d03a95211371a435d4bf23fac070b9d888ab1`  
		Last Modified: Thu, 25 Jan 2024 02:46:24 GMT  
		Size: 253.9 MB (253898804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c8bab34e5a8061d3a0f2d0ed0c490b56ba3d6c9e3783cab4de91d8258beec195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.7 MB (672703408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67bb5951887e3fc624d4afcc6c85f483a2693cc0cc35d5433dc1d23bff4e4bb`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:02:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:02:06 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:02:06 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501de43f2ca807a47bee9a46f28f249c48bd59bd930ca8904fbdf7811c9395d4`  
		Last Modified: Thu, 25 Jan 2024 01:09:26 GMT  
		Size: 235.1 MB (235137902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:123d96ebbb186077777ee5a768adb7e7ed1885751eb5aec5ce02ccee694d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:93b81276df3a527c057ca320a6a2f371c66f888bdf02b0250961dca80c5d09e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.6 MB (535639659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba4497951c56d65a7352c7fc37b44aca144fed4b3cfc46808f6dada764e84e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:41:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:35 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03b81ac697d5c5a0e5ecbd44f54c955933863e6a7c9ed4025dbfbe77c62a84`  
		Last Modified: Thu, 25 Jan 2024 02:49:00 GMT  
		Size: 94.6 MB (94598166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f86c482b14d0dd567c7ca0fb7effcef2ed33f73b2a62042cc7ac7c1f71aab1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525121370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a481c4cc7ca88b66b9faf097044e149908f85dade0579667a6209ec19ce4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:05:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:46 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2234875069a59c9bf7a6dfb1f7f91c3973761e66ef6cf49388c2e3b9e57d0b97`  
		Last Modified: Thu, 25 Jan 2024 01:11:40 GMT  
		Size: 87.6 MB (87555864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:d0538b8724d255fb581be15b6052fe60ed416902abb478ce5a51cc77fe806012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:11ae1a653525f2bc647252ae748638bd33486ece60ee8d4c6d3aebcf02181243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.3 MB (673332676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94366a276cfb07548758b841bdfc7c2e3eade9b32ad4cfdeb882d782823c8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:42:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:42:29 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:42:29 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340527fa69c46048963b7e474423a04f8a7820f9dd84264e2b679001fde3770`  
		Last Modified: Thu, 25 Jan 2024 02:49:43 GMT  
		Size: 232.3 MB (232291183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:da719cfd5edf7833755316c985250dd6c212a905c644c4ec3f1b2ff8a2a1566b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651072477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56402184ced3231482f9147752c2c464c0525571441c1449edbb43eb1e0823d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:06:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:23 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:06:24 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70e9ef23be8ba509b5e0a95421570245d3eab75ec12cef236f9ffea4cc87d0e`  
		Last Modified: Thu, 25 Jan 2024 01:12:13 GMT  
		Size: 213.5 MB (213506971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:1d9b6d7857fa8685a8156668a207b667a0f40e2d1d5d3627ae8521c12318f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:e90d02425a76e48f9ac3c8bb4391799d851db5802f3c88d53264a5d4d542b227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.0 MB (441041493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c306473efd48fe73b60c75f719b488f4cc574778c9dd85b8e0f247762ec9b0a6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8ee5d1e2c20192f71a30bb3a4d59caa00044a29a339406ba97ff86e5cc76df57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.6 MB (437565506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8919cf2556b77a25147f65a7a00df910ef38872d1dac662958b15f8f50821347`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:e94e637010e6e9eb8954742f82d0f6684b879f4073e2997502106045ad5d1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:d9ddc5a99da760c11b954f197f02a87defbb91a8e185bcc0693f906fefc6b507
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.1 MB (778102530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b44e49f1f64c28ec61e62444d86c291916c5e36d9a91da601a76a22caeaf35`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:32:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:32:51 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:32:51 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b9932d3733871709c236166d463a9a30dfb090c56fac0393d483e02a2cf497`  
		Last Modified: Thu, 25 Jan 2024 02:45:22 GMT  
		Size: 333.5 MB (333503321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:01a57b33c4b5ebbda35442e59755b9960df0d86757bc27e608949567179736f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 MB (759533930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e251d4a3d4d3d5575ef7f615379527fe3f8adcc2c65517d4acd075a36bfb13`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 00:53:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:53:22 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 00:53:22 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656bcd85ffcd7f237cfd08d1e8a42d3b0643b8e14212cee660588f0daeef2c4c`  
		Last Modified: Thu, 25 Jan 2024 01:08:36 GMT  
		Size: 316.5 MB (316464460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:3090856e384024bb81ca9cd6a59a7c5c0013c516875f852f73de93e78c6b6612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:aceeb22325a6ff8fdcdf436334c3002ea17d80e312d3eab180bb3fcf85777731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558563499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aff4a5810b474a03899adf88da05835a4d23541eeb5a017f039e254d6a9bf9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:40:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:40:10 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafd0723e0fc237476ead4a09f1852528ee50ec615c28e1cbf1b00984f3683d`  
		Last Modified: Thu, 25 Jan 2024 02:47:46 GMT  
		Size: 114.0 MB (113964290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e8b8a8c04131943156b9264dfcfdab415765ddb0c24898d7a2fa96092e8aa153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551597379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e7811fee5323f017aed5e08e5205f4ed978e25c64797ac3355b3c6d878f74a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:04:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:04:26 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525e30c91f3e504a6952036ea4874a7f48f14a7a070a8d9ec8d0d7244f66599`  
		Last Modified: Thu, 25 Jan 2024 01:10:38 GMT  
		Size: 108.5 MB (108527909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:9a9d610ca8940f76b73dc20e6f3ad103d320141bc3d3c07e3869b2f6c19fb43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a624eb28ad1a4ef3e0c18c6d03969e695089c3c4102f3aec95ec32a7a89a560b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763375242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2cd73ba2a1f579629860dffd5b32642cca6e32de753eb670888015e030750`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:41:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:05 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:41:05 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4c634d4206a4ace1d9cf177dff1a9149df35701f64b3880cd3898a8237649`  
		Last Modified: Thu, 25 Jan 2024 02:48:37 GMT  
		Size: 318.8 MB (318776033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:214a9a9f0229e7a26abac8d685623a7b2e5f07633637ec8b71bdb6b808be7d86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.0 MB (744978937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe475ba68f7386d2d8d6459ce500d92a8da4802ea06b3d094101862464819453`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:05:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:18 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:05:18 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3006529901d4b7accf97a0ab30853c76a519fc786406d8ba57606d45e0890c8b`  
		Last Modified: Thu, 25 Jan 2024 01:11:20 GMT  
		Size: 301.9 MB (301909467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:a408b9a33abc9e78c6b688e065847ad0c9f655e49a9a111d3da55e46729d7e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:8c4087734b10d78d2b80cfaa33aedc13b5cce195ccb2d7eca7718dfb3cc2bb5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444599209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e2f57465edcf6f0e77f185356917abb1f2b9f5a287d41327816110b95e93ce`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:77dd3beb6497b6c19476035ce41d5281891067ddaac2b3d4076ab468cc326f68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.1 MB (443069470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee99f5d6475532e4c13571b32b6d44bc84164c9a6d991cb96c2343bc7536509`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:latest`

```console
$ docker pull spark@sha256:123d96ebbb186077777ee5a768adb7e7ed1885751eb5aec5ce02ccee694d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:93b81276df3a527c057ca320a6a2f371c66f888bdf02b0250961dca80c5d09e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.6 MB (535639659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba4497951c56d65a7352c7fc37b44aca144fed4b3cfc46808f6dada764e84e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:41:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:35 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03b81ac697d5c5a0e5ecbd44f54c955933863e6a7c9ed4025dbfbe77c62a84`  
		Last Modified: Thu, 25 Jan 2024 02:49:00 GMT  
		Size: 94.6 MB (94598166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f86c482b14d0dd567c7ca0fb7effcef2ed33f73b2a62042cc7ac7c1f71aab1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525121370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a481c4cc7ca88b66b9faf097044e149908f85dade0579667a6209ec19ce4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:05:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:46 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2234875069a59c9bf7a6dfb1f7f91c3973761e66ef6cf49388c2e3b9e57d0b97`  
		Last Modified: Thu, 25 Jan 2024 01:11:40 GMT  
		Size: 87.6 MB (87555864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:python3`

```console
$ docker pull spark@sha256:123d96ebbb186077777ee5a768adb7e7ed1885751eb5aec5ce02ccee694d9c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:93b81276df3a527c057ca320a6a2f371c66f888bdf02b0250961dca80c5d09e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.6 MB (535639659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba4497951c56d65a7352c7fc37b44aca144fed4b3cfc46808f6dada764e84e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:41:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:41:35 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb03b81ac697d5c5a0e5ecbd44f54c955933863e6a7c9ed4025dbfbe77c62a84`  
		Last Modified: Thu, 25 Jan 2024 02:49:00 GMT  
		Size: 94.6 MB (94598166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7f86c482b14d0dd567c7ca0fb7effcef2ed33f73b2a62042cc7ac7c1f71aab1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525121370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a481c4cc7ca88b66b9faf097044e149908f85dade0579667a6209ec19ce4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:05:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:05:46 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2234875069a59c9bf7a6dfb1f7f91c3973761e66ef6cf49388c2e3b9e57d0b97`  
		Last Modified: Thu, 25 Jan 2024 01:11:40 GMT  
		Size: 87.6 MB (87555864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:python3-java17`

```console
$ docker pull spark@sha256:3090856e384024bb81ca9cd6a59a7c5c0013c516875f852f73de93e78c6b6612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:aceeb22325a6ff8fdcdf436334c3002ea17d80e312d3eab180bb3fcf85777731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558563499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aff4a5810b474a03899adf88da05835a4d23541eeb5a017f039e254d6a9bf9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:28:20 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:28:21 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:28:40 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:28:40 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:29:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:29:40 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:29:40 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:29:40 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:29:40 GMT
USER spark
# Thu, 25 Jan 2024 02:29:40 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:29:44 GMT
USER root
# Thu, 25 Jan 2024 02:40:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:40:10 GMT
USER spark
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb8b68f8fd5ce24a97ff6aace90937eea3bca94b9e2c09094b7731b5eca11a`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3dc1bb575f02cfd623c4fa066d550a1064314cb10c64af28ae1cfd997a3a37`  
		Last Modified: Thu, 25 Jan 2024 02:44:24 GMT  
		Size: 25.1 MB (25097888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7100d5bea49ee9ea85c02c78b2cd075fe9b223b10fb8735c19a542eb3f9a2022`  
		Last Modified: Thu, 25 Jan 2024 02:44:31 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea44649b461864b33465f7a6b18b7ed47f6133ba69ea0261351dabb3a26bc8b`  
		Last Modified: Thu, 25 Jan 2024 02:44:17 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafd0723e0fc237476ead4a09f1852528ee50ec615c28e1cbf1b00984f3683d`  
		Last Modified: Thu, 25 Jan 2024 02:47:46 GMT  
		Size: 114.0 MB (113964290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e8b8a8c04131943156b9264dfcfdab415765ddb0c24898d7a2fa96092e8aa153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551597379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e7811fee5323f017aed5e08e5205f4ed978e25c64797ac3355b3c6d878f74a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:47:52 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:47:53 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:48:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:48:18 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:49:18 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:49:20 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:49:20 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:49:20 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:49:20 GMT
USER spark
# Thu, 25 Jan 2024 00:49:20 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:49:30 GMT
USER root
# Thu, 25 Jan 2024 01:04:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:04:26 GMT
USER spark
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b26b3221c0fdb9ca31c8bd12dd9eac1fc7d85d2677ba7475ac277ba5b2a55b`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8362adba26c677d855936c2ac1fbef89b79b2dcfcbc22b907157ee2eaaf87`  
		Last Modified: Thu, 25 Jan 2024 01:07:50 GMT  
		Size: 24.7 MB (24737607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76f009d31932096df7b979537892874c0e9f5361d80db9713503897c6d9f89`  
		Last Modified: Thu, 25 Jan 2024 01:07:59 GMT  
		Size: 324.4 MB (324428341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee368b2b7a06b5d02dd055c7fe80dc8940a18ddf0e02a0a4d6d24702fd6f19bf`  
		Last Modified: Thu, 25 Jan 2024 01:07:47 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525e30c91f3e504a6952036ea4874a7f48f14a7a070a8d9ec8d0d7244f66599`  
		Last Modified: Thu, 25 Jan 2024 01:10:38 GMT  
		Size: 108.5 MB (108527909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:r`

```console
$ docker pull spark@sha256:d0538b8724d255fb581be15b6052fe60ed416902abb478ce5a51cc77fe806012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:11ae1a653525f2bc647252ae748638bd33486ece60ee8d4c6d3aebcf02181243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.3 MB (673332676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94366a276cfb07548758b841bdfc7c2e3eade9b32ad4cfdeb882d782823c8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 02:34:47 GMT
USER root
# Thu, 25 Jan 2024 02:42:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:42:29 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 02:42:29 GMT
USER spark
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8340527fa69c46048963b7e474423a04f8a7820f9dd84264e2b679001fde3770`  
		Last Modified: Thu, 25 Jan 2024 02:49:43 GMT  
		Size: 232.3 MB (232291183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:da719cfd5edf7833755316c985250dd6c212a905c644c4ec3f1b2ff8a2a1566b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651072477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56402184ced3231482f9147752c2c464c0525571441c1449edbb43eb1e0823d7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:47 GMT
USER root
# Thu, 25 Jan 2024 01:06:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 01:06:23 GMT
ENV R_HOME=/usr/lib/R
# Thu, 25 Jan 2024 01:06:24 GMT
USER spark
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70e9ef23be8ba509b5e0a95421570245d3eab75ec12cef236f9ffea4cc87d0e`  
		Last Modified: Thu, 25 Jan 2024 01:12:13 GMT  
		Size: 213.5 MB (213506971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:scala`

```console
$ docker pull spark@sha256:1d9b6d7857fa8685a8156668a207b667a0f40e2d1d5d3627ae8521c12318f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:e90d02425a76e48f9ac3c8bb4391799d851db5802f3c88d53264a5d4d542b227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.0 MB (441041493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c306473efd48fe73b60c75f719b488f4cc574778c9dd85b8e0f247762ec9b0a6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:34:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:34:33 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:33:08 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 02:33:08 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 02:33:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 02:33:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 02:34:33 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 02:34:34 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 02:34:34 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 02:34:34 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 02:34:34 GMT
USER spark
# Thu, 25 Jan 2024 02:34:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ea12d4b15e26af682fcff7db2c44c07d4ec61e4e2e6fca2af59f381d44a78d`  
		Last Modified: Wed, 24 Jan 2024 20:44:45 GMT  
		Size: 47.1 MB (47070433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb83f37fdd157c1a45a312fbd9b297d565861bba5f252525d0d9b6a47345d2`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda3617a74d125a49b13645110eca8516984fa5f1be65adee2df78af12e550e`  
		Last Modified: Wed, 24 Jan 2024 20:44:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf30e0dbaee3cf583ff8bb090af000534939772d2d1df724613f4ab0854663c`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d21b8725c4223a1ebe3c4d3ce3076fce38eccaf826fd822f5ee6af4b1fe`  
		Last Modified: Thu, 25 Jan 2024 02:45:31 GMT  
		Size: 24.0 MB (24034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd20f0b460b24f8665649e2627e370aab7229d58c7e6dbdd5e0e7ea2c3445cb`  
		Last Modified: Thu, 25 Jan 2024 02:45:42 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653185d0bfb02c954a494a33eb224c8a226b03d9016c1a67597dd801b063e025`  
		Last Modified: Thu, 25 Jan 2024 02:45:28 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8ee5d1e2c20192f71a30bb3a4d59caa00044a29a339406ba97ff86e5cc76df57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.6 MB (437565506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8919cf2556b77a25147f65a7a00df910ef38872d1dac662958b15f8f50821347`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:56 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 00:53:39 GMT
ARG spark_uid=185
# Thu, 25 Jan 2024 00:53:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Thu, 25 Jan 2024 00:54:09 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 00:54:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Thu, 25 Jan 2024 00:58:39 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Thu, 25 Jan 2024 00:58:39 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 25 Jan 2024 00:58:39 GMT
WORKDIR /opt/spark/work-dir
# Thu, 25 Jan 2024 00:58:39 GMT
USER spark
# Thu, 25 Jan 2024 00:58:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543f6650b69b3bee3f3e3f61edfc1914055bc8a224ee23b7e806dce4d5c4c0f`  
		Last Modified: Wed, 24 Jan 2024 20:49:51 GMT  
		Size: 45.4 MB (45398449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe86464de13c4a63218a37304fe2415dd099b19e0ef70f19f052ce4d90724`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d37719d910631e3d7c14ec2009137b7a8c5be2f1a32c2815b5922e96503a9a`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b79d56dab67c0170ef572ce73d2647d38054844483092a1887f1537932b4bf`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e28993074b5e410fe2a6776612ab2e0d6b6648b55b34a11bb9bd95aa694f66`  
		Last Modified: Thu, 25 Jan 2024 01:08:46 GMT  
		Size: 23.8 MB (23762010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8e472cc0e993174ae0b5ba9e63093283e8827e2579277d06ed47b8bb54448`  
		Last Modified: Thu, 25 Jan 2024 01:08:55 GMT  
		Size: 324.4 MB (324428408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944af86805030c6e49bb62bff7b0ef471c920145d733771ff53607319733fe`  
		Last Modified: Thu, 25 Jan 2024 01:08:43 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
