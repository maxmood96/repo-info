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
-	[`spark:3.5.1`](#spark351)
-	[`spark:3.5.1-java17`](#spark351-java17)
-	[`spark:3.5.1-java17-python3`](#spark351-java17-python3)
-	[`spark:3.5.1-java17-r`](#spark351-java17-r)
-	[`spark:3.5.1-java17-scala`](#spark351-java17-scala)
-	[`spark:3.5.1-python3`](#spark351-python3)
-	[`spark:3.5.1-r`](#spark351-r)
-	[`spark:3.5.1-scala`](#spark351-scala)
-	[`spark:3.5.1-scala2.12-java11-python3-r-ubuntu`](#spark351-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.1-scala2.12-java11-python3-ubuntu`](#spark351-scala212-java11-python3-ubuntu)
-	[`spark:3.5.1-scala2.12-java11-r-ubuntu`](#spark351-scala212-java11-r-ubuntu)
-	[`spark:3.5.1-scala2.12-java11-ubuntu`](#spark351-scala212-java11-ubuntu)
-	[`spark:3.5.1-scala2.12-java17-python3-r-ubuntu`](#spark351-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.1-scala2.12-java17-python3-ubuntu`](#spark351-scala212-java17-python3-ubuntu)
-	[`spark:3.5.1-scala2.12-java17-r-ubuntu`](#spark351-scala212-java17-r-ubuntu)
-	[`spark:3.5.1-scala2.12-java17-ubuntu`](#spark351-scala212-java17-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.4.1`

```console
$ docker pull spark@sha256:b4e931157e7b1e4c99d51c688875ee5dcfb6374907b1d1f3b435eebc2e9617a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1` - linux; amd64

```console
$ docker pull spark@sha256:92cf6331357019ca7fce03339485bfcb1bd15f9503ff1c90fffa126e11c8b379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529251178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3410172c418b27b3a4c8b11f47527841488850265ac9a2d6fb12fe6d0b9d2b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4fd2553b3cde3dc44739465863143422ef027b3e2ccf8fdad2ca285146761a`  
		Last Modified: Wed, 24 Jul 2024 04:04:19 GMT  
		Size: 94.4 MB (94379162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1` - unknown; unknown

```console
$ docker pull spark@sha256:72dc719ed84fe58d62c783ec530ba5844462b13a4d93efe223a4da723f345394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d11a1b5f7a10a5fe3a5a473ac828d1fbbe70a0127fba401adf8bd23ef6303`

```dockerfile
```

-	Layers:
	-	`sha256:830415755c1bcd381a9c3fad26dc08a6d830e790e968e596697d874f1b661d0c`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55fa4c8501c9f600c923c418fc382084759f9b64a1ecb9df30170c5895aad3`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae519d0087b6683ef6d6cb801f8872a82d20e37ab4c0495bd8bd97353aa28b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518763016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8230039c143ef46af79079b4ecabea25b437d7bf5b648505a090961afa093f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ccf3d89f6526886cfd3e83a15ac470caf5fe772c267292076312e1e0053d50`  
		Last Modified: Wed, 24 Jul 2024 17:51:50 GMT  
		Size: 87.3 MB (87328333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1` - unknown; unknown

```console
$ docker pull spark@sha256:a4bb7dd9f74b59b6dddc550ab3519aa7e3de111320995687dc78ecc2daaabda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd618ddab4afcff86e29050ed9ca88ca2a90ded4d38f09f0a201f46e2b75386`

```dockerfile
```

-	Layers:
	-	`sha256:84caf195619d750eba5ca8a279087555fac40f2896bc0e47597208d9c849fe1f`  
		Last Modified: Wed, 24 Jul 2024 17:51:49 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e8c16e2ac2e9e44f1a74315a1af747890a2698e1adf8d6830217b3047ce315`  
		Last Modified: Wed, 24 Jul 2024 17:51:48 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-python3`

```console
$ docker pull spark@sha256:b4e931157e7b1e4c99d51c688875ee5dcfb6374907b1d1f3b435eebc2e9617a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:92cf6331357019ca7fce03339485bfcb1bd15f9503ff1c90fffa126e11c8b379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529251178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3410172c418b27b3a4c8b11f47527841488850265ac9a2d6fb12fe6d0b9d2b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4fd2553b3cde3dc44739465863143422ef027b3e2ccf8fdad2ca285146761a`  
		Last Modified: Wed, 24 Jul 2024 04:04:19 GMT  
		Size: 94.4 MB (94379162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:72dc719ed84fe58d62c783ec530ba5844462b13a4d93efe223a4da723f345394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d11a1b5f7a10a5fe3a5a473ac828d1fbbe70a0127fba401adf8bd23ef6303`

```dockerfile
```

-	Layers:
	-	`sha256:830415755c1bcd381a9c3fad26dc08a6d830e790e968e596697d874f1b661d0c`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55fa4c8501c9f600c923c418fc382084759f9b64a1ecb9df30170c5895aad3`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae519d0087b6683ef6d6cb801f8872a82d20e37ab4c0495bd8bd97353aa28b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518763016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8230039c143ef46af79079b4ecabea25b437d7bf5b648505a090961afa093f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ccf3d89f6526886cfd3e83a15ac470caf5fe772c267292076312e1e0053d50`  
		Last Modified: Wed, 24 Jul 2024 17:51:50 GMT  
		Size: 87.3 MB (87328333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:a4bb7dd9f74b59b6dddc550ab3519aa7e3de111320995687dc78ecc2daaabda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd618ddab4afcff86e29050ed9ca88ca2a90ded4d38f09f0a201f46e2b75386`

```dockerfile
```

-	Layers:
	-	`sha256:84caf195619d750eba5ca8a279087555fac40f2896bc0e47597208d9c849fe1f`  
		Last Modified: Wed, 24 Jul 2024 17:51:49 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e8c16e2ac2e9e44f1a74315a1af747890a2698e1adf8d6830217b3047ce315`  
		Last Modified: Wed, 24 Jul 2024 17:51:48 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-r`

```console
$ docker pull spark@sha256:c4a5c55b0473f200c974ded22c5ca722cbcd7a31f572ed9ad177956ffa794201
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-r` - linux; amd64

```console
$ docker pull spark@sha256:b734c4736598f277b4479e08be1563cd8f93873879e7c6fd4642a920e964220b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 MB (667183022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae7f7b58ff6b61d186eb2956b5c09a3af6e28c5efb9da281f81493e6aebc48`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab41794466d719760f1ff9d0f7e68f1e9213be1cc4c13981a0fd4bdf927f72`  
		Last Modified: Wed, 24 Jul 2024 04:05:02 GMT  
		Size: 232.3 MB (232311006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:2256bcff13d74704e8eecee9ed3c30c4cab6acea1863103bd7571abff8bcc205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11094499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c282a044ea2134ab5a11d74f78feca9eca1a46ab4468fd7c7248d8fbef902255`

```dockerfile
```

-	Layers:
	-	`sha256:4e67ae10cd145cac3e07151a68abb4c830d4c25efcce650ef4cbbccad53a878b`  
		Last Modified: Wed, 24 Jul 2024 04:04:57 GMT  
		Size: 11.1 MB (11083868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc0201e90504fef514e2bca3958b809ee5e5dfa6a82d3627628676514717aa9`  
		Last Modified: Wed, 24 Jul 2024 04:04:57 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8287d99fd7223b0a247857754d269322c5a465e3ca70fcf03d4904bb95b4caf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.0 MB (644957514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3717ad3f72288f9aa98ee5100cee13e8a091ffebf6454f952bb546ec52a94421`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e7971174086bb160310e1756d2726077417678924080cda7c751b224dadf14`  
		Last Modified: Wed, 24 Jul 2024 17:53:33 GMT  
		Size: 213.5 MB (213522831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:528a4785a1300660dde901e07a5d6e0319820d3f5fd9974c2b8613b5002f01f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11079386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dd0a7931c75796539003313d23d72fa40c475cc270ee980952bd4060ba910f`

```dockerfile
```

-	Layers:
	-	`sha256:9b874b5e7dcb890c035cf4d68ccc2b05f9a2b8e04ccf44639a1b72a937b1ebd4`  
		Last Modified: Wed, 24 Jul 2024 17:53:29 GMT  
		Size: 11.1 MB (11068333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203e1bc82995131c66fac9ab803b27256e21bd6554755bae4562aa39f07b96f8`  
		Last Modified: Wed, 24 Jul 2024 17:53:28 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala`

```console
$ docker pull spark@sha256:9ffbf0a288fe3e045aa5fc550e3af2762f840bc8b3908ef3c530b46ebdfa4cfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:3061dc1c1052c04ddab9f884ff2fe4cb771162bf3c8abe80eea409c24f0daa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434872016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7511b6075fcb3345f4eea620b5770eed460505f261cc993b0f8fd14acdc2ea`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:aeb8a3fc32a0b6930ae2c7525676d8a49f4a0369ff9bdfcc03353cb38e2922be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70a334677ee97eb736413a8969c44cf9ce05f974e3c2a8f357edee7c5569079`

```dockerfile
```

-	Layers:
	-	`sha256:f971faa507ce335f7f982d7a088dff1a9114649aada7c5bfae81ea0b390d8fb2`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 4.2 MB (4206432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651c8ce09cef70288863cdb500098d9f544b83ff4b50d5676ae627b20762712d`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d0710b8ca3a2acaf27e15c25caab509d1962cf8410d3813041ab55dcf48c6254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431434683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2921b29e37a06c8a336bfa14766da5a8c61757fa0466fce9d6d5cb5f3419cbc7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:7194610a7f4179b3802eddd2086f29f4f035a995dc17e3e1c96b19018bd9adc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df812cec45133e543498c0edcfb2d6fbde99a4a8886473136c2395489e131eb2`

```dockerfile
```

-	Layers:
	-	`sha256:e3fb357384c182c85ea602b2c4438cf07fb2dc1c4f14d3aa66a7ab34d6417829`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 4.2 MB (4206723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c2b565e0bc3d56e510ea31d284d09bd53daffe95029d693ef7b130e929384c`  
		Last Modified: Wed, 24 Jul 2024 13:38:54 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:509f364ad6298f3db09397e4dd09644ba568289e2d4d68c6dd1c3753ad5b5f71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:14bc3f4909564aa0204122165117ff91a792fbdfb7cec9a930ea8d3d76a1b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.8 MB (688810120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638cb8198a60de4ce4b28ab0bdfddf4d1fc4f9b884b770f7db4faf92afe89da`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe69d69e42accf33ea3d31e77d0716a7c2eaa512bf1a211d8f78770e4da40a84`  
		Last Modified: Wed, 24 Jul 2024 04:04:55 GMT  
		Size: 253.9 MB (253938104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:af37cb16f02e032c1305eec8816eb06633a55e8bc808db83d0acd21b89e3caed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12217554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a94d1f8270c9a9da1049145d5e27c9792ae2a5c4ace5bacd3793c52498da30`

```dockerfile
```

-	Layers:
	-	`sha256:aa5513b21b5c637ce5c2b598e89e9228d01557d90d58a863d428826d01da08ac`  
		Last Modified: Wed, 24 Jul 2024 04:04:52 GMT  
		Size: 12.2 MB (12207044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07d7c675eae42f841e14a7bc3eda5b67406ef27cc268153ea37022f541e04c9`  
		Last Modified: Wed, 24 Jul 2024 04:04:52 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:c6bdc5e93d87584ff2ba6973c45130835c26c901ab4ad8c0162dbd06be828108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.6 MB (666590748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f78db46f87c9e7c1fcda12a63a12a437689086da06abeb9d34985144daf82b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56799cc174d9ef497b9b5a22e204471e57d37a12dd8afb6542d7d4ade95b32ca`  
		Last Modified: Wed, 24 Jul 2024 17:45:14 GMT  
		Size: 235.2 MB (235156065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:60c34dfab2d01def4bca816175c42cd6bf344cbb3c5277dd5bb0c2e91716c6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12202457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0d75abe141e7e53fd18cfa8041ba184a196d68cd676c493e1ba361c191eaa2`

```dockerfile
```

-	Layers:
	-	`sha256:5912dd1693fad8dc4dabeac30b47403103a616fae229ede0a5522349acdc1c37`  
		Last Modified: Wed, 24 Jul 2024 17:45:08 GMT  
		Size: 12.2 MB (12191538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54889823702e4e651ce6d06ab71ac5ec20a71869130618912d1563bb5ae13b1`  
		Last Modified: Wed, 24 Jul 2024 17:45:07 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:b4e931157e7b1e4c99d51c688875ee5dcfb6374907b1d1f3b435eebc2e9617a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:92cf6331357019ca7fce03339485bfcb1bd15f9503ff1c90fffa126e11c8b379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529251178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3410172c418b27b3a4c8b11f47527841488850265ac9a2d6fb12fe6d0b9d2b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4fd2553b3cde3dc44739465863143422ef027b3e2ccf8fdad2ca285146761a`  
		Last Modified: Wed, 24 Jul 2024 04:04:19 GMT  
		Size: 94.4 MB (94379162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:72dc719ed84fe58d62c783ec530ba5844462b13a4d93efe223a4da723f345394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d11a1b5f7a10a5fe3a5a473ac828d1fbbe70a0127fba401adf8bd23ef6303`

```dockerfile
```

-	Layers:
	-	`sha256:830415755c1bcd381a9c3fad26dc08a6d830e790e968e596697d874f1b661d0c`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55fa4c8501c9f600c923c418fc382084759f9b64a1ecb9df30170c5895aad3`  
		Last Modified: Wed, 24 Jul 2024 04:04:17 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae519d0087b6683ef6d6cb801f8872a82d20e37ab4c0495bd8bd97353aa28b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518763016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8230039c143ef46af79079b4ecabea25b437d7bf5b648505a090961afa093f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ccf3d89f6526886cfd3e83a15ac470caf5fe772c267292076312e1e0053d50`  
		Last Modified: Wed, 24 Jul 2024 17:51:50 GMT  
		Size: 87.3 MB (87328333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a4bb7dd9f74b59b6dddc550ab3519aa7e3de111320995687dc78ecc2daaabda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd618ddab4afcff86e29050ed9ca88ca2a90ded4d38f09f0a201f46e2b75386`

```dockerfile
```

-	Layers:
	-	`sha256:84caf195619d750eba5ca8a279087555fac40f2896bc0e47597208d9c849fe1f`  
		Last Modified: Wed, 24 Jul 2024 17:51:49 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e8c16e2ac2e9e44f1a74315a1af747890a2698e1adf8d6830217b3047ce315`  
		Last Modified: Wed, 24 Jul 2024 17:51:48 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:c4a5c55b0473f200c974ded22c5ca722cbcd7a31f572ed9ad177956ffa794201
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:b734c4736598f277b4479e08be1563cd8f93873879e7c6fd4642a920e964220b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 MB (667183022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae7f7b58ff6b61d186eb2956b5c09a3af6e28c5efb9da281f81493e6aebc48`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab41794466d719760f1ff9d0f7e68f1e9213be1cc4c13981a0fd4bdf927f72`  
		Last Modified: Wed, 24 Jul 2024 04:05:02 GMT  
		Size: 232.3 MB (232311006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2256bcff13d74704e8eecee9ed3c30c4cab6acea1863103bd7571abff8bcc205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11094499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c282a044ea2134ab5a11d74f78feca9eca1a46ab4468fd7c7248d8fbef902255`

```dockerfile
```

-	Layers:
	-	`sha256:4e67ae10cd145cac3e07151a68abb4c830d4c25efcce650ef4cbbccad53a878b`  
		Last Modified: Wed, 24 Jul 2024 04:04:57 GMT  
		Size: 11.1 MB (11083868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc0201e90504fef514e2bca3958b809ee5e5dfa6a82d3627628676514717aa9`  
		Last Modified: Wed, 24 Jul 2024 04:04:57 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8287d99fd7223b0a247857754d269322c5a465e3ca70fcf03d4904bb95b4caf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.0 MB (644957514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3717ad3f72288f9aa98ee5100cee13e8a091ffebf6454f952bb546ec52a94421`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
USER root
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e7971174086bb160310e1756d2726077417678924080cda7c751b224dadf14`  
		Last Modified: Wed, 24 Jul 2024 17:53:33 GMT  
		Size: 213.5 MB (213522831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:528a4785a1300660dde901e07a5d6e0319820d3f5fd9974c2b8613b5002f01f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11079386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dd0a7931c75796539003313d23d72fa40c475cc270ee980952bd4060ba910f`

```dockerfile
```

-	Layers:
	-	`sha256:9b874b5e7dcb890c035cf4d68ccc2b05f9a2b8e04ccf44639a1b72a937b1ebd4`  
		Last Modified: Wed, 24 Jul 2024 17:53:29 GMT  
		Size: 11.1 MB (11068333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203e1bc82995131c66fac9ab803b27256e21bd6554755bae4562aa39f07b96f8`  
		Last Modified: Wed, 24 Jul 2024 17:53:28 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:9ffbf0a288fe3e045aa5fc550e3af2762f840bc8b3908ef3c530b46ebdfa4cfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3061dc1c1052c04ddab9f884ff2fe4cb771162bf3c8abe80eea409c24f0daa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434872016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7511b6075fcb3345f4eea620b5770eed460505f261cc993b0f8fd14acdc2ea`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a441b2151695c58acf7e393207625281fc4b6979b16e89ecd257f11924cdda`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336ef63816d2f1faff6e559f077b956c125b471f52b857bec735fd03d4626b5`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 24.3 MB (24280126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e0788b3e5c90456fc1cb6995a8213cced6f568d40eb6682e57367a727fc23`  
		Last Modified: Wed, 24 Jul 2024 03:06:34 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c501baa7cd609f2b69cd9082cbc8f85b12e615f6d2db2966a6338921e8d30a7`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:aeb8a3fc32a0b6930ae2c7525676d8a49f4a0369ff9bdfcc03353cb38e2922be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70a334677ee97eb736413a8969c44cf9ce05f974e3c2a8f357edee7c5569079`

```dockerfile
```

-	Layers:
	-	`sha256:f971faa507ce335f7f982d7a088dff1a9114649aada7c5bfae81ea0b390d8fb2`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 4.2 MB (4206432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651c8ce09cef70288863cdb500098d9f544b83ff4b50d5676ae627b20762712d`  
		Last Modified: Wed, 24 Jul 2024 03:06:30 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d0710b8ca3a2acaf27e15c25caab509d1962cf8410d3813041ab55dcf48c6254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431434683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2921b29e37a06c8a336bfa14766da5a8c61757fa0466fce9d6d5cb5f3419cbc7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Jun 2023 08:05:47 GMT
ARG RELEASE
# Thu, 29 Jun 2023 08:05:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Jun 2023 08:05:47 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Jun 2023 08:05:47 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Jun 2023 08:05:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Jun 2023 08:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 08:05:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Jun 2023 08:05:47 GMT
ARG spark_uid=185
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Thu, 29 Jun 2023 08:05:47 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Jun 2023 08:05:47 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Jun 2023 08:05:47 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Jun 2023 08:05:47 GMT
USER spark
# Thu, 29 Jun 2023 08:05:47 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee851c24fc2e8d1938adc35f3ed50034f301dff785d40c6b37bc87969458f2`  
		Last Modified: Wed, 24 Jul 2024 13:39:02 GMT  
		Size: 317.9 MB (317884892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc97841aa56fc811e746f59481627b01389ea3bfcfd8aa860db1b17c3054ea9`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7194610a7f4179b3802eddd2086f29f4f035a995dc17e3e1c96b19018bd9adc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df812cec45133e543498c0edcfb2d6fbde99a4a8886473136c2395489e131eb2`

```dockerfile
```

-	Layers:
	-	`sha256:e3fb357384c182c85ea602b2c4438cf07fb2dc1c4f14d3aa66a7ab34d6417829`  
		Last Modified: Wed, 24 Jul 2024 13:38:55 GMT  
		Size: 4.2 MB (4206723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c2b565e0bc3d56e510ea31d284d09bd53daffe95029d693ef7b130e929384c`  
		Last Modified: Wed, 24 Jul 2024 13:38:54 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0`

```console
$ docker pull spark@sha256:9b9209c95139548e1980ba7b17d02c681914f159383c4368eeb3a973d646c119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0` - linux; amd64

```console
$ docker pull spark@sha256:33880475ed4b0c3694af827eb56151d430f2ff0c552ae1b4f72c0f61462593fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535794312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64fd51010e993bf46a0dfd63d10250de71843c35eebdc8fcb6127fe9bdb6f6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200c6b5ae96d2a9c38d7af97fc948be575b6800b3265710b8a56601bd9564c9`  
		Last Modified: Wed, 24 Jul 2024 04:04:14 GMT  
		Size: 94.4 MB (94379945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0` - unknown; unknown

```console
$ docker pull spark@sha256:22bb87d2e4e540cde35b897a77aeb9350edb52fb985bf6977c780ec34d50a257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d630d468e0882d13e4e649277736187e1d07e5e801c519a5525ac62d95f00f`

```dockerfile
```

-	Layers:
	-	`sha256:0a353c651da4852b19b3df24fd0a709f0b58ede59841e9f94a55825c4203298a`  
		Last Modified: Wed, 24 Jul 2024 04:04:13 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d25235cb2d4063ddabb684768834e1c9890f3d0fb5a9f8389addd4f8f59eae0`  
		Last Modified: Wed, 24 Jul 2024 04:04:12 GMT  
		Size: 10.9 KB (10933 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:688b87c48728b6a416eb7e57a69ff2bcc5529123a70c33ff05fe43ece44396e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525305510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb725be859db8917fbf706ec21fa914a61fd7e01ed312ebf9f061815bf4d957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5bcc9069e69cc995e61f88bfc8631043d0e8000d591f8cecd4d8720aee2a3c`  
		Last Modified: Wed, 24 Jul 2024 17:49:03 GMT  
		Size: 87.3 MB (87328513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0` - unknown; unknown

```console
$ docker pull spark@sha256:fc7d1aff1115b262afecbb209ed00ab682fb620701907bcdbd6af354718ed4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8952396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5967f68d652bfd26d3320cee2b057036dd5295f6803228961bab6c29666a288`

```dockerfile
```

-	Layers:
	-	`sha256:33eeb526533e1997e6d0a9045e8e1258c87178c71d341217e019dd62effc43cf`  
		Last Modified: Wed, 24 Jul 2024 17:49:01 GMT  
		Size: 8.9 MB (8941028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8473da0015eddc13fff6ea2b5ca1ae569c071dc58ad4b60e723ac3172c8813`  
		Last Modified: Wed, 24 Jul 2024 17:49:00 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-java17`

```console
$ docker pull spark@sha256:a782174b8b8c843f425806df2cbb5512e35d79a72c8af5964ac977b308085bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17` - linux; amd64

```console
$ docker pull spark@sha256:3e6a1f28518c57c67cb67b4595bc4769760af420ff1694b48fc1729977dbf7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558182288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c87c630a5591eebee1a017eb5c576f679534dbbfa890516a50898e5bb26a600`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81535de18232e25ae8803d11597baeabe5697501f09295ddba02f5b1f437b0c2`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17` - unknown; unknown

```console
$ docker pull spark@sha256:12a053828a52c49a580d1f57f88df24c094726b13d352c95f461726f904eb46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04501e5d3067d56867bdb11f92a949b5ba15460f71fed44e703fb5dc7f26fe7a`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c2ec2c86eaf77dc830478e70c61a5b373b85b955d95adec55bfd2dfc386c8`  
		Last Modified: Tue, 23 Jul 2024 03:04:30 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f156139c238030c032a3566bd1a44e26cf2ff4252e4857a52f199bb52cc1e9e8`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b303ab63ac96e36f9b51e3019782d5dbc24dde7b484e4bb5f5d622d859dda871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551256754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e37f5506d85576cac554e1b83b614153ed8d612b1517c36bced3833a4d3f1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba108c627b9e9e46a70b0e22cbb13abedbeddd7a3ec9af4f1a85993cb24614f4`  
		Last Modified: Wed, 24 Jul 2024 13:43:40 GMT  
		Size: 114.3 MB (114303424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17` - unknown; unknown

```console
$ docker pull spark@sha256:3c808f9c58191ad4f5a5daf6eeb85dc4cd14c81c402339d83223f1798879c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9744616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20bf5c3cc156b6e6b67f1b1e507c2eff519a5860b1423bfc0aef495812ff47`

```dockerfile
```

-	Layers:
	-	`sha256:1fc72ba37e1ef204c785d4b7c96fae60ef77e638295413fbf8cba026b53c2f4c`  
		Last Modified: Wed, 24 Jul 2024 13:43:37 GMT  
		Size: 9.7 MB (9733219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aeac44f2e93fd06843767fb1b4b9da7f726eb93f9efbd4db2e2771ffcd45e2`  
		Last Modified: Wed, 24 Jul 2024 13:43:36 GMT  
		Size: 11.4 KB (11397 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-java17-python3`

```console
$ docker pull spark@sha256:a782174b8b8c843f425806df2cbb5512e35d79a72c8af5964ac977b308085bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:3e6a1f28518c57c67cb67b4595bc4769760af420ff1694b48fc1729977dbf7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558182288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c87c630a5591eebee1a017eb5c576f679534dbbfa890516a50898e5bb26a600`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81535de18232e25ae8803d11597baeabe5697501f09295ddba02f5b1f437b0c2`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:12a053828a52c49a580d1f57f88df24c094726b13d352c95f461726f904eb46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04501e5d3067d56867bdb11f92a949b5ba15460f71fed44e703fb5dc7f26fe7a`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c2ec2c86eaf77dc830478e70c61a5b373b85b955d95adec55bfd2dfc386c8`  
		Last Modified: Tue, 23 Jul 2024 03:04:30 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f156139c238030c032a3566bd1a44e26cf2ff4252e4857a52f199bb52cc1e9e8`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b303ab63ac96e36f9b51e3019782d5dbc24dde7b484e4bb5f5d622d859dda871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551256754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e37f5506d85576cac554e1b83b614153ed8d612b1517c36bced3833a4d3f1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba108c627b9e9e46a70b0e22cbb13abedbeddd7a3ec9af4f1a85993cb24614f4`  
		Last Modified: Wed, 24 Jul 2024 13:43:40 GMT  
		Size: 114.3 MB (114303424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:3c808f9c58191ad4f5a5daf6eeb85dc4cd14c81c402339d83223f1798879c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9744616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20bf5c3cc156b6e6b67f1b1e507c2eff519a5860b1423bfc0aef495812ff47`

```dockerfile
```

-	Layers:
	-	`sha256:1fc72ba37e1ef204c785d4b7c96fae60ef77e638295413fbf8cba026b53c2f4c`  
		Last Modified: Wed, 24 Jul 2024 13:43:37 GMT  
		Size: 9.7 MB (9733219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aeac44f2e93fd06843767fb1b4b9da7f726eb93f9efbd4db2e2771ffcd45e2`  
		Last Modified: Wed, 24 Jul 2024 13:43:36 GMT  
		Size: 11.4 KB (11397 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-java17-r`

```console
$ docker pull spark@sha256:1957516e00f085a07566df8995d6698dd5bc61c172f231b86c9996f660c1b735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:ab68698352bf0d93b9cb12a668593b2d38cc2ae22879a983c4b4572a5931c2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763746380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d097281537bac7542ff8e9ad41b82a5cd4f7fcf7ede48563d40b3170d1f4e8`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1882de9505accfa92e7428dfd5ac2a3104b0f270f9c1b1db2f9f8119053e9ea7`  
		Last Modified: Tue, 23 Jul 2024 03:05:33 GMT  
		Size: 323.8 MB (323832086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:30b716741d81a8adcbb85c308f2b77da546091c518e48663a85f13bece0bf463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156101b636e86d243b4769f3969ed5f44b3d32a93b36f3b0cea5627c63434ad5`

```dockerfile
```

-	Layers:
	-	`sha256:fb1cf620dabf192067d1596cb31d07a96130fef6442c3c198a7e773e1e018160`  
		Last Modified: Tue, 23 Jul 2024 03:05:24 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d078a8ac3670f7b494c371b77d33943b3d1df08bcb7d66e10f24a0ab9499a487`  
		Last Modified: Tue, 23 Jul 2024 03:05:23 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a65251a34ef322f568a04fdb6cba44de785e19355d4bb2bbef0a9b0250499ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.5 MB (745462364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c0d46067370ab1ca36e6e81f01dbaa947fe9447ee87f784efdf0ec96af05fa`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38b61c8827dfdaa0c3cc757dbcbb7343e987635b396394bb150cb41d14f8b89`  
		Last Modified: Wed, 24 Jul 2024 13:45:52 GMT  
		Size: 308.5 MB (308509034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:78e3a5e3091375c5a319bfc985262747a4e78cc9c2e2f03ec68baa70c4aeb74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7bb475bca9705b8305d7e02f39737cb2c9612b90183f8ca03dab54e562c13e`

```dockerfile
```

-	Layers:
	-	`sha256:1535954c5733f684ae1b9f8c8fe58036a5a7e78ecf4cd79095557f35776b6ee5`  
		Last Modified: Wed, 24 Jul 2024 13:45:45 GMT  
		Size: 17.7 MB (17730394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2704bd77451725059084fe9d6ebc4580a0e0d60ffa1ca6ffd50e6ac18b3239b7`  
		Last Modified: Wed, 24 Jul 2024 13:45:44 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-java17-scala`

```console
$ docker pull spark@sha256:4dc81cf0d1f6da2c43567878f13ad43fc50ce2b1f10e6963168dae27481f5b7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:6cf0cfefdae2ff308e07391f51bc82b8865ca9254910f571b4dc59b5919d1e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439914294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b614a0a8925c9d8043e27fac05cf58b637f9bbdc698357a05e0794cc1d390633`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:d76c8271c29726c42d96297a956210e38095e9c30cfd78d8e8ac335d9a9504c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edfb7f55b5e62b1ab8b253e49b59463c7ecabbf5a55580663dbff8c81201d99`

```dockerfile
```

-	Layers:
	-	`sha256:3e74741fad8dcf2775cd9aaf31fda6053df19ae246572bcb533ca97c7591b966`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b37f134655b84c46868dd72b260196d3c47dddc8e80579fea30625d6a91b5f6`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:525b9bc58961c3e89d881f27b542c543cbe488f0951305d6d4708f7c6a0cf6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436953330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24b5356309458d8fd16cf456096e9229b04f8c92e73c833c855d73b4661e20a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:4e17a2305405567fa9ece8bd990716796862d979d74f46b2f8f245846f60afb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bcc983618d6d6b1eebd427a32ed7d5a5a290819ca13c0c7b341d39da21f977`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f507567e7b91788ceabcde89e678d2a0f745abba2233899a489fa8d73b9`  
		Last Modified: Wed, 24 Jul 2024 08:38:15 GMT  
		Size: 4.2 MB (4218135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58086460b88cb00b7f9a823a382b7dec7eb944da79d5c64f6839470ae062a95`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-python3`

```console
$ docker pull spark@sha256:9b9209c95139548e1980ba7b17d02c681914f159383c4368eeb3a973d646c119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-python3` - linux; amd64

```console
$ docker pull spark@sha256:33880475ed4b0c3694af827eb56151d430f2ff0c552ae1b4f72c0f61462593fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535794312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64fd51010e993bf46a0dfd63d10250de71843c35eebdc8fcb6127fe9bdb6f6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200c6b5ae96d2a9c38d7af97fc948be575b6800b3265710b8a56601bd9564c9`  
		Last Modified: Wed, 24 Jul 2024 04:04:14 GMT  
		Size: 94.4 MB (94379945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-python3` - unknown; unknown

```console
$ docker pull spark@sha256:22bb87d2e4e540cde35b897a77aeb9350edb52fb985bf6977c780ec34d50a257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d630d468e0882d13e4e649277736187e1d07e5e801c519a5525ac62d95f00f`

```dockerfile
```

-	Layers:
	-	`sha256:0a353c651da4852b19b3df24fd0a709f0b58ede59841e9f94a55825c4203298a`  
		Last Modified: Wed, 24 Jul 2024 04:04:13 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d25235cb2d4063ddabb684768834e1c9890f3d0fb5a9f8389addd4f8f59eae0`  
		Last Modified: Wed, 24 Jul 2024 04:04:12 GMT  
		Size: 10.9 KB (10933 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:688b87c48728b6a416eb7e57a69ff2bcc5529123a70c33ff05fe43ece44396e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525305510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb725be859db8917fbf706ec21fa914a61fd7e01ed312ebf9f061815bf4d957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5bcc9069e69cc995e61f88bfc8631043d0e8000d591f8cecd4d8720aee2a3c`  
		Last Modified: Wed, 24 Jul 2024 17:49:03 GMT  
		Size: 87.3 MB (87328513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-python3` - unknown; unknown

```console
$ docker pull spark@sha256:fc7d1aff1115b262afecbb209ed00ab682fb620701907bcdbd6af354718ed4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8952396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5967f68d652bfd26d3320cee2b057036dd5295f6803228961bab6c29666a288`

```dockerfile
```

-	Layers:
	-	`sha256:33eeb526533e1997e6d0a9045e8e1258c87178c71d341217e019dd62effc43cf`  
		Last Modified: Wed, 24 Jul 2024 17:49:01 GMT  
		Size: 8.9 MB (8941028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8473da0015eddc13fff6ea2b5ca1ae569c071dc58ad4b60e723ac3172c8813`  
		Last Modified: Wed, 24 Jul 2024 17:49:00 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-r`

```console
$ docker pull spark@sha256:f173b836abe3883a5ff09d302ff775a649d23505b2c643f6aff56267cb6e3632
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-r` - linux; amd64

```console
$ docker pull spark@sha256:71b9e09a4e950c3b453299af36d9729a7b1f01e43172873dc43d9bc8e923e541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673727507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef74d0b4141e3028060be0b1b0569d25c8118be8ab576a7fe8eb01365cdaed5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8ef35e9ab5e3de27d464785168d585d67bd77f837f70a401210e06068fcf7e`  
		Last Modified: Wed, 24 Jul 2024 04:04:46 GMT  
		Size: 232.3 MB (232313140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-r` - unknown; unknown

```console
$ docker pull spark@sha256:d5f856d2b8ee3cbd2400d6b9543597b803ba420633602c2182e57b1b19c7060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ae03a8e643e6ce2724a2c5b770b26298551238c1140a6db4b898fc7e476637`

```dockerfile
```

-	Layers:
	-	`sha256:b34db3d5dd2bb116be37b5b1d8d7374b7765818e7f21631d26bfa4ac878271ef`  
		Last Modified: Wed, 24 Jul 2024 04:04:42 GMT  
		Size: 11.1 MB (11092771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda265ba61f138572bf4a32723570785ceb01a4769c515e7d019d6b458b4125f`  
		Last Modified: Wed, 24 Jul 2024 04:04:41 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:75d90e375a61f1d68f367fd22f4057de125057b291c34e725c7cc5d94848b1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.5 MB (651500588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0721a3a0f8a4c6a6ed1fabc809ce0310299c1fa5d1ed5168d0d2de10c06a0096`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cda64b5a3f9ff84701e2a2fa0b1c1812e96bec6e46f6c29729660693057252`  
		Last Modified: Wed, 24 Jul 2024 17:50:46 GMT  
		Size: 213.5 MB (213523591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-r` - unknown; unknown

```console
$ docker pull spark@sha256:3a1de4bec86adfb3eb3f203c099a80316d54db43e1907f308d2512776c09c545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c73df4cd544e0643b19fc3c095429cdadee9774b95cb11d37a0b021969d4c38`

```dockerfile
```

-	Layers:
	-	`sha256:dfa4d604898095fd6105f7c2e96a5c858b44bb1753954da78b1f05a65e4009ec`  
		Last Modified: Wed, 24 Jul 2024 17:50:42 GMT  
		Size: 11.1 MB (11077236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4d50a297ee1fc68af4762dab28868d75e08245088930c7c0d2709989691e1d`  
		Last Modified: Wed, 24 Jul 2024 17:50:41 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala`

```console
$ docker pull spark@sha256:107d927f3f1d110ec9c61de3917bb0bb2378ce9e6330604236da42d05734b2bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala` - linux; amd64

```console
$ docker pull spark@sha256:96f7c7cfcbeb93f6b5c18634fe9cea812f4fe0613a2194094734df6aaa44b407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441414367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1093887a8d6e793f55db45176614544f707703554dfbced27505ffbf9340ac79`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:779f93b42cfe16ab8a44340be9160ce42bd08c9f96bdc3bac0dbab62e0934d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a58dcd4ecf3b62e32b66cd63ef3341c60fdbac97ceecd23dbb7a838cf97495`

```dockerfile
```

-	Layers:
	-	`sha256:89f19c464a2e90e494af0d6de3d9516a0685c88ce524e6626c2a08a2f60df018`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 4.2 MB (4215309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4559b7180655e85da346c58c09e69651337d47045ad271ef32d3b8ee0a279ed5`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 22.4 KB (22406 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07cf89335e729274fb44d7ba2abb21c89784e83c7a2633144be134839e67b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437976997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbffad98661223a927932322760d8caf980e448190e7ccdfbe56a3be814c945`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:94fc4aafd2ae6762ce505751ccfbff5e99242f6cd58434a36f21435630223901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11085e54ea786a71f7b7bdf7b7927ad14efb10054255efd04e4427dbd884a7c8`

```dockerfile
```

-	Layers:
	-	`sha256:994402b9b5ea55f84b455739e28c41792d3a6a502233feca3775e9e3c2a46d7c`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 4.2 MB (4215600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9160d1cc7da5a1d2d59f1aaf427224c147ba9511d562043a1aa1485e69f09730`  
		Last Modified: Wed, 24 Jul 2024 13:33:21 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:8ad1cd3dda0e1821c328ebb8f140b7bf6c89cf69413dea30d8aac2c82e14e7e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:7bc8c3f868e67d49303712735d143f8de0d6fcb4763f4004fe780eb7f8850cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.4 MB (695354051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca3d8dd3ac75723f265b6cc47411e7fcaed0a98902cc827f418948aa6c9a9ad`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a8271e1df4d737289044fa4f3a19d4566436d866cd820a0366ad1974701814`  
		Last Modified: Wed, 24 Jul 2024 04:05:02 GMT  
		Size: 253.9 MB (253939684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8bb8f7313066f6bf1dd44944b622c71116038e75670cfdbab8483cd7d922bfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e025a2c69717429bbb4ce2318cbc0004d34e5f94dbbab7c40c78b1f635b7856a`

```dockerfile
```

-	Layers:
	-	`sha256:b4d1b2a3f1577c63db9b89783aa832b5d01f2bb6c7e4646373d1685f918a6d78`  
		Last Modified: Wed, 24 Jul 2024 04:04:57 GMT  
		Size: 12.2 MB (12215947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c53fe04b37dd88ec129c0d6cb95568c8c59d51443c39f07240bf34a2e88ca7`  
		Last Modified: Wed, 24 Jul 2024 04:04:56 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8709e40734ffcccd451b3ab027e410d306e1b41bb0b65b4168d32a5dc89f8d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.1 MB (673132630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b29d81a1e3c424fcbf69862fbb29e1d7fb086255427cd32175795f8e14d2a01`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcad1b230c3e4a3e9128df11a8cf513e8250f0e60d14eba813485df25224fc7`  
		Last Modified: Wed, 24 Jul 2024 17:43:17 GMT  
		Size: 235.2 MB (235155633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:463bfe2192082bcc87d586ba04f6c40bf261398198651e5cf30a7d17773caf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12211360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f326f20bf05886cb88bdea152cf5d76360d1d6ba89f24072fe7b0fa6748eb3`

```dockerfile
```

-	Layers:
	-	`sha256:095c75dc712d14275349a10ee47ad9d8bc8abed663131aad428a76eae372fa31`  
		Last Modified: Wed, 24 Jul 2024 17:43:11 GMT  
		Size: 12.2 MB (12200441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f150803c30bcaaa1406fa9f2e4bd560e1367d8bbbf6eb28ebf2be25bfea29e05`  
		Last Modified: Wed, 24 Jul 2024 17:43:11 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:9b9209c95139548e1980ba7b17d02c681914f159383c4368eeb3a973d646c119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:33880475ed4b0c3694af827eb56151d430f2ff0c552ae1b4f72c0f61462593fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535794312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64fd51010e993bf46a0dfd63d10250de71843c35eebdc8fcb6127fe9bdb6f6`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200c6b5ae96d2a9c38d7af97fc948be575b6800b3265710b8a56601bd9564c9`  
		Last Modified: Wed, 24 Jul 2024 04:04:14 GMT  
		Size: 94.4 MB (94379945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:22bb87d2e4e540cde35b897a77aeb9350edb52fb985bf6977c780ec34d50a257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d630d468e0882d13e4e649277736187e1d07e5e801c519a5525ac62d95f00f`

```dockerfile
```

-	Layers:
	-	`sha256:0a353c651da4852b19b3df24fd0a709f0b58ede59841e9f94a55825c4203298a`  
		Last Modified: Wed, 24 Jul 2024 04:04:13 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d25235cb2d4063ddabb684768834e1c9890f3d0fb5a9f8389addd4f8f59eae0`  
		Last Modified: Wed, 24 Jul 2024 04:04:12 GMT  
		Size: 10.9 KB (10933 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:688b87c48728b6a416eb7e57a69ff2bcc5529123a70c33ff05fe43ece44396e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525305510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb725be859db8917fbf706ec21fa914a61fd7e01ed312ebf9f061815bf4d957`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5bcc9069e69cc995e61f88bfc8631043d0e8000d591f8cecd4d8720aee2a3c`  
		Last Modified: Wed, 24 Jul 2024 17:49:03 GMT  
		Size: 87.3 MB (87328513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:fc7d1aff1115b262afecbb209ed00ab682fb620701907bcdbd6af354718ed4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8952396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5967f68d652bfd26d3320cee2b057036dd5295f6803228961bab6c29666a288`

```dockerfile
```

-	Layers:
	-	`sha256:33eeb526533e1997e6d0a9045e8e1258c87178c71d341217e019dd62effc43cf`  
		Last Modified: Wed, 24 Jul 2024 17:49:01 GMT  
		Size: 8.9 MB (8941028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8473da0015eddc13fff6ea2b5ca1ae569c071dc58ad4b60e723ac3172c8813`  
		Last Modified: Wed, 24 Jul 2024 17:49:00 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:f173b836abe3883a5ff09d302ff775a649d23505b2c643f6aff56267cb6e3632
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:71b9e09a4e950c3b453299af36d9729a7b1f01e43172873dc43d9bc8e923e541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673727507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef74d0b4141e3028060be0b1b0569d25c8118be8ab576a7fe8eb01365cdaed5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8ef35e9ab5e3de27d464785168d585d67bd77f837f70a401210e06068fcf7e`  
		Last Modified: Wed, 24 Jul 2024 04:04:46 GMT  
		Size: 232.3 MB (232313140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d5f856d2b8ee3cbd2400d6b9543597b803ba420633602c2182e57b1b19c7060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ae03a8e643e6ce2724a2c5b770b26298551238c1140a6db4b898fc7e476637`

```dockerfile
```

-	Layers:
	-	`sha256:b34db3d5dd2bb116be37b5b1d8d7374b7765818e7f21631d26bfa4ac878271ef`  
		Last Modified: Wed, 24 Jul 2024 04:04:42 GMT  
		Size: 11.1 MB (11092771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda265ba61f138572bf4a32723570785ceb01a4769c515e7d019d6b458b4125f`  
		Last Modified: Wed, 24 Jul 2024 04:04:41 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:75d90e375a61f1d68f367fd22f4057de125057b291c34e725c7cc5d94848b1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.5 MB (651500588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0721a3a0f8a4c6a6ed1fabc809ce0310299c1fa5d1ed5168d0d2de10c06a0096`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
USER root
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV R_HOME=/usr/lib/R
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cda64b5a3f9ff84701e2a2fa0b1c1812e96bec6e46f6c29729660693057252`  
		Last Modified: Wed, 24 Jul 2024 17:50:46 GMT  
		Size: 213.5 MB (213523591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3a1de4bec86adfb3eb3f203c099a80316d54db43e1907f308d2512776c09c545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c73df4cd544e0643b19fc3c095429cdadee9774b95cb11d37a0b021969d4c38`

```dockerfile
```

-	Layers:
	-	`sha256:dfa4d604898095fd6105f7c2e96a5c858b44bb1753954da78b1f05a65e4009ec`  
		Last Modified: Wed, 24 Jul 2024 17:50:42 GMT  
		Size: 11.1 MB (11077236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4d50a297ee1fc68af4762dab28868d75e08245088930c7c0d2709989691e1d`  
		Last Modified: Wed, 24 Jul 2024 17:50:41 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:107d927f3f1d110ec9c61de3917bb0bb2378ce9e6330604236da42d05734b2bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:96f7c7cfcbeb93f6b5c18634fe9cea812f4fe0613a2194094734df6aaa44b407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441414367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1093887a8d6e793f55db45176614544f707703554dfbced27505ffbf9340ac79`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e100c290c0f4312d3e87dd383fb0ed64e3ff38e7c30e304c43f9e7aecf130`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f2e3593fb7406aa8b309d02bedbc1c3f2b0a4dd4716f58c3e27f75e5dd610e`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 24.3 MB (24280185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122ccb56807dc550d0175a64c0953950f8633c73655c4119c0c83cdef2b3408`  
		Last Modified: Wed, 24 Jul 2024 03:07:28 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb036fadd5c6eb6dc3cb65261824b095cb65b0785ac1aa4b3ca182613ee44d0`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:779f93b42cfe16ab8a44340be9160ce42bd08c9f96bdc3bac0dbab62e0934d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a58dcd4ecf3b62e32b66cd63ef3341c60fdbac97ceecd23dbb7a838cf97495`

```dockerfile
```

-	Layers:
	-	`sha256:89f19c464a2e90e494af0d6de3d9516a0685c88ce524e6626c2a08a2f60df018`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 4.2 MB (4215309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4559b7180655e85da346c58c09e69651337d47045ad271ef32d3b8ee0a279ed5`  
		Last Modified: Wed, 24 Jul 2024 03:07:24 GMT  
		Size: 22.4 KB (22406 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07cf89335e729274fb44d7ba2abb21c89784e83c7a2633144be134839e67b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437976997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbffad98661223a927932322760d8caf980e448190e7ccdfbe56a3be814c945`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 14 Sep 2023 13:22:32 GMT
ARG RELEASE
# Thu, 14 Sep 2023 13:22:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Sep 2023 13:22:32 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 14 Sep 2023 13:22:32 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 14 Sep 2023 13:22:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Sep 2023 13:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 13:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Sep 2023 13:22:32 GMT
ARG spark_uid=185
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Thu, 14 Sep 2023 13:22:32 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 14 Sep 2023 13:22:32 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 14 Sep 2023 13:22:32 GMT
WORKDIR /opt/spark/work-dir
# Thu, 14 Sep 2023 13:22:32 GMT
USER spark
# Thu, 14 Sep 2023 13:22:32 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52ab307a4c3c8786df10eab86dda1064b7851c2e65260f07db89e0193754db`  
		Last Modified: Wed, 24 Jul 2024 13:33:29 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276f2a1172ed4987da63487c6dde17a5fb50aa13b450faf5db79944b019509f`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:94fc4aafd2ae6762ce505751ccfbff5e99242f6cd58434a36f21435630223901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11085e54ea786a71f7b7bdf7b7927ad14efb10054255efd04e4427dbd884a7c8`

```dockerfile
```

-	Layers:
	-	`sha256:994402b9b5ea55f84b455739e28c41792d3a6a502233feca3775e9e3c2a46d7c`  
		Last Modified: Wed, 24 Jul 2024 13:33:22 GMT  
		Size: 4.2 MB (4215600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9160d1cc7da5a1d2d59f1aaf427224c147ba9511d562043a1aa1485e69f09730`  
		Last Modified: Wed, 24 Jul 2024 13:33:21 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:737832a2c61e3a89b81bb03236751dbf139adee5258ddf373c429203f7a9b6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:502302d46c5145937be173582d9dbe463e7e9c7fbd8d192a9cf41b1cdfd7f262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.5 MB (778460460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0becc5d93e02ac45adbabf4025dc884f6dae303674fbf209b18e4a23aa018f3f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed109f7174e3d63067f852e4527d76b11c6bbd3dbecc563a090c6d4637d20`  
		Last Modified: Tue, 23 Jul 2024 03:05:36 GMT  
		Size: 338.5 MB (338546166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2a3ecfae3b1f18db3d8e22dd69445d359ca50c564a156ab0ad866715ba7c6806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536d46cba0c33a1261f8885cd36564313dcff57876dc0f4c5ac43d24adaa42b5`

```dockerfile
```

-	Layers:
	-	`sha256:a894e059e816fd4f58c2e150e1566246716064c4ec78b3e4befde4bca905ddca`  
		Last Modified: Tue, 23 Jul 2024 03:05:27 GMT  
		Size: 18.8 MB (18776000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3fa2b5738e2ae21ce02a5fb8775e2e06e9f7b4986613853c07ad1644cdeeae`  
		Last Modified: Tue, 23 Jul 2024 03:05:26 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:02f29840e358f7745b6cde77d6170776743a0e95a6457a40527e4e45a2162abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 MB (759996845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227987899cd7641b58af45a4a42bef794fa6de639250ca2544cdc24c5bf2f4cf`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bb63a18fd097885325f3ddcefe162da1ab4b6d517d982cddadd175fd760ea`  
		Last Modified: Wed, 24 Jul 2024 13:28:08 GMT  
		Size: 323.0 MB (323043515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d4559ea6a6466bf989d3551e46dc8910928c6609a3e2662326c62f45ec9f3fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18753245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5802b9fb9e418ebeacbcc7c558cdd7f86e654f85522fe081f41fbcc9efe8824`

```dockerfile
```

-	Layers:
	-	`sha256:abf845a564da023aac8ed6135bdcc792687862214fcadfd4d8de306ed129dd2b`  
		Last Modified: Wed, 24 Jul 2024 13:28:01 GMT  
		Size: 18.7 MB (18742326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7172df032dff1232b3cec3efe977e41fb2c709177552926dd0376e1bafd03d32`  
		Last Modified: Wed, 24 Jul 2024 13:28:01 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:a782174b8b8c843f425806df2cbb5512e35d79a72c8af5964ac977b308085bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3e6a1f28518c57c67cb67b4595bc4769760af420ff1694b48fc1729977dbf7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558182288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c87c630a5591eebee1a017eb5c576f679534dbbfa890516a50898e5bb26a600`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81535de18232e25ae8803d11597baeabe5697501f09295ddba02f5b1f437b0c2`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:12a053828a52c49a580d1f57f88df24c094726b13d352c95f461726f904eb46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04501e5d3067d56867bdb11f92a949b5ba15460f71fed44e703fb5dc7f26fe7a`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c2ec2c86eaf77dc830478e70c61a5b373b85b955d95adec55bfd2dfc386c8`  
		Last Modified: Tue, 23 Jul 2024 03:04:30 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f156139c238030c032a3566bd1a44e26cf2ff4252e4857a52f199bb52cc1e9e8`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b303ab63ac96e36f9b51e3019782d5dbc24dde7b484e4bb5f5d622d859dda871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551256754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e37f5506d85576cac554e1b83b614153ed8d612b1517c36bced3833a4d3f1f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba108c627b9e9e46a70b0e22cbb13abedbeddd7a3ec9af4f1a85993cb24614f4`  
		Last Modified: Wed, 24 Jul 2024 13:43:40 GMT  
		Size: 114.3 MB (114303424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3c808f9c58191ad4f5a5daf6eeb85dc4cd14c81c402339d83223f1798879c26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9744616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20bf5c3cc156b6e6b67f1b1e507c2eff519a5860b1423bfc0aef495812ff47`

```dockerfile
```

-	Layers:
	-	`sha256:1fc72ba37e1ef204c785d4b7c96fae60ef77e638295413fbf8cba026b53c2f4c`  
		Last Modified: Wed, 24 Jul 2024 13:43:37 GMT  
		Size: 9.7 MB (9733219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aeac44f2e93fd06843767fb1b4b9da7f726eb93f9efbd4db2e2771ffcd45e2`  
		Last Modified: Wed, 24 Jul 2024 13:43:36 GMT  
		Size: 11.4 KB (11397 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:1957516e00f085a07566df8995d6698dd5bc61c172f231b86c9996f660c1b735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:ab68698352bf0d93b9cb12a668593b2d38cc2ae22879a983c4b4572a5931c2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763746380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d097281537bac7542ff8e9ad41b82a5cd4f7fcf7ede48563d40b3170d1f4e8`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1882de9505accfa92e7428dfd5ac2a3104b0f270f9c1b1db2f9f8119053e9ea7`  
		Last Modified: Tue, 23 Jul 2024 03:05:33 GMT  
		Size: 323.8 MB (323832086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:30b716741d81a8adcbb85c308f2b77da546091c518e48663a85f13bece0bf463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156101b636e86d243b4769f3969ed5f44b3d32a93b36f3b0cea5627c63434ad5`

```dockerfile
```

-	Layers:
	-	`sha256:fb1cf620dabf192067d1596cb31d07a96130fef6442c3c198a7e773e1e018160`  
		Last Modified: Tue, 23 Jul 2024 03:05:24 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d078a8ac3670f7b494c371b77d33943b3d1df08bcb7d66e10f24a0ab9499a487`  
		Last Modified: Tue, 23 Jul 2024 03:05:23 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a65251a34ef322f568a04fdb6cba44de785e19355d4bb2bbef0a9b0250499ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.5 MB (745462364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c0d46067370ab1ca36e6e81f01dbaa947fe9447ee87f784efdf0ec96af05fa`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
USER root
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV R_HOME=/usr/lib/R
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38b61c8827dfdaa0c3cc757dbcbb7343e987635b396394bb150cb41d14f8b89`  
		Last Modified: Wed, 24 Jul 2024 13:45:52 GMT  
		Size: 308.5 MB (308509034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:78e3a5e3091375c5a319bfc985262747a4e78cc9c2e2f03ec68baa70c4aeb74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7bb475bca9705b8305d7e02f39737cb2c9612b90183f8ca03dab54e562c13e`

```dockerfile
```

-	Layers:
	-	`sha256:1535954c5733f684ae1b9f8c8fe58036a5a7e78ecf4cd79095557f35776b6ee5`  
		Last Modified: Wed, 24 Jul 2024 13:45:45 GMT  
		Size: 17.7 MB (17730394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2704bd77451725059084fe9d6ebc4580a0e0d60ffa1ca6ffd50e6ac18b3239b7`  
		Last Modified: Wed, 24 Jul 2024 13:45:44 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:4dc81cf0d1f6da2c43567878f13ad43fc50ce2b1f10e6963168dae27481f5b7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6cf0cfefdae2ff308e07391f51bc82b8865ca9254910f571b4dc59b5919d1e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439914294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b614a0a8925c9d8043e27fac05cf58b637f9bbdc698357a05e0794cc1d390633`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6730d92fd8576f4d396ceb1997ca679238c8670b7df6fcaf6f58f8360ac07`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a426832eebc4de086452c4174c483747fb770a9a101d07f71a857f72c340d4`  
		Last Modified: Tue, 23 Jul 2024 02:07:11 GMT  
		Size: 24.9 MB (24890880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e413baa841ad2ce05bfe75cc5a7e533970e17f5b1d0c6c5d2ee1e2a0033b6e`  
		Last Modified: Tue, 23 Jul 2024 02:07:14 GMT  
		Size: 324.4 MB (324427123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926565581d62e0f981671783c8c053b7aa644a06ea912d34f5f66082d6f9408d`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d76c8271c29726c42d96297a956210e38095e9c30cfd78d8e8ac335d9a9504c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edfb7f55b5e62b1ab8b253e49b59463c7ecabbf5a55580663dbff8c81201d99`

```dockerfile
```

-	Layers:
	-	`sha256:3e74741fad8dcf2775cd9aaf31fda6053df19ae246572bcb533ca97c7591b966`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b37f134655b84c46868dd72b260196d3c47dddc8e80579fea30625d6a91b5f6`  
		Last Modified: Tue, 23 Jul 2024 02:07:10 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:525b9bc58961c3e89d881f27b542c543cbe488f0951305d6d4708f7c6a0cf6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436953330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24b5356309458d8fd16cf456096e9229b04f8c92e73c833c855d73b4661e20a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Nov 2023 03:33:39 GMT
ARG RELEASE
# Fri, 10 Nov 2023 03:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 10 Nov 2023 03:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Nov 2023 03:33:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 10 Nov 2023 03:33:39 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Nov 2023 03:33:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 03:33:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 10 Nov 2023 03:33:39 GMT
ARG spark_uid=185
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz.asc GPG_KEY=FC3AE3A7EAA1BAC98770840E7E1ABCC53AAA2216
# Fri, 10 Nov 2023 03:33:39 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 10 Nov 2023 03:33:39 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 10 Nov 2023 03:33:39 GMT
WORKDIR /opt/spark/work-dir
# Fri, 10 Nov 2023 03:33:39 GMT
USER spark
# Fri, 10 Nov 2023 03:33:39 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2848a1d327a5b71d01392538ab6abda5c4b9667a14094e9476ec249d419aaea`  
		Last Modified: Wed, 24 Jul 2024 08:38:21 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27061b2a9e0e4d641dc642c9d2adc2976ec91d31f75f9d5fc15aeaf090d7b051`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4e17a2305405567fa9ece8bd990716796862d979d74f46b2f8f245846f60afb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bcc983618d6d6b1eebd427a32ed7d5a5a290819ca13c0c7b341d39da21f977`

```dockerfile
```

-	Layers:
	-	`sha256:bfe76f507567e7b91788ceabcde89e678d2a0f745abba2233899a489fa8d73b9`  
		Last Modified: Wed, 24 Jul 2024 08:38:15 GMT  
		Size: 4.2 MB (4218135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58086460b88cb00b7f9a823a382b7dec7eb944da79d5c64f6839470ae062a95`  
		Last Modified: Wed, 24 Jul 2024 08:38:14 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1`

```console
$ docker pull spark@sha256:949e41e69700ce48a7e9ed2422d9466aa0dd53ea596a32ba4bde5a481f3e80cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1` - linux; amd64

```console
$ docker pull spark@sha256:ffa3e64ad80d524e876abf809dba60919bde26b210b267bbe8e8764ab86c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535849031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f600e30f900b5b7744276f4368820140c76743aa51f0f6eee316b899fb0130`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c6966f4aad89717ff3771ce987c0d71548ce56fc036157b92b0fda5f4c373`  
		Last Modified: Wed, 24 Jul 2024 04:04:09 GMT  
		Size: 94.4 MB (94378969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1` - unknown; unknown

```console
$ docker pull spark@sha256:116f98af3fd6c41c3cb7c31f81eb1e27c09adee21b16059d0a471bf84f27f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d66c8df5936e909d91c350ad73075d785568aaf206f7288437adbb8c3d706`

```dockerfile
```

-	Layers:
	-	`sha256:67e2c0b0979c518cb212345bc7a57cb8dcf515145a8317b340e58add19d567a5`  
		Last Modified: Wed, 24 Jul 2024 04:04:08 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193ed5fa925a5ea45c09bd3e84ae93f61ecf87f79ead30d5a2fdc2bee1fd4ed8`  
		Last Modified: Wed, 24 Jul 2024 04:04:07 GMT  
		Size: 11.5 KB (11528 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:210cfe7e5338d8abadc85fa194f6527238b20f0bd2b786d1aee406cbd2eeebec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525361338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7af0a2d73eaeccf8d6915e53b71e65fdf4eed6e9a72555799fb7cbc598264`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff825649a77bf8ba74c15fc4f976ccf2d59f2ce97c5943ad492917d7f4e71b70`  
		Last Modified: Wed, 24 Jul 2024 17:46:16 GMT  
		Size: 87.3 MB (87328529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1` - unknown; unknown

```console
$ docker pull spark@sha256:e99471365b803ed4195f0a4902c854375ab64780a0f13a2109a616117942f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def03a0083c56021bc6eeb831d52d476c56c8acda6fbc9ee7ea87c1f51dea7c1`

```dockerfile
```

-	Layers:
	-	`sha256:821e9024d5ba5d90562d11b8f761ada7ec8425f614f99b9fbf3cec61643e1eb5`  
		Last Modified: Wed, 24 Jul 2024 17:46:14 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9767794f3d8cefe157caafb77e0d01162009a57cd6b0e7cdfb0d93d85f8a2dd7`  
		Last Modified: Wed, 24 Jul 2024 17:46:13 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-java17`

```console
$ docker pull spark@sha256:09e9037d3b0d8004982a97769249cce750a87e53412b80c386fcc92c75a01682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17` - linux; amd64

```console
$ docker pull spark@sha256:5b20d4acddf622278771505762961e0a5a6bbb2b5d3e217e5cf17f5b176c78b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558237741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff083f99b47dcc0dd3c244cbc94567cba0082f837b5321e3273fc60a63e3e07`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be391528e0568d45fa2c2e7979973a35405a1fea1061dae36ef25a595a87ff`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17` - unknown; unknown

```console
$ docker pull spark@sha256:6937ff3390bb6a9c72efce84f9d2e5d15bfb0fc29aa54f18828161e46e3048bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388d3f8cccd9aa597029aada345c714cb99e527ab055e66b09a72cfd4aabf75`

```dockerfile
```

-	Layers:
	-	`sha256:0188049db488542bfa5dcf97f6060e99f7b5e5c15bdc72ff340912050df41efb`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 9.7 MB (9738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdef03fb97752abe7bfec9d5c9d060e8949bc9bc8bf4791bbf7ecb8ef800c6b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:28 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae958a7906486de066c7cfeb38de935b3b621f8c285f5af0c6a2930fff27e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551313767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9d9af8f590887974192aa67217786d59f11300e79a8fb1946470f5198fe4e7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4e42f2e5bb2668fbc5fb276127e60a8fccd498f379574064fa9c172d873b3e`  
		Last Modified: Wed, 24 Jul 2024 13:40:17 GMT  
		Size: 114.3 MB (114304649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17` - unknown; unknown

```console
$ docker pull spark@sha256:88d518211d0607550c0913bfd1fe426bdf75de65d62d90e6964fa2e37baddc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd366026542bb0b33534e066dbb1db02077740759f46c79007d7a82e60b677ce`

```dockerfile
```

-	Layers:
	-	`sha256:d3c29183fa59de1275fec91e8e02c30ca71cc9fa25054a7391d6ae215997f0c0`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 9.7 MB (9733543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b11412dc0f90f910fa4a91be2f405cc8013c5516ba85b46ef424c9ed3d7a0d`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-java17-python3`

```console
$ docker pull spark@sha256:09e9037d3b0d8004982a97769249cce750a87e53412b80c386fcc92c75a01682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:5b20d4acddf622278771505762961e0a5a6bbb2b5d3e217e5cf17f5b176c78b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558237741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff083f99b47dcc0dd3c244cbc94567cba0082f837b5321e3273fc60a63e3e07`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be391528e0568d45fa2c2e7979973a35405a1fea1061dae36ef25a595a87ff`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:6937ff3390bb6a9c72efce84f9d2e5d15bfb0fc29aa54f18828161e46e3048bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388d3f8cccd9aa597029aada345c714cb99e527ab055e66b09a72cfd4aabf75`

```dockerfile
```

-	Layers:
	-	`sha256:0188049db488542bfa5dcf97f6060e99f7b5e5c15bdc72ff340912050df41efb`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 9.7 MB (9738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdef03fb97752abe7bfec9d5c9d060e8949bc9bc8bf4791bbf7ecb8ef800c6b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:28 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae958a7906486de066c7cfeb38de935b3b621f8c285f5af0c6a2930fff27e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551313767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9d9af8f590887974192aa67217786d59f11300e79a8fb1946470f5198fe4e7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4e42f2e5bb2668fbc5fb276127e60a8fccd498f379574064fa9c172d873b3e`  
		Last Modified: Wed, 24 Jul 2024 13:40:17 GMT  
		Size: 114.3 MB (114304649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:88d518211d0607550c0913bfd1fe426bdf75de65d62d90e6964fa2e37baddc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd366026542bb0b33534e066dbb1db02077740759f46c79007d7a82e60b677ce`

```dockerfile
```

-	Layers:
	-	`sha256:d3c29183fa59de1275fec91e8e02c30ca71cc9fa25054a7391d6ae215997f0c0`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 9.7 MB (9733543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b11412dc0f90f910fa4a91be2f405cc8013c5516ba85b46ef424c9ed3d7a0d`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-java17-r`

```console
$ docker pull spark@sha256:a0b316109830e4ffc8bd742f30d8bdbd808f8fde777a8c33e879741d1fe163c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:81a627d59c49515538e5bab1cdf84168a5ccae6281c81c3f4381f1edbbd0f91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763802252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f4b68ed28dc26e180790d2d01146c61a49514b118f11c99e8758bd269967bd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c93fcadfaf6e316d539ca44d02cf480de1771391384eb161f6bcc02347e0e`  
		Last Modified: Tue, 23 Jul 2024 03:05:16 GMT  
		Size: 323.8 MB (323832040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:b6df580221b2a535d4753eaf9af3e5c958137abd33d380c98e1b55cb4b8f9695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2bd94fdd77b4935de1be0d19c78541d9a580214434d11a7240ce1dd3e1ff85`

```dockerfile
```

-	Layers:
	-	`sha256:d919b3f1ee9203d72dc5272708d48a07c8231a6524d2eed86ae249cbe7f02bbf`  
		Last Modified: Tue, 23 Jul 2024 03:05:12 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5d8d296e976908bb419af6d5111d23c43799f7d11fea68040099260b012956`  
		Last Modified: Tue, 23 Jul 2024 03:05:11 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3a7ae18a0309bd4dea1cb3f1757c86dbf1d3e4b2b8c4eec22b603ff466891c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.5 MB (745518562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd7e587327ffc5676b1a1c92fd25a5dd2f2137b55e1f77aa6a671c52cbe20a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8a45d62f9ef347fc874f47b07f944b29041327131c6237e0c3edad8c76e722`  
		Last Modified: Wed, 24 Jul 2024 13:42:32 GMT  
		Size: 308.5 MB (308509444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:ef270f609d8c2021450652f90f6b862d6c33b6f79c621d7f8c1c97a30c47a737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d848ebe798b3659765d213170cb37e8757c8d0dc4fc4e081b3a57f468d268779`

```dockerfile
```

-	Layers:
	-	`sha256:6b9c994308ad2c098252d9a1124e35796e18d922b665502f78f6539f89f557a9`  
		Last Modified: Wed, 24 Jul 2024 13:42:26 GMT  
		Size: 17.7 MB (17730394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46cc1678daf6dc428cbe28d5517b73d4dc5031907a80a081801a98d61ceebbba`  
		Last Modified: Wed, 24 Jul 2024 13:42:25 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-java17-scala`

```console
$ docker pull spark@sha256:c7cce8f600ab0a579ad07acdc9ea31d5b28fd628297248e67016f288477f860c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:a39e2b5ec180cebfafd468a58b76fa79d214bf81e4610efaac1b687a06d7fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 MB (439970212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6307b9b4a9b98780cb305341084aff9dff03affc496bc9f8dc503020019e051`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:57e9f77f247465b3c6e75682c82e33e4bdab0ce89afc2ea8245d339ea53c0a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7741eb2d029d03b483d9073e2018b71e28f7830b50413aab93feea1f827fd`

```dockerfile
```

-	Layers:
	-	`sha256:31231ac9c67b8e3c802a02c120c746e4563ec6a7038b3b5a292a329b1314b46b`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d18d6d994a430f4f1df86b22a2984223a60ac20f2f333515817e04e5bfc9d`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 22.4 KB (22420 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b6af3cb64cd901f0ac86c39b72fe732da1f5ca03fd1863b58ad61769502c6965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (437009118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3029b109a2589b5300cda5bda87cfb6a21e7158457b6aaea4d1421928925285c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:735808f67a0ce721d9b41fef6bb4c12e58fc7e74f1e5e40cef5dfffed7f737a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b34cc5a2b96df88cf5353f5686d2510a245c77dc0cd0e0fdb4e3a01f4d045b`

```dockerfile
```

-	Layers:
	-	`sha256:961ebc93fad36a0551a611434c850a4e2b030940d439ea207f2b167664f62aa8`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56074a0894bfb2850308233701566c1719103ba246aaecfac2160633662f8bc`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-python3`

```console
$ docker pull spark@sha256:949e41e69700ce48a7e9ed2422d9466aa0dd53ea596a32ba4bde5a481f3e80cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:ffa3e64ad80d524e876abf809dba60919bde26b210b267bbe8e8764ab86c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535849031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f600e30f900b5b7744276f4368820140c76743aa51f0f6eee316b899fb0130`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c6966f4aad89717ff3771ce987c0d71548ce56fc036157b92b0fda5f4c373`  
		Last Modified: Wed, 24 Jul 2024 04:04:09 GMT  
		Size: 94.4 MB (94378969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:116f98af3fd6c41c3cb7c31f81eb1e27c09adee21b16059d0a471bf84f27f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d66c8df5936e909d91c350ad73075d785568aaf206f7288437adbb8c3d706`

```dockerfile
```

-	Layers:
	-	`sha256:67e2c0b0979c518cb212345bc7a57cb8dcf515145a8317b340e58add19d567a5`  
		Last Modified: Wed, 24 Jul 2024 04:04:08 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193ed5fa925a5ea45c09bd3e84ae93f61ecf87f79ead30d5a2fdc2bee1fd4ed8`  
		Last Modified: Wed, 24 Jul 2024 04:04:07 GMT  
		Size: 11.5 KB (11528 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:210cfe7e5338d8abadc85fa194f6527238b20f0bd2b786d1aee406cbd2eeebec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525361338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7af0a2d73eaeccf8d6915e53b71e65fdf4eed6e9a72555799fb7cbc598264`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff825649a77bf8ba74c15fc4f976ccf2d59f2ce97c5943ad492917d7f4e71b70`  
		Last Modified: Wed, 24 Jul 2024 17:46:16 GMT  
		Size: 87.3 MB (87328529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:e99471365b803ed4195f0a4902c854375ab64780a0f13a2109a616117942f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def03a0083c56021bc6eeb831d52d476c56c8acda6fbc9ee7ea87c1f51dea7c1`

```dockerfile
```

-	Layers:
	-	`sha256:821e9024d5ba5d90562d11b8f761ada7ec8425f614f99b9fbf3cec61643e1eb5`  
		Last Modified: Wed, 24 Jul 2024 17:46:14 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9767794f3d8cefe157caafb77e0d01162009a57cd6b0e7cdfb0d93d85f8a2dd7`  
		Last Modified: Wed, 24 Jul 2024 17:46:13 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-r`

```console
$ docker pull spark@sha256:914e677f7def1b7f4e790f4366f5d39157efcc742f878a4a86e1c14614f1dc36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-r` - linux; amd64

```console
$ docker pull spark@sha256:34f22d270af328afdd34f17b420f72c17d8a39b3b3c012780575b75fc01db951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673782262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb6e39b0602722862cc27652edae7bf2933eac82b11cf877c76d206aa445ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba554b0fe77763624eb139886abaf076009c7a459f4d863938de9e2d4d78577`  
		Last Modified: Wed, 24 Jul 2024 04:04:37 GMT  
		Size: 232.3 MB (232312200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:35a06afa58e827281fe62c6d1e6689990cabc30041c752ea60b8692fd340b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b658da12608f71ef99b38c90020c22d419470b9946ef67df976e69dd9a2668b`

```dockerfile
```

-	Layers:
	-	`sha256:47831f4c4619ad9d05d075146f9b6c762bcf61e02ccd7401a8dbfaaf5dd7502b`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 11.1 MB (11093057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5d097d96b4c4d524559593076b339b7b86bcc83edf0628e9a7823dc31f2630`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:900a363ed22f78bac4276bf5b621e5ab4bba214506741f47cb31de6527646115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651556115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506dfa3bd267a5f1e792592ca06ed56e9198afd9d135d80c23596d471cd2bbd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed5fc9d0dfd624efc95555b0dc242c4960af5ead88ae18ceba19843973cacd`  
		Last Modified: Wed, 24 Jul 2024 17:47:56 GMT  
		Size: 213.5 MB (213523306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:0d08f8800907ce35dad2d0c9631f4b28ae9be9f703ed876329a2388ebb0dc7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dba68effc14643c2a78973cfcb5e92e232839da2820808a5e45fc1b98c18ce`

```dockerfile
```

-	Layers:
	-	`sha256:f3e171c38dfbcb2e568a45b0ed3ecb7fbbaa059e9430c4842ba95d5c55791bd9`  
		Last Modified: Wed, 24 Jul 2024 17:47:51 GMT  
		Size: 11.1 MB (11077508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:064952329f0bbbcd24824eb0dbce821f4902b4318c37f8bc0977ed825f3d4e61`  
		Last Modified: Wed, 24 Jul 2024 17:47:50 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala`

```console
$ docker pull spark@sha256:a2a67aee0b1ede62bba596e6b527d6e8675082828e8cfb5f754c3b3c4bf7ed89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:b3c88206ba9c4f18b52fa6c48850884e1121511840c62901db9bb477c9d221b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441470062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264755707daac00848a07620bd739a3b2877208f56e3f6d9485889818709b8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:7ed1cf4dcd5311eb43687fce8cccaf1ff0319249d5c41a53e135d25a9bcf1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7056533e38deffacc1132d59f8a5d47adfc76f9ccfc36ca98d3d26af0aea34a`

```dockerfile
```

-	Layers:
	-	`sha256:a667c347527d146dbc4c8ccea57e03f9c37ec0bdc9d2188d168927e27b6c7fa7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 4.2 MB (4215629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40f3b6637e9413897114f4ca1e9f8d4c953da75e7750575565fae7cf001ab6c`  
		Last Modified: Wed, 24 Jul 2024 03:07:48 GMT  
		Size: 22.7 KB (22701 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ee5517a34a6ffb2e376e5f8611decbf537371086349d21b760c7d9f3bdeb2c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438032809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a9722c6464b514a6c4d68040e136d687f321e559b5563d949c63bd4ef3288`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:a15e3a5be64b99ccce0567ee1268695f9c4824f2510664c9cb6f7e6930c06111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be2ba2dadea0316672f0278a8f49282dbe01dd429f1f29c11a8ed63bf2b191b`

```dockerfile
```

-	Layers:
	-	`sha256:69a61f3d33eeec536b9fc8d373a0020bc4314b5199339970c3d76bab1ec0536b`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 4.2 MB (4215906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec679dd5baa6991c4a15ec481e116c0e4ed71b1c895a615cb37453098dd40326`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 23.0 KB (23006 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:a7ac492f6bb0c92df1b87e41aaa52bc65c25c39fc65b39b3f55c19e601b7554a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:8fa32ff98a7770922c8b445f0967217e43e2b4504dea45f4e3a56a7417577239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.4 MB (695410675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f18ae879f96a3013fb1bd21220b23230ff11807ac1363cb8866f3762ad75f2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7e557e3156ff2f2749c475d599776917771e3af20425ef7af707b0ab6549ab`  
		Last Modified: Wed, 24 Jul 2024 04:04:48 GMT  
		Size: 253.9 MB (253940613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:20785427e0d73ca0868ff97ff3aa804b0b40017c0164567490dc04edc1f8bf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0a8120dacdee6e7ecbfef423d177d5aa7dfa5fd7f9b0f9fee92f5e412e3402`

```dockerfile
```

-	Layers:
	-	`sha256:7553f4af80565a8d3f723dd075430f6d3b266b4ef8d9497c0cd2cdcd54a61b41`  
		Last Modified: Wed, 24 Jul 2024 04:04:44 GMT  
		Size: 12.2 MB (12215947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce81c79c444288dc5d82e730e9d57ed028528a4e8f8167d93eed8bddc6860c19`  
		Last Modified: Wed, 24 Jul 2024 04:04:44 GMT  
		Size: 10.5 KB (10509 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:dca9644ec07241a0d6c3646e7d3c2029db48f6f6e02e443a250fc7504a5d669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.2 MB (673188840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f3dfe4f0f92c4b11f24bf06a9fb6ff1b2cf8e7dcf183ecc9742087a6486415`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5921642d7c5b04f43e7946cd681dc99b0fe63c1de44c80ecad1a3b8dfd6733`  
		Last Modified: Wed, 24 Jul 2024 17:41:17 GMT  
		Size: 235.2 MB (235156031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:195f5ce0b1fe8a382571adbd542e468e4568396cf3ffdce999097cac08d89a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12211359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845322e8870be36ab9d0d8d0bbdb56fc4096411d75f95d2396d21313f050262e`

```dockerfile
```

-	Layers:
	-	`sha256:81d4765487d07b3b3c54f9ea01dcd972d0f922b9bb9cab6cf5de2508ec7425a0`  
		Last Modified: Wed, 24 Jul 2024 17:41:12 GMT  
		Size: 12.2 MB (12200441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07e052fa139139bf3002a294e45d637037326fea5dd97c59d3445bc544cd739`  
		Last Modified: Wed, 24 Jul 2024 17:41:11 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:949e41e69700ce48a7e9ed2422d9466aa0dd53ea596a32ba4bde5a481f3e80cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:ffa3e64ad80d524e876abf809dba60919bde26b210b267bbe8e8764ab86c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535849031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f600e30f900b5b7744276f4368820140c76743aa51f0f6eee316b899fb0130`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c6966f4aad89717ff3771ce987c0d71548ce56fc036157b92b0fda5f4c373`  
		Last Modified: Wed, 24 Jul 2024 04:04:09 GMT  
		Size: 94.4 MB (94378969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:116f98af3fd6c41c3cb7c31f81eb1e27c09adee21b16059d0a471bf84f27f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d66c8df5936e909d91c350ad73075d785568aaf206f7288437adbb8c3d706`

```dockerfile
```

-	Layers:
	-	`sha256:67e2c0b0979c518cb212345bc7a57cb8dcf515145a8317b340e58add19d567a5`  
		Last Modified: Wed, 24 Jul 2024 04:04:08 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193ed5fa925a5ea45c09bd3e84ae93f61ecf87f79ead30d5a2fdc2bee1fd4ed8`  
		Last Modified: Wed, 24 Jul 2024 04:04:07 GMT  
		Size: 11.5 KB (11528 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:210cfe7e5338d8abadc85fa194f6527238b20f0bd2b786d1aee406cbd2eeebec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525361338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7af0a2d73eaeccf8d6915e53b71e65fdf4eed6e9a72555799fb7cbc598264`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff825649a77bf8ba74c15fc4f976ccf2d59f2ce97c5943ad492917d7f4e71b70`  
		Last Modified: Wed, 24 Jul 2024 17:46:16 GMT  
		Size: 87.3 MB (87328529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e99471365b803ed4195f0a4902c854375ab64780a0f13a2109a616117942f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def03a0083c56021bc6eeb831d52d476c56c8acda6fbc9ee7ea87c1f51dea7c1`

```dockerfile
```

-	Layers:
	-	`sha256:821e9024d5ba5d90562d11b8f761ada7ec8425f614f99b9fbf3cec61643e1eb5`  
		Last Modified: Wed, 24 Jul 2024 17:46:14 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9767794f3d8cefe157caafb77e0d01162009a57cd6b0e7cdfb0d93d85f8a2dd7`  
		Last Modified: Wed, 24 Jul 2024 17:46:13 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:914e677f7def1b7f4e790f4366f5d39157efcc742f878a4a86e1c14614f1dc36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:34f22d270af328afdd34f17b420f72c17d8a39b3b3c012780575b75fc01db951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673782262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb6e39b0602722862cc27652edae7bf2933eac82b11cf877c76d206aa445ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba554b0fe77763624eb139886abaf076009c7a459f4d863938de9e2d4d78577`  
		Last Modified: Wed, 24 Jul 2024 04:04:37 GMT  
		Size: 232.3 MB (232312200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:35a06afa58e827281fe62c6d1e6689990cabc30041c752ea60b8692fd340b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b658da12608f71ef99b38c90020c22d419470b9946ef67df976e69dd9a2668b`

```dockerfile
```

-	Layers:
	-	`sha256:47831f4c4619ad9d05d075146f9b6c762bcf61e02ccd7401a8dbfaaf5dd7502b`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 11.1 MB (11093057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5d097d96b4c4d524559593076b339b7b86bcc83edf0628e9a7823dc31f2630`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:900a363ed22f78bac4276bf5b621e5ab4bba214506741f47cb31de6527646115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651556115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506dfa3bd267a5f1e792592ca06ed56e9198afd9d135d80c23596d471cd2bbd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed5fc9d0dfd624efc95555b0dc242c4960af5ead88ae18ceba19843973cacd`  
		Last Modified: Wed, 24 Jul 2024 17:47:56 GMT  
		Size: 213.5 MB (213523306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0d08f8800907ce35dad2d0c9631f4b28ae9be9f703ed876329a2388ebb0dc7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dba68effc14643c2a78973cfcb5e92e232839da2820808a5e45fc1b98c18ce`

```dockerfile
```

-	Layers:
	-	`sha256:f3e171c38dfbcb2e568a45b0ed3ecb7fbbaa059e9430c4842ba95d5c55791bd9`  
		Last Modified: Wed, 24 Jul 2024 17:47:51 GMT  
		Size: 11.1 MB (11077508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:064952329f0bbbcd24824eb0dbce821f4902b4318c37f8bc0977ed825f3d4e61`  
		Last Modified: Wed, 24 Jul 2024 17:47:50 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:a2a67aee0b1ede62bba596e6b527d6e8675082828e8cfb5f754c3b3c4bf7ed89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:b3c88206ba9c4f18b52fa6c48850884e1121511840c62901db9bb477c9d221b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441470062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264755707daac00848a07620bd739a3b2877208f56e3f6d9485889818709b8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7ed1cf4dcd5311eb43687fce8cccaf1ff0319249d5c41a53e135d25a9bcf1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7056533e38deffacc1132d59f8a5d47adfc76f9ccfc36ca98d3d26af0aea34a`

```dockerfile
```

-	Layers:
	-	`sha256:a667c347527d146dbc4c8ccea57e03f9c37ec0bdc9d2188d168927e27b6c7fa7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 4.2 MB (4215629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40f3b6637e9413897114f4ca1e9f8d4c953da75e7750575565fae7cf001ab6c`  
		Last Modified: Wed, 24 Jul 2024 03:07:48 GMT  
		Size: 22.7 KB (22701 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ee5517a34a6ffb2e376e5f8611decbf537371086349d21b760c7d9f3bdeb2c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438032809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a9722c6464b514a6c4d68040e136d687f321e559b5563d949c63bd4ef3288`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a15e3a5be64b99ccce0567ee1268695f9c4824f2510664c9cb6f7e6930c06111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be2ba2dadea0316672f0278a8f49282dbe01dd429f1f29c11a8ed63bf2b191b`

```dockerfile
```

-	Layers:
	-	`sha256:69a61f3d33eeec536b9fc8d373a0020bc4314b5199339970c3d76bab1ec0536b`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 4.2 MB (4215906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec679dd5baa6991c4a15ec481e116c0e4ed71b1c895a615cb37453098dd40326`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 23.0 KB (23006 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:21a3c3b2a62583bb3460b20bc347518dc37f2f0db0c19f159c45f9e11a40416d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bd0ba33604f7064e1f782cccb7bdb0ff03a9ed8fe7d2932070b3e8db1f2fd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.5 MB (778516383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af11b3a0a8bf000677124f6dcd64638b7e2c95cb6c827f1b695ca1019c562971`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031658dc0239c229cb8b2bdc84ff486a9f259b9a4151071b6acce38a286a886`  
		Last Modified: Tue, 23 Jul 2024 03:05:50 GMT  
		Size: 338.5 MB (338546171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a9b18ad2484994a458b4fb58fca93301872c0f2b179868006e0446df4c7bdca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad2061e0dba06f4d7daad5f08f913fffe6a7e4d3bc2ea7e19de10487eaaf02`

```dockerfile
```

-	Layers:
	-	`sha256:21ceacd0fac6efc6f5567453152badd1e8b03d40025c34fbe99cab342ad989c3`  
		Last Modified: Tue, 23 Jul 2024 03:05:31 GMT  
		Size: 18.8 MB (18775974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504884bbcdf170701fceab469e3fb597ba22aed83e528af13d95ada61c2355b5`  
		Last Modified: Tue, 23 Jul 2024 03:05:29 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8de53b8a9e6a47e07fb35d9bd96316221c7da82c06d9a18360de02fac4680423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.1 MB (760052988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e99d1787883f860c99dee16ddf8cf52e3ad79f43f788ddfa243c58a3e8880`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d921983a0a3420ed5fe2f3427f3aa4a00dec5ff3bd71403c494658c9bccb4f5`  
		Last Modified: Wed, 24 Jul 2024 13:22:01 GMT  
		Size: 323.0 MB (323043870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:29380da39fd161889c0fc02b9280c93e42389f8fcf0d70235dc5dc5b4c3c329b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18753245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa9f7307407e2f965ed84a5b67e0d0274a1b9fafdd3b4cc1d0d9ff5f719d094`

```dockerfile
```

-	Layers:
	-	`sha256:5eaa772e1e161ea18f2ad0973f1e40cd35b026e039824bbb37535941b8a49de6`  
		Last Modified: Wed, 24 Jul 2024 13:21:55 GMT  
		Size: 18.7 MB (18742326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd3c7aa83854a8d15c61dd8fbc598b9891a5512c1cf8c6dfb692fe48cb8558d`  
		Last Modified: Wed, 24 Jul 2024 13:21:53 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:09e9037d3b0d8004982a97769249cce750a87e53412b80c386fcc92c75a01682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5b20d4acddf622278771505762961e0a5a6bbb2b5d3e217e5cf17f5b176c78b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558237741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff083f99b47dcc0dd3c244cbc94567cba0082f837b5321e3273fc60a63e3e07`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be391528e0568d45fa2c2e7979973a35405a1fea1061dae36ef25a595a87ff`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6937ff3390bb6a9c72efce84f9d2e5d15bfb0fc29aa54f18828161e46e3048bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388d3f8cccd9aa597029aada345c714cb99e527ab055e66b09a72cfd4aabf75`

```dockerfile
```

-	Layers:
	-	`sha256:0188049db488542bfa5dcf97f6060e99f7b5e5c15bdc72ff340912050df41efb`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 9.7 MB (9738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdef03fb97752abe7bfec9d5c9d060e8949bc9bc8bf4791bbf7ecb8ef800c6b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:28 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae958a7906486de066c7cfeb38de935b3b621f8c285f5af0c6a2930fff27e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551313767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9d9af8f590887974192aa67217786d59f11300e79a8fb1946470f5198fe4e7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4e42f2e5bb2668fbc5fb276127e60a8fccd498f379574064fa9c172d873b3e`  
		Last Modified: Wed, 24 Jul 2024 13:40:17 GMT  
		Size: 114.3 MB (114304649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:88d518211d0607550c0913bfd1fe426bdf75de65d62d90e6964fa2e37baddc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd366026542bb0b33534e066dbb1db02077740759f46c79007d7a82e60b677ce`

```dockerfile
```

-	Layers:
	-	`sha256:d3c29183fa59de1275fec91e8e02c30ca71cc9fa25054a7391d6ae215997f0c0`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 9.7 MB (9733543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b11412dc0f90f910fa4a91be2f405cc8013c5516ba85b46ef424c9ed3d7a0d`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:a0b316109830e4ffc8bd742f30d8bdbd808f8fde777a8c33e879741d1fe163c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:81a627d59c49515538e5bab1cdf84168a5ccae6281c81c3f4381f1edbbd0f91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763802252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f4b68ed28dc26e180790d2d01146c61a49514b118f11c99e8758bd269967bd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c93fcadfaf6e316d539ca44d02cf480de1771391384eb161f6bcc02347e0e`  
		Last Modified: Tue, 23 Jul 2024 03:05:16 GMT  
		Size: 323.8 MB (323832040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b6df580221b2a535d4753eaf9af3e5c958137abd33d380c98e1b55cb4b8f9695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2bd94fdd77b4935de1be0d19c78541d9a580214434d11a7240ce1dd3e1ff85`

```dockerfile
```

-	Layers:
	-	`sha256:d919b3f1ee9203d72dc5272708d48a07c8231a6524d2eed86ae249cbe7f02bbf`  
		Last Modified: Tue, 23 Jul 2024 03:05:12 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5d8d296e976908bb419af6d5111d23c43799f7d11fea68040099260b012956`  
		Last Modified: Tue, 23 Jul 2024 03:05:11 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:3a7ae18a0309bd4dea1cb3f1757c86dbf1d3e4b2b8c4eec22b603ff466891c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.5 MB (745518562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd7e587327ffc5676b1a1c92fd25a5dd2f2137b55e1f77aa6a671c52cbe20a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8a45d62f9ef347fc874f47b07f944b29041327131c6237e0c3edad8c76e722`  
		Last Modified: Wed, 24 Jul 2024 13:42:32 GMT  
		Size: 308.5 MB (308509444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ef270f609d8c2021450652f90f6b862d6c33b6f79c621d7f8c1c97a30c47a737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d848ebe798b3659765d213170cb37e8757c8d0dc4fc4e081b3a57f468d268779`

```dockerfile
```

-	Layers:
	-	`sha256:6b9c994308ad2c098252d9a1124e35796e18d922b665502f78f6539f89f557a9`  
		Last Modified: Wed, 24 Jul 2024 13:42:26 GMT  
		Size: 17.7 MB (17730394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46cc1678daf6dc428cbe28d5517b73d4dc5031907a80a081801a98d61ceebbba`  
		Last Modified: Wed, 24 Jul 2024 13:42:25 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:c7cce8f600ab0a579ad07acdc9ea31d5b28fd628297248e67016f288477f860c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a39e2b5ec180cebfafd468a58b76fa79d214bf81e4610efaac1b687a06d7fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 MB (439970212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6307b9b4a9b98780cb305341084aff9dff03affc496bc9f8dc503020019e051`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:57e9f77f247465b3c6e75682c82e33e4bdab0ce89afc2ea8245d339ea53c0a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7741eb2d029d03b483d9073e2018b71e28f7830b50413aab93feea1f827fd`

```dockerfile
```

-	Layers:
	-	`sha256:31231ac9c67b8e3c802a02c120c746e4563ec6a7038b3b5a292a329b1314b46b`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d18d6d994a430f4f1df86b22a2984223a60ac20f2f333515817e04e5bfc9d`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 22.4 KB (22420 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b6af3cb64cd901f0ac86c39b72fe732da1f5ca03fd1863b58ad61769502c6965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (437009118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3029b109a2589b5300cda5bda87cfb6a21e7158457b6aaea4d1421928925285c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:735808f67a0ce721d9b41fef6bb4c12e58fc7e74f1e5e40cef5dfffed7f737a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b34cc5a2b96df88cf5353f5686d2510a245c77dc0cd0e0fdb4e3a01f4d045b`

```dockerfile
```

-	Layers:
	-	`sha256:961ebc93fad36a0551a611434c850a4e2b030940d439ea207f2b167664f62aa8`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56074a0894bfb2850308233701566c1719103ba246aaecfac2160633662f8bc`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:949e41e69700ce48a7e9ed2422d9466aa0dd53ea596a32ba4bde5a481f3e80cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:ffa3e64ad80d524e876abf809dba60919bde26b210b267bbe8e8764ab86c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535849031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f600e30f900b5b7744276f4368820140c76743aa51f0f6eee316b899fb0130`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c6966f4aad89717ff3771ce987c0d71548ce56fc036157b92b0fda5f4c373`  
		Last Modified: Wed, 24 Jul 2024 04:04:09 GMT  
		Size: 94.4 MB (94378969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:116f98af3fd6c41c3cb7c31f81eb1e27c09adee21b16059d0a471bf84f27f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d66c8df5936e909d91c350ad73075d785568aaf206f7288437adbb8c3d706`

```dockerfile
```

-	Layers:
	-	`sha256:67e2c0b0979c518cb212345bc7a57cb8dcf515145a8317b340e58add19d567a5`  
		Last Modified: Wed, 24 Jul 2024 04:04:08 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193ed5fa925a5ea45c09bd3e84ae93f61ecf87f79ead30d5a2fdc2bee1fd4ed8`  
		Last Modified: Wed, 24 Jul 2024 04:04:07 GMT  
		Size: 11.5 KB (11528 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:210cfe7e5338d8abadc85fa194f6527238b20f0bd2b786d1aee406cbd2eeebec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525361338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7af0a2d73eaeccf8d6915e53b71e65fdf4eed6e9a72555799fb7cbc598264`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff825649a77bf8ba74c15fc4f976ccf2d59f2ce97c5943ad492917d7f4e71b70`  
		Last Modified: Wed, 24 Jul 2024 17:46:16 GMT  
		Size: 87.3 MB (87328529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:e99471365b803ed4195f0a4902c854375ab64780a0f13a2109a616117942f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def03a0083c56021bc6eeb831d52d476c56c8acda6fbc9ee7ea87c1f51dea7c1`

```dockerfile
```

-	Layers:
	-	`sha256:821e9024d5ba5d90562d11b8f761ada7ec8425f614f99b9fbf3cec61643e1eb5`  
		Last Modified: Wed, 24 Jul 2024 17:46:14 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9767794f3d8cefe157caafb77e0d01162009a57cd6b0e7cdfb0d93d85f8a2dd7`  
		Last Modified: Wed, 24 Jul 2024 17:46:13 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:949e41e69700ce48a7e9ed2422d9466aa0dd53ea596a32ba4bde5a481f3e80cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:ffa3e64ad80d524e876abf809dba60919bde26b210b267bbe8e8764ab86c1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535849031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f600e30f900b5b7744276f4368820140c76743aa51f0f6eee316b899fb0130`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c6966f4aad89717ff3771ce987c0d71548ce56fc036157b92b0fda5f4c373`  
		Last Modified: Wed, 24 Jul 2024 04:04:09 GMT  
		Size: 94.4 MB (94378969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:116f98af3fd6c41c3cb7c31f81eb1e27c09adee21b16059d0a471bf84f27f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d66c8df5936e909d91c350ad73075d785568aaf206f7288437adbb8c3d706`

```dockerfile
```

-	Layers:
	-	`sha256:67e2c0b0979c518cb212345bc7a57cb8dcf515145a8317b340e58add19d567a5`  
		Last Modified: Wed, 24 Jul 2024 04:04:08 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193ed5fa925a5ea45c09bd3e84ae93f61ecf87f79ead30d5a2fdc2bee1fd4ed8`  
		Last Modified: Wed, 24 Jul 2024 04:04:07 GMT  
		Size: 11.5 KB (11528 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:210cfe7e5338d8abadc85fa194f6527238b20f0bd2b786d1aee406cbd2eeebec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525361338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7af0a2d73eaeccf8d6915e53b71e65fdf4eed6e9a72555799fb7cbc598264`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff825649a77bf8ba74c15fc4f976ccf2d59f2ce97c5943ad492917d7f4e71b70`  
		Last Modified: Wed, 24 Jul 2024 17:46:16 GMT  
		Size: 87.3 MB (87328529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:e99471365b803ed4195f0a4902c854375ab64780a0f13a2109a616117942f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def03a0083c56021bc6eeb831d52d476c56c8acda6fbc9ee7ea87c1f51dea7c1`

```dockerfile
```

-	Layers:
	-	`sha256:821e9024d5ba5d90562d11b8f761ada7ec8425f614f99b9fbf3cec61643e1eb5`  
		Last Modified: Wed, 24 Jul 2024 17:46:14 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9767794f3d8cefe157caafb77e0d01162009a57cd6b0e7cdfb0d93d85f8a2dd7`  
		Last Modified: Wed, 24 Jul 2024 17:46:13 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:09e9037d3b0d8004982a97769249cce750a87e53412b80c386fcc92c75a01682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:5b20d4acddf622278771505762961e0a5a6bbb2b5d3e217e5cf17f5b176c78b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558237741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff083f99b47dcc0dd3c244cbc94567cba0082f837b5321e3273fc60a63e3e07`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2789aebe161258ac11a859ccb5d0fb5b6ecf9f075a42b2624f658321c906a`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f9910a0d274ee1e7f26bcb9132577d3949cd10e517b242e3a2d0fc861af59`  
		Last Modified: Tue, 23 Jul 2024 02:04:10 GMT  
		Size: 24.9 MB (24890965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacfdfc7f6ff3498278728627b6a35caad10a0a2822142d9bcc6aaf9c84f3a93`  
		Last Modified: Tue, 23 Jul 2024 02:04:15 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1327eb429f7a96e90facc0bf762dd7475587e0e6c3d340e0315695e8fd51d86`  
		Last Modified: Tue, 23 Jul 2024 02:04:09 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be391528e0568d45fa2c2e7979973a35405a1fea1061dae36ef25a595a87ff`  
		Last Modified: Tue, 23 Jul 2024 03:04:32 GMT  
		Size: 118.3 MB (118267529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:6937ff3390bb6a9c72efce84f9d2e5d15bfb0fc29aa54f18828161e46e3048bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388d3f8cccd9aa597029aada345c714cb99e527ab055e66b09a72cfd4aabf75`

```dockerfile
```

-	Layers:
	-	`sha256:0188049db488542bfa5dcf97f6060e99f7b5e5c15bdc72ff340912050df41efb`  
		Last Modified: Tue, 23 Jul 2024 03:04:29 GMT  
		Size: 9.7 MB (9738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdef03fb97752abe7bfec9d5c9d060e8949bc9bc8bf4791bbf7ecb8ef800c6b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:28 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cae958a7906486de066c7cfeb38de935b3b621f8c285f5af0c6a2930fff27e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551313767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9d9af8f590887974192aa67217786d59f11300e79a8fb1946470f5198fe4e7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ff66bc0d2a892008f69c16fb9094aa7d25c2ba42a681fbb01a93859f2ac78`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aff32585fb314accc22c633590befd0da941ceef146d4267b38b1d9f78ae18`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce80bc940a98abc610627dac1176c12bf7623845c5c91fa592f911e2fa02d3`  
		Last Modified: Wed, 24 Jul 2024 08:36:20 GMT  
		Size: 24.6 MB (24560508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d893130d96dd42f81d18441c2507500843b6bd9fbbd2af6231e1e4cc6886c935`  
		Last Modified: Wed, 24 Jul 2024 08:36:26 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b4f7f9685fa3404e391a731cf89d6f792840bcbd08326467d3210b587b4fd`  
		Last Modified: Wed, 24 Jul 2024 08:36:19 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4e42f2e5bb2668fbc5fb276127e60a8fccd498f379574064fa9c172d873b3e`  
		Last Modified: Wed, 24 Jul 2024 13:40:17 GMT  
		Size: 114.3 MB (114304649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:88d518211d0607550c0913bfd1fe426bdf75de65d62d90e6964fa2e37baddc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd366026542bb0b33534e066dbb1db02077740759f46c79007d7a82e60b677ce`

```dockerfile
```

-	Layers:
	-	`sha256:d3c29183fa59de1275fec91e8e02c30ca71cc9fa25054a7391d6ae215997f0c0`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 9.7 MB (9733543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b11412dc0f90f910fa4a91be2f405cc8013c5516ba85b46ef424c9ed3d7a0d`  
		Last Modified: Wed, 24 Jul 2024 13:40:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:914e677f7def1b7f4e790f4366f5d39157efcc742f878a4a86e1c14614f1dc36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:34f22d270af328afdd34f17b420f72c17d8a39b3b3c012780575b75fc01db951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673782262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb6e39b0602722862cc27652edae7bf2933eac82b11cf877c76d206aa445ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba554b0fe77763624eb139886abaf076009c7a459f4d863938de9e2d4d78577`  
		Last Modified: Wed, 24 Jul 2024 04:04:37 GMT  
		Size: 232.3 MB (232312200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:35a06afa58e827281fe62c6d1e6689990cabc30041c752ea60b8692fd340b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b658da12608f71ef99b38c90020c22d419470b9946ef67df976e69dd9a2668b`

```dockerfile
```

-	Layers:
	-	`sha256:47831f4c4619ad9d05d075146f9b6c762bcf61e02ccd7401a8dbfaaf5dd7502b`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 11.1 MB (11093057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5d097d96b4c4d524559593076b339b7b86bcc83edf0628e9a7823dc31f2630`  
		Last Modified: Wed, 24 Jul 2024 04:04:34 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:900a363ed22f78bac4276bf5b621e5ab4bba214506741f47cb31de6527646115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651556115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506dfa3bd267a5f1e792592ca06ed56e9198afd9d135d80c23596d471cd2bbd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
USER root
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV R_HOME=/usr/lib/R
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed5fc9d0dfd624efc95555b0dc242c4960af5ead88ae18ceba19843973cacd`  
		Last Modified: Wed, 24 Jul 2024 17:47:56 GMT  
		Size: 213.5 MB (213523306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:0d08f8800907ce35dad2d0c9631f4b28ae9be9f703ed876329a2388ebb0dc7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dba68effc14643c2a78973cfcb5e92e232839da2820808a5e45fc1b98c18ce`

```dockerfile
```

-	Layers:
	-	`sha256:f3e171c38dfbcb2e568a45b0ed3ecb7fbbaa059e9430c4842ba95d5c55791bd9`  
		Last Modified: Wed, 24 Jul 2024 17:47:51 GMT  
		Size: 11.1 MB (11077508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:064952329f0bbbcd24824eb0dbce821f4902b4318c37f8bc0977ed825f3d4e61`  
		Last Modified: Wed, 24 Jul 2024 17:47:50 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:a2a67aee0b1ede62bba596e6b527d6e8675082828e8cfb5f754c3b3c4bf7ed89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:b3c88206ba9c4f18b52fa6c48850884e1121511840c62901db9bb477c9d221b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441470062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264755707daac00848a07620bd739a3b2877208f56e3f6d9485889818709b8e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6cec726e90127e0f7495956c17587524c52f160d7c1eb43b44b146ec26249`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91282fd6308de65152b0ab7c53a8aeb3e3585d36d2405c17a3195c9a7e51be0c`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08f90a69ee1728e6df5b50dc26986ca5a7eec8edaf677f0459cf45ecb1aae7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 24.3 MB (24280110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d54d7cf688add4f6e0b3eac57f670b0f4a478feddf06cb2566b58a6463838d`  
		Last Modified: Wed, 24 Jul 2024 03:07:53 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a6b52548b5ea776a293396b5c80bc64f7b6326d1672aeaf0a8f541167b29a4`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:7ed1cf4dcd5311eb43687fce8cccaf1ff0319249d5c41a53e135d25a9bcf1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7056533e38deffacc1132d59f8a5d47adfc76f9ccfc36ca98d3d26af0aea34a`

```dockerfile
```

-	Layers:
	-	`sha256:a667c347527d146dbc4c8ccea57e03f9c37ec0bdc9d2188d168927e27b6c7fa7`  
		Last Modified: Wed, 24 Jul 2024 03:07:49 GMT  
		Size: 4.2 MB (4215629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40f3b6637e9413897114f4ca1e9f8d4c953da75e7750575565fae7cf001ab6c`  
		Last Modified: Wed, 24 Jul 2024 03:07:48 GMT  
		Size: 22.7 KB (22701 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ee5517a34a6ffb2e376e5f8611decbf537371086349d21b760c7d9f3bdeb2c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438032809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a9722c6464b514a6c4d68040e136d687f321e559b5563d949c63bd4ef3288`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 01:49:01 GMT
ARG RELEASE
# Thu, 29 Feb 2024 01:49:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 01:49:01 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 29 Feb 2024 01:49:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 29 Feb 2024 01:49:01 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 29 Feb 2024 01:49:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 01:49:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 29 Feb 2024 01:49:01 GMT
ARG spark_uid=185
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz.asc GPG_KEY=FD3E84942E5E6106235A1D25BD356A9F8740E4FF
# Thu, 29 Feb 2024 01:49:01 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 29 Feb 2024 01:49:01 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 29 Feb 2024 01:49:01 GMT
WORKDIR /opt/spark/work-dir
# Thu, 29 Feb 2024 01:49:01 GMT
USER spark
# Thu, 29 Feb 2024 01:49:01 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12c24742f866d4f8d3900c4704ef8304b647071ab582c32a23facfcb9cfd56`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b8950a9287556d1c73492eee2e296677a4697e4f865eb4de55c3764c9b9fd`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa01a896bea31a0a3a3ad4b70f5a5fe3fad54f0806d5bc090980d3f98a6dbb8f`  
		Last Modified: Wed, 24 Jul 2024 13:24:43 GMT  
		Size: 24.0 MB (24005196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9fadbc5e3f1aeafaa051c22626bc2fb24263b594b5905a15e8ec60c793ad37`  
		Last Modified: Wed, 24 Jul 2024 13:24:49 GMT  
		Size: 324.5 MB (324482964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050cee4c3ceef58830fff6747445c89c700e637c17ffcdf9674d8c54f082876d`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:a15e3a5be64b99ccce0567ee1268695f9c4824f2510664c9cb6f7e6930c06111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be2ba2dadea0316672f0278a8f49282dbe01dd429f1f29c11a8ed63bf2b191b`

```dockerfile
```

-	Layers:
	-	`sha256:69a61f3d33eeec536b9fc8d373a0020bc4314b5199339970c3d76bab1ec0536b`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 4.2 MB (4215906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec679dd5baa6991c4a15ec481e116c0e4ed71b1c895a615cb37453098dd40326`  
		Last Modified: Wed, 24 Jul 2024 13:24:42 GMT  
		Size: 23.0 KB (23006 bytes)  
		MIME: application/vnd.in-toto+json
