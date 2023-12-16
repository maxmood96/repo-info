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
$ docker pull spark@sha256:3adf35b5f50409d1b3c003af911bfaa364e2694f1b849fadb7bfad811c9107c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1` - linux; amd64

```console
$ docker pull spark@sha256:3b01d82f350a46331468fccdda234ab2661d531ecb9263e848c4d2a393cce9c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528776871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0e03bd9e2b74df80a07b418db077245dca8c232df1551e90d57bd1aa0bb536`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:12:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:13:00 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6131560ed4aba3d15accd8d3e77861e3716e3c3ebdeace18d15a7dd0ffabff8`  
		Last Modified: Sat, 16 Dec 2023 15:19:56 GMT  
		Size: 94.6 MB (94597381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:55d89aaf69fe0300edb3472bab3d0650031361dd27b7e5eefed11bbe53efe843
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.3 MB (518273157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3646e3c527e5a58335fb9554d8b79d3ff40611610b86e6bc538d000ddb387f`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:38:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:38:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d981aa937fc1cbe57d8db5a7e75843a8aa5e627693c83e5961b5dd157a9f09`  
		Last Modified: Sat, 16 Dec 2023 15:43:51 GMT  
		Size: 87.6 MB (87555099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-python3`

```console
$ docker pull spark@sha256:3adf35b5f50409d1b3c003af911bfaa364e2694f1b849fadb7bfad811c9107c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:3b01d82f350a46331468fccdda234ab2661d531ecb9263e848c4d2a393cce9c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528776871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0e03bd9e2b74df80a07b418db077245dca8c232df1551e90d57bd1aa0bb536`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:12:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:13:00 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6131560ed4aba3d15accd8d3e77861e3716e3c3ebdeace18d15a7dd0ffabff8`  
		Last Modified: Sat, 16 Dec 2023 15:19:56 GMT  
		Size: 94.6 MB (94597381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:55d89aaf69fe0300edb3472bab3d0650031361dd27b7e5eefed11bbe53efe843
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.3 MB (518273157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3646e3c527e5a58335fb9554d8b79d3ff40611610b86e6bc538d000ddb387f`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:38:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:38:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d981aa937fc1cbe57d8db5a7e75843a8aa5e627693c83e5961b5dd157a9f09`  
		Last Modified: Sat, 16 Dec 2023 15:43:51 GMT  
		Size: 87.6 MB (87555099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-r`

```console
$ docker pull spark@sha256:e97b687f1cc5a90b8764e69e730fd71b7f90e7aa0a8c01a3655ab6aaee89224c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-r` - linux; amd64

```console
$ docker pull spark@sha256:bbba0721f2a3ce1af5043f6eda755f9f6574348e3d4c047fe986be0c79dccf87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666471019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266aa807d2acfbf99f752bf7a5a5122900ae941b6c8d798eda734bf3896f3cdc`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:13:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:13:47 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:13:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c28000a0bdaa332a9c1b1ce3b749ff4c33874a5874cb9bfc843d9aa4384d21`  
		Last Modified: Sat, 16 Dec 2023 15:20:34 GMT  
		Size: 232.3 MB (232291529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fc32732c7513330bac0421a24131ff9ee5678227a5c6d9a282a01c4ea8b0b2ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644224438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402512bab1e4e5cad525fc2538ea094c3bd7b4a5211332223e6045f0ea547164`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:38:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:38:52 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:38:52 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc244ec4e3ad1a1ca5adbe954e3f1599ef31fa9b78384533388f0b1341312927`  
		Last Modified: Sat, 16 Dec 2023 15:44:20 GMT  
		Size: 213.5 MB (213506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala`

```console
$ docker pull spark@sha256:a78f06cb2a0b3e3d38672f74b8eb058c40387539dbb6eee65800ec93ff76dfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:f0ddc5f9373c1088c8bf66d83991db94dff3b75babbc1d0c6fdce06908ff2ce9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434179490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa3b3af2d8629f7332ab50b733fc840f5983b253d3470b6ec3d64fa338b7d2e`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49f0bc5ca1ce19f6f8a036ef0e39388571ed5c5144e09616ac495ce739cbfde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 MB (430718058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e8761fa22cc51c4f645f112f916e50e8ee6637dfc13a3fa4ceb92710ce66c`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:5cd482c89bfb489f2f94cb7eb5c70c3d7237ad6b9b91f2007670c8809c94b1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4e53f701156ad74d36dcb140ad7128f2b33005bb47bf3fbcca043756133b4c41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.1 MB (688074531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3957c751f84d3b68ed82feee69d6a129e6a533598e6f1468aed3ce8adcae0d42`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:09:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:09:55 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:09:55 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac48edccb9a8351de1f8cf9f0714b30bdf6ed8bb774f9c89ca712494b71549`  
		Last Modified: Sat, 16 Dec 2023 15:17:17 GMT  
		Size: 253.9 MB (253895041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5a9165be7d7f99c9d625232d0f0232c2f1a13ba7b1cbee2b5b660dcf314b3649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.9 MB (665854426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6850439c3e38788b5051e8ef4013c28e9f13e31cd0ad0b8f29b641b39afb94`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:35:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:35:41 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:35:41 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1331ad3c9078d2c8b7b10ec266b4be5432b84a660def97ad488969e7f36c8da0`  
		Last Modified: Sat, 16 Dec 2023 15:41:40 GMT  
		Size: 235.1 MB (235136368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:3adf35b5f50409d1b3c003af911bfaa364e2694f1b849fadb7bfad811c9107c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3b01d82f350a46331468fccdda234ab2661d531ecb9263e848c4d2a393cce9c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528776871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0e03bd9e2b74df80a07b418db077245dca8c232df1551e90d57bd1aa0bb536`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:12:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:13:00 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6131560ed4aba3d15accd8d3e77861e3716e3c3ebdeace18d15a7dd0ffabff8`  
		Last Modified: Sat, 16 Dec 2023 15:19:56 GMT  
		Size: 94.6 MB (94597381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:55d89aaf69fe0300edb3472bab3d0650031361dd27b7e5eefed11bbe53efe843
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.3 MB (518273157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3646e3c527e5a58335fb9554d8b79d3ff40611610b86e6bc538d000ddb387f`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:38:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:38:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d981aa937fc1cbe57d8db5a7e75843a8aa5e627693c83e5961b5dd157a9f09`  
		Last Modified: Sat, 16 Dec 2023 15:43:51 GMT  
		Size: 87.6 MB (87555099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:e97b687f1cc5a90b8764e69e730fd71b7f90e7aa0a8c01a3655ab6aaee89224c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bbba0721f2a3ce1af5043f6eda755f9f6574348e3d4c047fe986be0c79dccf87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666471019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266aa807d2acfbf99f752bf7a5a5122900ae941b6c8d798eda734bf3896f3cdc`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:09:04 GMT
USER root
# Sat, 16 Dec 2023 15:13:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:13:47 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:13:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c28000a0bdaa332a9c1b1ce3b749ff4c33874a5874cb9bfc843d9aa4384d21`  
		Last Modified: Sat, 16 Dec 2023 15:20:34 GMT  
		Size: 232.3 MB (232291529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fc32732c7513330bac0421a24131ff9ee5678227a5c6d9a282a01c4ea8b0b2ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644224438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402512bab1e4e5cad525fc2538ea094c3bd7b4a5211332223e6045f0ea547164`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:34:59 GMT
USER root
# Sat, 16 Dec 2023 15:38:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:38:52 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:38:52 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc244ec4e3ad1a1ca5adbe954e3f1599ef31fa9b78384533388f0b1341312927`  
		Last Modified: Sat, 16 Dec 2023 15:44:20 GMT  
		Size: 213.5 MB (213506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.4.1-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:a78f06cb2a0b3e3d38672f74b8eb058c40387539dbb6eee65800ec93ff76dfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:f0ddc5f9373c1088c8bf66d83991db94dff3b75babbc1d0c6fdce06908ff2ce9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434179490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa3b3af2d8629f7332ab50b733fc840f5983b253d3470b6ec3d64fa338b7d2e`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:54 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:08:56 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:08:57 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:08:57 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:08:57 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:08:57 GMT
USER spark
# Sat, 16 Dec 2023 15:08:57 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09e507cae6283502087b71d45803bd1009b3ee5bd401ef29c98f0529529fb09`  
		Last Modified: Sat, 16 Dec 2023 15:16:39 GMT  
		Size: 317.9 MB (317886722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de330cd0b25839260093a935746f8dbdb809617cee148910fc93e7a994c533c1`  
		Last Modified: Sat, 16 Dec 2023 15:16:25 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49f0bc5ca1ce19f6f8a036ef0e39388571ed5c5144e09616ac495ce739cbfde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 MB (430718058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e8761fa22cc51c4f645f112f916e50e8ee6637dfc13a3fa4ceb92710ce66c`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:49 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sat, 16 Dec 2023 15:34:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:34:49 GMT
COPY file:01f69f91109a74812cb83cbe729877b82d879c4c4634d429eef0305a59878741 in /opt/ 
# Sat, 16 Dec 2023 15:34:49 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:34:49 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:34:49 GMT
USER spark
# Sat, 16 Dec 2023 15:34:49 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341c06d5ef0a9ad2ba0582a65082d2f5ed9897ae99fdf5b939ed3323d2de0f3`  
		Last Modified: Sat, 16 Dec 2023 15:41:09 GMT  
		Size: 317.9 MB (317886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d361b3f64559dad32d15b43c21bd03a6b779f7f0e6d76faf039ae47402170f2`  
		Last Modified: Sat, 16 Dec 2023 15:40:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0`

```console
$ docker pull spark@sha256:6c38d88ffe68da6cba1b89ce87b9bdda140c8e8a860d9ccbea636defb8375bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0` - linux; amd64

```console
$ docker pull spark@sha256:3d9421fad17d881162732e32e3485dbf6555f44ee9891098e6514cfe16bb2e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535318479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62829cbf8e129a9c57bb72b10674f621e9b82635e311ed678994321d9b3dbf`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:11:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a6d4fb04bd7c6c4602ca25d57414eb902b7477ad6799bc1b9545cf4c728a8`  
		Last Modified: Sat, 16 Dec 2023 15:18:50 GMT  
		Size: 94.6 MB (94597297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8146ff1f03bf71acbc33de07bc05233bfd3e88acb8065f59cff9ab867108ad4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.8 MB (524814565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f855f35df1d0419c06b81a3017649f9f2b0c1c65e1d4fe1df8b59157ac67ba`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e01694674b2c8c4fb4ade623ec9339da9dd1c8b918d26318ec4a72e1464272`  
		Last Modified: Sat, 16 Dec 2023 15:42:56 GMT  
		Size: 87.6 MB (87554826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17`

```console
$ docker pull spark@sha256:45434200f1ee61f97e923853abdfa604ed3f5ec62a1233df15bd832f53951bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17` - linux; amd64

```console
$ docker pull spark@sha256:cb3845d130e4939a9db01bea457d1b8e529c72114dd899bf148bef12dbd4532d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558257546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e4ae51a967eb61bb0028d0c6ed864bec154f67419137846692fd07c1ce612`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:10:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:10:23 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8042fed2c4284b581e7f4c215ed6de85e1eb2ab8c7b8f2d03dc93c73d440cde2`  
		Last Modified: Sat, 16 Dec 2023 15:17:39 GMT  
		Size: 114.0 MB (113962831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:23903c7cc06b0ee4984f1529875e81a06da2ed22b8e4910221300856426262e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551297888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5a07c12b767ea05f9fa4a26953c9bb0643ef5af6d3993cad4dfb47dd80e299`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:06 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910f1bc2926dc144f57f82a7e01fa90e74fc76605782cf79bf5cd4d508f562d4`  
		Last Modified: Sat, 16 Dec 2023 15:41:58 GMT  
		Size: 108.5 MB (108528468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-python3`

```console
$ docker pull spark@sha256:45434200f1ee61f97e923853abdfa604ed3f5ec62a1233df15bd832f53951bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:cb3845d130e4939a9db01bea457d1b8e529c72114dd899bf148bef12dbd4532d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558257546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e4ae51a967eb61bb0028d0c6ed864bec154f67419137846692fd07c1ce612`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:10:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:10:23 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8042fed2c4284b581e7f4c215ed6de85e1eb2ab8c7b8f2d03dc93c73d440cde2`  
		Last Modified: Sat, 16 Dec 2023 15:17:39 GMT  
		Size: 114.0 MB (113962831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:23903c7cc06b0ee4984f1529875e81a06da2ed22b8e4910221300856426262e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551297888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5a07c12b767ea05f9fa4a26953c9bb0643ef5af6d3993cad4dfb47dd80e299`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:06 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910f1bc2926dc144f57f82a7e01fa90e74fc76605782cf79bf5cd4d508f562d4`  
		Last Modified: Sat, 16 Dec 2023 15:41:58 GMT  
		Size: 108.5 MB (108528468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-r`

```console
$ docker pull spark@sha256:63e840a966f1ff7493aa0b2d9915ce93e5577989b4482afb74f69bf4e12e48c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:6115cc7ec18c24c22cacadaee40b0a53a0fad3cd5c503b581ec75c0df88c2405
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **762.7 MB (762706246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eea1bae7b93be6708d3c627c808693bb0cade24d161a2a24891b6392244f392`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:11:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:15 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:11:15 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc8e50972bec4e5d3a9c92a81d454869187cd34cd4bf4f2f062d95523637a5`  
		Last Modified: Sat, 16 Dec 2023 15:18:28 GMT  
		Size: 318.4 MB (318411531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a9adcc96997a923e5954966230a414b36f637f19e325e06893510c8871b9ca23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.3 MB (744312573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3384efbae43e44abcb3ce0f22364e3e4158ae630a42bee3a915815a8c7b379`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:54 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:36:55 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac674b081ff78d3b38862dfba8de24e138cf1c8d38e1efea833775d3eda7db5`  
		Last Modified: Sat, 16 Dec 2023 15:42:37 GMT  
		Size: 301.5 MB (301543153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-java17-scala`

```console
$ docker pull spark@sha256:521e1fbbeb3d499257fce1d29b875a37f965a99905ee6db0e63b720e29344835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:1aab976a969919c33299469f6dc3b110b506b5b6d4f815517bb44142baddc935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444294715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89338a3a3c1fe10a7e8fa3bc4b77a5e5347bcc5f8b926738f89d67c1c031247`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:24b1b65ec14bd1df837594aba28d6cb24722bf95eaab2cababc5d11c909c1a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.8 MB (442769420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfd25ff18fec75c86ed76dc1d88c9d585c40dcb9350cd8fc53bda5bda09ba9d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-python3`

```console
$ docker pull spark@sha256:6c38d88ffe68da6cba1b89ce87b9bdda140c8e8a860d9ccbea636defb8375bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-python3` - linux; amd64

```console
$ docker pull spark@sha256:3d9421fad17d881162732e32e3485dbf6555f44ee9891098e6514cfe16bb2e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535318479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62829cbf8e129a9c57bb72b10674f621e9b82635e311ed678994321d9b3dbf`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:11:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a6d4fb04bd7c6c4602ca25d57414eb902b7477ad6799bc1b9545cf4c728a8`  
		Last Modified: Sat, 16 Dec 2023 15:18:50 GMT  
		Size: 94.6 MB (94597297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8146ff1f03bf71acbc33de07bc05233bfd3e88acb8065f59cff9ab867108ad4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.8 MB (524814565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f855f35df1d0419c06b81a3017649f9f2b0c1c65e1d4fe1df8b59157ac67ba`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e01694674b2c8c4fb4ade623ec9339da9dd1c8b918d26318ec4a72e1464272`  
		Last Modified: Sat, 16 Dec 2023 15:42:56 GMT  
		Size: 87.6 MB (87554826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-r`

```console
$ docker pull spark@sha256:c299b13fad5b38f29fe13bfe32fcc2dd75e75d8ac2e6cadf3ee163232649f6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-r` - linux; amd64

```console
$ docker pull spark@sha256:29560930e6dd00c933202b2966fbde5302620c0a68d668834d81eb225b062317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.0 MB (673012454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a9ca4a56b0d494e1ad70f94354c6d93b89dd2fc0134ea4f7192540e060a27`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:12:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:12:32 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:12:32 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ef7e94c6f43dc0815f513a95d4f211bb32ee57e7cd860b18639726bead7ba3`  
		Last Modified: Sat, 16 Dec 2023 15:19:32 GMT  
		Size: 232.3 MB (232291272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8d32cfb7c09086304cc55bd6b413a1cc3a33150081138739e9508c2c19d593cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650765835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29a5977dca19ed1f24c09c1997f65e642311f76e7f71434b1e6f57c69c59901`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:54 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:37:54 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a0653de496ad67c37233d3c897c90445263406549b3ef4d81fc14fed459f27`  
		Last Modified: Sat, 16 Dec 2023 15:43:30 GMT  
		Size: 213.5 MB (213506096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala`

```console
$ docker pull spark@sha256:8b1e5dc8c6a101e82627f721f388ad791e1e918bc91c3c789760ddc6da3918af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala` - linux; amd64

```console
$ docker pull spark@sha256:b0f4a41645c8fa0881d37d17532cc429910b734b3c5f95622d6db55ce54c317d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.7 MB (440721182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55625ddbf4c5f36681876b8f74cfbc0fa7e009b8922b30d5cf0530ea1233f883`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ace88c6ae0164d3a75f23ebb1cbc84c14365b94a5f7fa3b7e5ad67a1b6a3e4b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437259739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cd7b76ddb5fae9058ce840bc40c4e619f0525ea3d7ce56e5ef98e4c39ce2a6`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:67822fdd17f7aa4c3dcd3eeb3a60a60b7b01c2c3a3245d3d3460c1a8274ad6f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a128a762120ca254650ee02995a758167427367f3a7313b4978438734cf92c41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.6 MB (694616760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7880ac3e9620d475be2051e096c4b7fd0a33efbcae70b1880de44ae12e8ae9`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:07:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:07:49 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:07:49 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4049857f6e285c06de8cbde7a04569a22950f986cb6d73d744ee5e2a87e4d238`  
		Last Modified: Sat, 16 Dec 2023 15:16:18 GMT  
		Size: 253.9 MB (253895578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:af010ea5ecdb76cb8e558711adb36f3cbe553d8a0002d9e9ceea464bc07de831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.4 MB (672396824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1132ef5d04d1cbedcde25e73e41dad759ed839697d4a253cbc7e676198d0ea94`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:33:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:33:37 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:33:37 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff5a7a68d5933ef4bd3159ec3a131db2b8c425c3d46bee4af0237d976842369`  
		Last Modified: Sat, 16 Dec 2023 15:40:52 GMT  
		Size: 235.1 MB (235137085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:6c38d88ffe68da6cba1b89ce87b9bdda140c8e8a860d9ccbea636defb8375bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3d9421fad17d881162732e32e3485dbf6555f44ee9891098e6514cfe16bb2e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535318479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62829cbf8e129a9c57bb72b10674f621e9b82635e311ed678994321d9b3dbf`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:11:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a6d4fb04bd7c6c4602ca25d57414eb902b7477ad6799bc1b9545cf4c728a8`  
		Last Modified: Sat, 16 Dec 2023 15:18:50 GMT  
		Size: 94.6 MB (94597297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8146ff1f03bf71acbc33de07bc05233bfd3e88acb8065f59cff9ab867108ad4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.8 MB (524814565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f855f35df1d0419c06b81a3017649f9f2b0c1c65e1d4fe1df8b59157ac67ba`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e01694674b2c8c4fb4ade623ec9339da9dd1c8b918d26318ec4a72e1464272`  
		Last Modified: Sat, 16 Dec 2023 15:42:56 GMT  
		Size: 87.6 MB (87554826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:c299b13fad5b38f29fe13bfe32fcc2dd75e75d8ac2e6cadf3ee163232649f6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:29560930e6dd00c933202b2966fbde5302620c0a68d668834d81eb225b062317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.0 MB (673012454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a9ca4a56b0d494e1ad70f94354c6d93b89dd2fc0134ea4f7192540e060a27`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:12:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:12:32 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:12:32 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ef7e94c6f43dc0815f513a95d4f211bb32ee57e7cd860b18639726bead7ba3`  
		Last Modified: Sat, 16 Dec 2023 15:19:32 GMT  
		Size: 232.3 MB (232291272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8d32cfb7c09086304cc55bd6b413a1cc3a33150081138739e9508c2c19d593cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650765835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29a5977dca19ed1f24c09c1997f65e642311f76e7f71434b1e6f57c69c59901`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:54 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:37:54 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a0653de496ad67c37233d3c897c90445263406549b3ef4d81fc14fed459f27`  
		Last Modified: Sat, 16 Dec 2023 15:43:30 GMT  
		Size: 213.5 MB (213506096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:8b1e5dc8c6a101e82627f721f388ad791e1e918bc91c3c789760ddc6da3918af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:b0f4a41645c8fa0881d37d17532cc429910b734b3c5f95622d6db55ce54c317d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.7 MB (440721182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55625ddbf4c5f36681876b8f74cfbc0fa7e009b8922b30d5cf0530ea1233f883`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ace88c6ae0164d3a75f23ebb1cbc84c14365b94a5f7fa3b7e5ad67a1b6a3e4b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437259739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cd7b76ddb5fae9058ce840bc40c4e619f0525ea3d7ce56e5ef98e4c39ce2a6`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:9ca72409861a47faccb342d5ef668b4f51cefd2cce72dd3243ab491476f4ae29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a573bc2f6886d4bfb60603d33c20271d6ac196c28255f2f726ec51d66296f54b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.4 MB (777423875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cb5da05730df21110f11cf9511480c731eee00b512430c0fa37c27fdf74631`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:03:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:03:22 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:03:22 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3692d0376fbf3d9b38855d9acbab9c27a289df552db20d644027e3090e725401`  
		Last Modified: Sat, 16 Dec 2023 15:15:13 GMT  
		Size: 333.1 MB (333129160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:87699cc7d6c549e7882cf9fdcde51f6e0061bd85df566f83afcb3ab050928092
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 MB (758863790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadf24816d84ae7f7a6bccfb92255f2cf714ade08923a53884d8e7712a427f18`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:29:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:14 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:29:14 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbd9b1c0108f33928f880d05d84e46d9e8dd77eee52888f10020578fabcb3c8`  
		Last Modified: Sat, 16 Dec 2023 15:40:02 GMT  
		Size: 316.1 MB (316094370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:45434200f1ee61f97e923853abdfa604ed3f5ec62a1233df15bd832f53951bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:cb3845d130e4939a9db01bea457d1b8e529c72114dd899bf148bef12dbd4532d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558257546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e4ae51a967eb61bb0028d0c6ed864bec154f67419137846692fd07c1ce612`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:10:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:10:23 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8042fed2c4284b581e7f4c215ed6de85e1eb2ab8c7b8f2d03dc93c73d440cde2`  
		Last Modified: Sat, 16 Dec 2023 15:17:39 GMT  
		Size: 114.0 MB (113962831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:23903c7cc06b0ee4984f1529875e81a06da2ed22b8e4910221300856426262e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551297888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5a07c12b767ea05f9fa4a26953c9bb0643ef5af6d3993cad4dfb47dd80e299`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:06 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910f1bc2926dc144f57f82a7e01fa90e74fc76605782cf79bf5cd4d508f562d4`  
		Last Modified: Sat, 16 Dec 2023 15:41:58 GMT  
		Size: 108.5 MB (108528468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:63e840a966f1ff7493aa0b2d9915ce93e5577989b4482afb74f69bf4e12e48c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6115cc7ec18c24c22cacadaee40b0a53a0fad3cd5c503b581ec75c0df88c2405
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **762.7 MB (762706246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eea1bae7b93be6708d3c627c808693bb0cade24d161a2a24891b6392244f392`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:11:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:15 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:11:15 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc8e50972bec4e5d3a9c92a81d454869187cd34cd4bf4f2f062d95523637a5`  
		Last Modified: Sat, 16 Dec 2023 15:18:28 GMT  
		Size: 318.4 MB (318411531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a9adcc96997a923e5954966230a414b36f637f19e325e06893510c8871b9ca23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.3 MB (744312573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3384efbae43e44abcb3ce0f22364e3e4158ae630a42bee3a915815a8c7b379`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:54 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:36:55 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac674b081ff78d3b38862dfba8de24e138cf1c8d38e1efea833775d3eda7db5`  
		Last Modified: Sat, 16 Dec 2023 15:42:37 GMT  
		Size: 301.5 MB (301543153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:3.5.0-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:521e1fbbeb3d499257fce1d29b875a37f965a99905ee6db0e63b720e29344835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:1aab976a969919c33299469f6dc3b110b506b5b6d4f815517bb44142baddc935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444294715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89338a3a3c1fe10a7e8fa3bc4b77a5e5347bcc5f8b926738f89d67c1c031247`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:24b1b65ec14bd1df837594aba28d6cb24722bf95eaab2cababc5d11c909c1a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.8 MB (442769420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfd25ff18fec75c86ed76dc1d88c9d585c40dcb9350cd8fc53bda5bda09ba9d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:latest`

```console
$ docker pull spark@sha256:6c38d88ffe68da6cba1b89ce87b9bdda140c8e8a860d9ccbea636defb8375bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:3d9421fad17d881162732e32e3485dbf6555f44ee9891098e6514cfe16bb2e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535318479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62829cbf8e129a9c57bb72b10674f621e9b82635e311ed678994321d9b3dbf`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:11:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a6d4fb04bd7c6c4602ca25d57414eb902b7477ad6799bc1b9545cf4c728a8`  
		Last Modified: Sat, 16 Dec 2023 15:18:50 GMT  
		Size: 94.6 MB (94597297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8146ff1f03bf71acbc33de07bc05233bfd3e88acb8065f59cff9ab867108ad4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.8 MB (524814565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f855f35df1d0419c06b81a3017649f9f2b0c1c65e1d4fe1df8b59157ac67ba`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e01694674b2c8c4fb4ade623ec9339da9dd1c8b918d26318ec4a72e1464272`  
		Last Modified: Sat, 16 Dec 2023 15:42:56 GMT  
		Size: 87.6 MB (87554826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:python3`

```console
$ docker pull spark@sha256:6c38d88ffe68da6cba1b89ce87b9bdda140c8e8a860d9ccbea636defb8375bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:3d9421fad17d881162732e32e3485dbf6555f44ee9891098e6514cfe16bb2e10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535318479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62829cbf8e129a9c57bb72b10674f621e9b82635e311ed678994321d9b3dbf`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:11:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:11:47 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a6d4fb04bd7c6c4602ca25d57414eb902b7477ad6799bc1b9545cf4c728a8`  
		Last Modified: Sat, 16 Dec 2023 15:18:50 GMT  
		Size: 94.6 MB (94597297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8146ff1f03bf71acbc33de07bc05233bfd3e88acb8065f59cff9ab867108ad4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.8 MB (524814565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f855f35df1d0419c06b81a3017649f9f2b0c1c65e1d4fe1df8b59157ac67ba`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:14 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e01694674b2c8c4fb4ade623ec9339da9dd1c8b918d26318ec4a72e1464272`  
		Last Modified: Sat, 16 Dec 2023 15:42:56 GMT  
		Size: 87.6 MB (87554826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:python3-java17`

```console
$ docker pull spark@sha256:45434200f1ee61f97e923853abdfa604ed3f5ec62a1233df15bd832f53951bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:cb3845d130e4939a9db01bea457d1b8e529c72114dd899bf148bef12dbd4532d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.3 MB (558257546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e4ae51a967eb61bb0028d0c6ed864bec154f67419137846692fd07c1ce612`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:34 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 14:58:35 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 14:58:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:58:51 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 14:59:50 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 14:59:51 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 14:59:51 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 14:59:51 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 14:59:51 GMT
USER spark
# Sat, 16 Dec 2023 14:59:51 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 14:59:58 GMT
USER root
# Sat, 16 Dec 2023 15:10:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:10:23 GMT
USER spark
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57117148c11ecbb2f167284da58ab4f78f87d356d6cde4c2ea5934b301f167e`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83494de259b6ee581252a13defac70925bc7b142f8669f3a973a01bca42a46ed`  
		Last Modified: Sat, 16 Dec 2023 15:14:15 GMT  
		Size: 24.8 MB (24809842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb293eebe7dd607ed760e4f00f67540672f6a100f42f248c54dcd9f40fba15e`  
		Last Modified: Sat, 16 Dec 2023 15:14:25 GMT  
		Size: 324.4 MB (324428362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84866bc64e88951e66437bb9fcaaa051db816850c840caf3914bae4129864055`  
		Last Modified: Sat, 16 Dec 2023 15:14:11 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8042fed2c4284b581e7f4c215ed6de85e1eb2ab8c7b8f2d03dc93c73d440cde2`  
		Last Modified: Sat, 16 Dec 2023 15:17:39 GMT  
		Size: 114.0 MB (113962831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:23903c7cc06b0ee4984f1529875e81a06da2ed22b8e4910221300856426262e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551297888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5a07c12b767ea05f9fa4a26953c9bb0643ef5af6d3993cad4dfb47dd80e299`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:24:03 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:24:04 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:24:21 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:24:22 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:25:22 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:25:24 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:25:24 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:25:24 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:25:25 GMT
USER spark
# Sat, 16 Dec 2023 15:25:25 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:25:41 GMT
USER root
# Sat, 16 Dec 2023 15:36:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:36:06 GMT
USER spark
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a422b5ab768fe61690e4590ee179b9a73d75fecac7cdffbbfb7fe29ba60573`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12273f4d1b216e332be2e6e0ec53fb10b74810839e6f2a8689a2351b585a6fc4`  
		Last Modified: Sat, 16 Dec 2023 15:39:16 GMT  
		Size: 24.5 MB (24454408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b138261b24da3cb33d946d685327ae834e704288510a8819496ba4efcf6b2c4`  
		Last Modified: Sat, 16 Dec 2023 15:39:25 GMT  
		Size: 324.4 MB (324428406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c30c661099c6d3736f252152c187e1612333a380d738cd815c33b9f1c48f79`  
		Last Modified: Sat, 16 Dec 2023 15:39:14 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910f1bc2926dc144f57f82a7e01fa90e74fc76605782cf79bf5cd4d508f562d4`  
		Last Modified: Sat, 16 Dec 2023 15:41:58 GMT  
		Size: 108.5 MB (108528468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:r`

```console
$ docker pull spark@sha256:c299b13fad5b38f29fe13bfe32fcc2dd75e75d8ac2e6cadf3ee163232649f6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:29560930e6dd00c933202b2966fbde5302620c0a68d668834d81eb225b062317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.0 MB (673012454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a9ca4a56b0d494e1ad70f94354c6d93b89dd2fc0134ea4f7192540e060a27`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:05:16 GMT
USER root
# Sat, 16 Dec 2023 15:12:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:12:32 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:12:32 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ef7e94c6f43dc0815f513a95d4f211bb32ee57e7cd860b18639726bead7ba3`  
		Last Modified: Sat, 16 Dec 2023 15:19:32 GMT  
		Size: 232.3 MB (232291272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8d32cfb7c09086304cc55bd6b413a1cc3a33150081138739e9508c2c19d593cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650765835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29a5977dca19ed1f24c09c1997f65e642311f76e7f71434b1e6f57c69c59901`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sat, 16 Dec 2023 15:30:57 GMT
USER root
# Sat, 16 Dec 2023 15:37:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:37:54 GMT
ENV R_HOME=/usr/lib/R
# Sat, 16 Dec 2023 15:37:54 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a0653de496ad67c37233d3c897c90445263406549b3ef4d81fc14fed459f27`  
		Last Modified: Sat, 16 Dec 2023 15:43:30 GMT  
		Size: 213.5 MB (213506096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spark:scala`

```console
$ docker pull spark@sha256:8b1e5dc8c6a101e82627f721f388ad791e1e918bc91c3c789760ddc6da3918af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:b0f4a41645c8fa0881d37d17532cc429910b734b3c5f95622d6db55ce54c317d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.7 MB (440721182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55625ddbf4c5f36681876b8f74cfbc0fa7e009b8922b30d5cf0530ea1233f883`
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
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:37 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:03:37 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:04:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:04:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:05:05 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:05:05 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:05:05 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:05:06 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:05:06 GMT
USER spark
# Sat, 16 Dec 2023 15:05:06 GMT
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
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a364530a5e1cbfe9a41f50716d93e9695abd720edb5daa737977f6d5cfaab5b9`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a2e1ed666dda4afdce57887d677ceeeb8ce926e7b384158f731600328c1ef`  
		Last Modified: Sat, 16 Dec 2023 15:15:24 GMT  
		Size: 23.7 MB (23715642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7142fb97c8cd8614c0f2c8571e70195625deaeeb9b6d27f1fcb0dd1199f81c5e`  
		Last Modified: Sat, 16 Dec 2023 15:15:34 GMT  
		Size: 324.4 MB (324428361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5776a21767e177ea7b0db65ab1164abbbd7c64063a4dfd8192d8fcec8817f1`  
		Last Modified: Sat, 16 Dec 2023 15:15:20 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ace88c6ae0164d3a75f23ebb1cbc84c14365b94a5f7fa3b7e5ad67a1b6a3e4b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437259739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cd7b76ddb5fae9058ce840bc40c4e619f0525ea3d7ce56e5ef98e4c39ce2a6`
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
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:29:19 GMT
ARG spark_uid=185
# Sat, 16 Dec 2023 15:29:19 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark
# Sat, 16 Dec 2023 15:29:45 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:29:45 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Sat, 16 Dec 2023 15:30:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP";
# Sat, 16 Dec 2023 15:30:50 GMT
COPY file:b1ecb91165fbd66c0d3cfad8d169bf4914b1cf964de586096e80f8b5ca8b3b12 in /opt/ 
# Sat, 16 Dec 2023 15:30:50 GMT
ENV SPARK_HOME=/opt/spark
# Sat, 16 Dec 2023 15:30:50 GMT
WORKDIR /opt/spark/work-dir
# Sat, 16 Dec 2023 15:30:50 GMT
USER spark
# Sat, 16 Dec 2023 15:30:50 GMT
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
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4d2f6410befe09626d1237fd7e7601279940858d84d3cba118b26e2bdfaec`  
		Last Modified: Sat, 16 Dec 2023 15:40:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628ba73dac016be3a7ebe880ea99127206e168b9adff73cc946d905524a4a40`  
		Last Modified: Sat, 16 Dec 2023 15:40:12 GMT  
		Size: 23.5 MB (23453721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714ac870e2cd916de73c3b8f51696ebc32e830bb209ee1e9774ebe345301b54`  
		Last Modified: Sat, 16 Dec 2023 15:40:21 GMT  
		Size: 324.4 MB (324428360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb88d7832876710c7f32f02119a7a278024ae13b40e47e575bc60f7921f9a3e`  
		Last Modified: Sat, 16 Dec 2023 15:40:09 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
