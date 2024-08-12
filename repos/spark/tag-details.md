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
-	[`spark:3.5.2`](#spark352)
-	[`spark:3.5.2-java17`](#spark352-java17)
-	[`spark:3.5.2-java17-python3`](#spark352-java17-python3)
-	[`spark:3.5.2-java17-r`](#spark352-java17-r)
-	[`spark:3.5.2-java17-scala`](#spark352-java17-scala)
-	[`spark:3.5.2-python3`](#spark352-python3)
-	[`spark:3.5.2-r`](#spark352-r)
-	[`spark:3.5.2-scala`](#spark352-scala)
-	[`spark:3.5.2-scala2.12-java11-python3-r-ubuntu`](#spark352-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.2-scala2.12-java11-python3-ubuntu`](#spark352-scala212-java11-python3-ubuntu)
-	[`spark:3.5.2-scala2.12-java11-r-ubuntu`](#spark352-scala212-java11-r-ubuntu)
-	[`spark:3.5.2-scala2.12-java11-ubuntu`](#spark352-scala212-java11-ubuntu)
-	[`spark:3.5.2-scala2.12-java17-python3-r-ubuntu`](#spark352-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.2-scala2.12-java17-python3-ubuntu`](#spark352-scala212-java17-python3-ubuntu)
-	[`spark:3.5.2-scala2.12-java17-r-ubuntu`](#spark352-scala212-java17-r-ubuntu)
-	[`spark:3.5.2-scala2.12-java17-ubuntu`](#spark352-scala212-java17-ubuntu)
-	[`spark:4.0.0-preview1`](#spark400-preview1)
-	[`spark:4.0.0-preview1-python3`](#spark400-preview1-python3)
-	[`spark:4.0.0-preview1-r`](#spark400-preview1-r)
-	[`spark:4.0.0-preview1-scala`](#spark400-preview1-scala)
-	[`spark:4.0.0-preview1-scala2.13-java17-python3-r-ubuntu`](#spark400-preview1-scala213-java17-python3-r-ubuntu)
-	[`spark:4.0.0-preview1-scala2.13-java17-python3-ubuntu`](#spark400-preview1-scala213-java17-python3-ubuntu)
-	[`spark:4.0.0-preview1-scala2.13-java17-r-ubuntu`](#spark400-preview1-scala213-java17-r-ubuntu)
-	[`spark:4.0.0-preview1-scala2.13-java17-ubuntu`](#spark400-preview1-scala213-java17-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.4.1`

```console
$ docker pull spark@sha256:dce7e55e5ba3b9a0ca4a6900588570efac076598ebce8d3d85186a0e5eabb9bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1` - linux; amd64

```console
$ docker pull spark@sha256:7210fdc649081e3856e42fe2aed1042fe376823a6f3a4975f41cf5225ee350ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529249532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa5291206faba0099383f9a378683dc78d59bf8113dffd07848f9240a421533`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f22eb50d5d925ca0f81da6db343dbdc81aa611e812032056634628414f48a3`  
		Last Modified: Thu, 25 Jul 2024 20:09:20 GMT  
		Size: 94.4 MB (94377097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1` - unknown; unknown

```console
$ docker pull spark@sha256:b926196df80c5a7d862a90488ae71afe95f754cbd86cc7032bf7cc1a092008e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292d40861cc7dc89d7d70263469c35810ef43831d8c2857a16210e5cd2cf872`

```dockerfile
```

-	Layers:
	-	`sha256:09418961dcd7d74b2c7d2e39a17e27da2d656c41aead2f65639b7fa71e39df3e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e683ae3f9f327b13c93a69066b24e46e949b32c28b989d1dc3c43b9e9ba23e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:41466285cf8ea843fa3b3c94325dd7104683eda4ca5b0fa7211777c2c2b9bac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518759398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7625946dc98d5705557e5291d72b3d243c115ffce766463fbe341b12486f5d3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ee5e76db80c90568838c628d8d2d829c19b4dbfb03c0ba21bdc7c67222c57`  
		Last Modified: Fri, 26 Jul 2024 01:05:05 GMT  
		Size: 87.3 MB (87324289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1` - unknown; unknown

```console
$ docker pull spark@sha256:663131e879b7c3969172266de932037a884f105281a5433ed3cde65ccbc31d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e9f5ed76542e0d5265955f26f6ca2a3babd721ebfef2a50be74868b0e7f02e`

```dockerfile
```

-	Layers:
	-	`sha256:79c6cdf6d368d9de17fb3d8a24ad7baef0da1924aecfea1604724cd7fdd452c5`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6df2db9df8d6822e06b96d6a2183e6c79272432cd953f88690f6de0e12c0fed`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-python3`

```console
$ docker pull spark@sha256:dce7e55e5ba3b9a0ca4a6900588570efac076598ebce8d3d85186a0e5eabb9bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-python3` - linux; amd64

```console
$ docker pull spark@sha256:7210fdc649081e3856e42fe2aed1042fe376823a6f3a4975f41cf5225ee350ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529249532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa5291206faba0099383f9a378683dc78d59bf8113dffd07848f9240a421533`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f22eb50d5d925ca0f81da6db343dbdc81aa611e812032056634628414f48a3`  
		Last Modified: Thu, 25 Jul 2024 20:09:20 GMT  
		Size: 94.4 MB (94377097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:b926196df80c5a7d862a90488ae71afe95f754cbd86cc7032bf7cc1a092008e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292d40861cc7dc89d7d70263469c35810ef43831d8c2857a16210e5cd2cf872`

```dockerfile
```

-	Layers:
	-	`sha256:09418961dcd7d74b2c7d2e39a17e27da2d656c41aead2f65639b7fa71e39df3e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e683ae3f9f327b13c93a69066b24e46e949b32c28b989d1dc3c43b9e9ba23e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:41466285cf8ea843fa3b3c94325dd7104683eda4ca5b0fa7211777c2c2b9bac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518759398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7625946dc98d5705557e5291d72b3d243c115ffce766463fbe341b12486f5d3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ee5e76db80c90568838c628d8d2d829c19b4dbfb03c0ba21bdc7c67222c57`  
		Last Modified: Fri, 26 Jul 2024 01:05:05 GMT  
		Size: 87.3 MB (87324289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-python3` - unknown; unknown

```console
$ docker pull spark@sha256:663131e879b7c3969172266de932037a884f105281a5433ed3cde65ccbc31d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e9f5ed76542e0d5265955f26f6ca2a3babd721ebfef2a50be74868b0e7f02e`

```dockerfile
```

-	Layers:
	-	`sha256:79c6cdf6d368d9de17fb3d8a24ad7baef0da1924aecfea1604724cd7fdd452c5`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6df2db9df8d6822e06b96d6a2183e6c79272432cd953f88690f6de0e12c0fed`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-r`

```console
$ docker pull spark@sha256:f3986bc4f3efdda2f13d572aee646699d4828b0502531e4d313fafd55974a300
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-r` - linux; amd64

```console
$ docker pull spark@sha256:fb0d9bb47f902b77a127eef7556c5ba37f9c64d1da1c55e1cb2732a174124321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 MB (667171108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4b53bdf6f9442c1511f74b580211471c46c7c59126782410833c03bc5b1b14`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb45576f9906fbae578a15a7a4e6825477b15340b18bd0ed0be9633e9ad0221`  
		Last Modified: Thu, 25 Jul 2024 20:10:27 GMT  
		Size: 232.3 MB (232298673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:1ff25735941029aa3d898ab2bb6c4eee691671a7a3dc295595b965cd11cc4260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11094500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be967ace03a57baadfa2c1515654a79802cb0cdefeeacd88319a5a8bc844451`

```dockerfile
```

-	Layers:
	-	`sha256:d8e380cb508aed710e6c43598b19e04f240b2eef8402f96f9b7f00b6c810d52e`  
		Last Modified: Thu, 25 Jul 2024 20:10:23 GMT  
		Size: 11.1 MB (11083868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b664ffc49eed408eb906994a2874385d84e8c5daf79ba2c32f8c7379d8eb0571`  
		Last Modified: Thu, 25 Jul 2024 20:10:22 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:de1adbd2454f85d6f9318fee69ae9d96169dc19a31f4351c879144e9096a8d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.9 MB (644949529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf7b320972726f31b2f4c9362d3e90c41e3c3a23f28336abf133091fcf1cc07`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cef8c8c8aca197c53d5121523432d71f3ab0c5629fa611dec61ad49a7a31879`  
		Last Modified: Fri, 26 Jul 2024 01:06:48 GMT  
		Size: 213.5 MB (213514420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-r` - unknown; unknown

```console
$ docker pull spark@sha256:b05ac0f7f539d3db9e7ab3013b27e84fe680eef31f895f33eed7fb79ea51f553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11079386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651cabbc9483b471f22046e28703203ee2a6fc17c0b78c54f0df52abeadc381f`

```dockerfile
```

-	Layers:
	-	`sha256:bda6d6ca3adb61c07de41f3290ee3c957dc29b71424dd3d5695fd259c3d6e2ea`  
		Last Modified: Fri, 26 Jul 2024 01:06:43 GMT  
		Size: 11.1 MB (11068333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962ed10060202da95fa6de2c4440aa0fa82e697df6626f1b95b52dfc4a5b5efd`  
		Last Modified: Fri, 26 Jul 2024 01:06:42 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala`

```console
$ docker pull spark@sha256:0694ad9ad47557edc294feaae808d8c97e401e68eea8463f5ea5b59c067647c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala` - linux; amd64

```console
$ docker pull spark@sha256:999a40beefadc6f06807ffedd2925cb9832b0f72b32175a6e15dbb4fc668f7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434872435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1453b3891def7712af8e00211e28ca319f522333a3f08b8cea4668bd00580fb3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:76dddb523fc934215c745ac9ca68815a707d1c2e0f315f2ab5db2514a12b2aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebd68e97aa34c85555e4639c0bcbd8086eefb13e88c66f41da66674d698e10b`

```dockerfile
```

-	Layers:
	-	`sha256:f9478da28473c345981aa24b593f4cc4a1c08776f810ec893ede1a5edba2bcc7`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 4.2 MB (4206406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74617bf770dde47c7b2672422be5ad6511319566ef8fb417f366ffe80fe0c677`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:da6e2b6d04cb5269ec6def211291d0d498da02fd09d2a5249ac9dc738bedd424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431435109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004fa2cba8523660125e1418f8739751face3e201850810b33e12018508a2772`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala` - unknown; unknown

```console
$ docker pull spark@sha256:8625ee711ee5ad8aa3e1d2b47a9387e5b2fed26a284a6d6209a5aa54f67f9fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ed6125f96ce604b3bfff8eaff6d68ffad6dd39ea1408485ad3f7093c5dd364`

```dockerfile
```

-	Layers:
	-	`sha256:e376ff396db5635fbe144f18d9ac43c9b52888b37b58152a84a43df89051c8bd`  
		Last Modified: Thu, 25 Jul 2024 23:09:19 GMT  
		Size: 4.2 MB (4206697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50dfec08a82dfdd4ff92ec8e946049e6cb67b82a3fcee3ef600c682f04870df`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:770a711d0e091e410fe8bea5f5e4329d7a3623829528fdf52bcb759616ca2312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a369fbfca209c18727286e1e5e072382e74444e1dbb8ac2c913f51ef6bbb0dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.8 MB (688805355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f6e3844a5bbdec32273d3b2a94d08db588fea2b8d89f79f2042c0f248d0051`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd538c2988cb3a744f5a2d188fcdce1380a548cbfa623b12f9e9e48b8a9fb071`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 253.9 MB (253932920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5dc25bbf45294914b197685cac5efc90b8bddfd0be8c986e9f039f57c9f74bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12217554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc777ae7d311699119476bc1c3d4ce158c63fd125b84e3e087301b7c3bada45c`

```dockerfile
```

-	Layers:
	-	`sha256:1582c3f4e184462b8d3e3142357354844eb82bb54a6cabde1b1b6aa70147516d`  
		Last Modified: Thu, 25 Jul 2024 20:10:03 GMT  
		Size: 12.2 MB (12207044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44fd739ab2f137d420b9c08dd38e9ab3afcc18daa6da8ec4b86dfd69a70e7f8c`  
		Last Modified: Thu, 25 Jul 2024 20:10:03 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e2bfe0fb4dfd9391234e7ea2b0001fe2bdd54f5a06c3299a79e39fdbf822aae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.6 MB (666577014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41b6ab8ce531eed3cfe546cbad0a94f3afbbe968dac88e3e7999044e5839125`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad47be542b434c930bc1393466a75ca631b0ec5212a39fdf5c52ae61708cfbd4`  
		Last Modified: Fri, 26 Jul 2024 00:51:09 GMT  
		Size: 235.1 MB (235141905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:efbb4888d2006fa9e1d67920606297b4ff4e4b078cd29d7ca79af1efb07ccd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12202457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441403cbd5531ad0c21f666eb703d4e6f0b6220540418f2ea3d9ecb0e7872015`

```dockerfile
```

-	Layers:
	-	`sha256:cc5c15ec7b810912a68f921813782dbfda1585c201de5f711aa9e5499d45b986`  
		Last Modified: Fri, 26 Jul 2024 00:51:05 GMT  
		Size: 12.2 MB (12191538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99642068bd997cfab00e1e5f0c8f504b1b429a3219f3d0a4d9bb1cdd68102c79`  
		Last Modified: Fri, 26 Jul 2024 00:51:04 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:dce7e55e5ba3b9a0ca4a6900588570efac076598ebce8d3d85186a0e5eabb9bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:7210fdc649081e3856e42fe2aed1042fe376823a6f3a4975f41cf5225ee350ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529249532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa5291206faba0099383f9a378683dc78d59bf8113dffd07848f9240a421533`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f22eb50d5d925ca0f81da6db343dbdc81aa611e812032056634628414f48a3`  
		Last Modified: Thu, 25 Jul 2024 20:09:20 GMT  
		Size: 94.4 MB (94377097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b926196df80c5a7d862a90488ae71afe95f754cbd86cc7032bf7cc1a092008e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8939154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292d40861cc7dc89d7d70263469c35810ef43831d8c2857a16210e5cd2cf872`

```dockerfile
```

-	Layers:
	-	`sha256:09418961dcd7d74b2c7d2e39a17e27da2d656c41aead2f65639b7fa71e39df3e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 8.9 MB (8928219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e683ae3f9f327b13c93a69066b24e46e949b32c28b989d1dc3c43b9e9ba23e`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 10.9 KB (10935 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:41466285cf8ea843fa3b3c94325dd7104683eda4ca5b0fa7211777c2c2b9bac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518759398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7625946dc98d5705557e5291d72b3d243c115ffce766463fbe341b12486f5d3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ee5e76db80c90568838c628d8d2d829c19b4dbfb03c0ba21bdc7c67222c57`  
		Last Modified: Fri, 26 Jul 2024 01:05:05 GMT  
		Size: 87.3 MB (87324289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:663131e879b7c3969172266de932037a884f105281a5433ed3cde65ccbc31d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e9f5ed76542e0d5265955f26f6ca2a3babd721ebfef2a50be74868b0e7f02e`

```dockerfile
```

-	Layers:
	-	`sha256:79c6cdf6d368d9de17fb3d8a24ad7baef0da1924aecfea1604724cd7fdd452c5`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 8.9 MB (8932125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6df2db9df8d6822e06b96d6a2183e6c79272432cd953f88690f6de0e12c0fed`  
		Last Modified: Fri, 26 Jul 2024 01:05:02 GMT  
		Size: 11.4 KB (11368 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:f3986bc4f3efdda2f13d572aee646699d4828b0502531e4d313fafd55974a300
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fb0d9bb47f902b77a127eef7556c5ba37f9c64d1da1c55e1cb2732a174124321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 MB (667171108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4b53bdf6f9442c1511f74b580211471c46c7c59126782410833c03bc5b1b14`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb45576f9906fbae578a15a7a4e6825477b15340b18bd0ed0be9633e9ad0221`  
		Last Modified: Thu, 25 Jul 2024 20:10:27 GMT  
		Size: 232.3 MB (232298673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:1ff25735941029aa3d898ab2bb6c4eee691671a7a3dc295595b965cd11cc4260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11094500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be967ace03a57baadfa2c1515654a79802cb0cdefeeacd88319a5a8bc844451`

```dockerfile
```

-	Layers:
	-	`sha256:d8e380cb508aed710e6c43598b19e04f240b2eef8402f96f9b7f00b6c810d52e`  
		Last Modified: Thu, 25 Jul 2024 20:10:23 GMT  
		Size: 11.1 MB (11083868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b664ffc49eed408eb906994a2874385d84e8c5daf79ba2c32f8c7379d8eb0571`  
		Last Modified: Thu, 25 Jul 2024 20:10:22 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:de1adbd2454f85d6f9318fee69ae9d96169dc19a31f4351c879144e9096a8d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.9 MB (644949529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf7b320972726f31b2f4c9362d3e90c41e3c3a23f28336abf133091fcf1cc07`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cef8c8c8aca197c53d5121523432d71f3ab0c5629fa611dec61ad49a7a31879`  
		Last Modified: Fri, 26 Jul 2024 01:06:48 GMT  
		Size: 213.5 MB (213514420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b05ac0f7f539d3db9e7ab3013b27e84fe680eef31f895f33eed7fb79ea51f553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11079386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651cabbc9483b471f22046e28703203ee2a6fc17c0b78c54f0df52abeadc381f`

```dockerfile
```

-	Layers:
	-	`sha256:bda6d6ca3adb61c07de41f3290ee3c957dc29b71424dd3d5695fd259c3d6e2ea`  
		Last Modified: Fri, 26 Jul 2024 01:06:43 GMT  
		Size: 11.1 MB (11068333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962ed10060202da95fa6de2c4440aa0fa82e697df6626f1b95b52dfc4a5b5efd`  
		Last Modified: Fri, 26 Jul 2024 01:06:42 GMT  
		Size: 11.1 KB (11053 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.1-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:0694ad9ad47557edc294feaae808d8c97e401e68eea8463f5ea5b59c067647c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:999a40beefadc6f06807ffedd2925cb9832b0f72b32175a6e15dbb4fc668f7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434872435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1453b3891def7712af8e00211e28ca319f522333a3f08b8cea4668bd00580fb3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b80f6feddd39667ce3b37074d2c42f0595b43e35ae8f71470aeac92122e1de`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 24.3 MB (24280089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e562bdb6bb9cb4267f4a5e59c2fb3956d79e4181e7c47c02258b14a87482191`  
		Last Modified: Thu, 25 Jul 2024 19:08:27 GMT  
		Size: 317.9 MB (317884922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2562b7951bc82b92a10c992d13d03de4ea8298f78cf201e5bb4da4dacd2a9c`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:76dddb523fc934215c745ac9ca68815a707d1c2e0f315f2ab5db2514a12b2aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebd68e97aa34c85555e4639c0bcbd8086eefb13e88c66f41da66674d698e10b`

```dockerfile
```

-	Layers:
	-	`sha256:f9478da28473c345981aa24b593f4cc4a1c08776f810ec893ede1a5edba2bcc7`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 4.2 MB (4206406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74617bf770dde47c7b2672422be5ad6511319566ef8fb417f366ffe80fe0c677`  
		Last Modified: Thu, 25 Jul 2024 19:08:23 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:da6e2b6d04cb5269ec6def211291d0d498da02fd09d2a5249ac9dc738bedd424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431435109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004fa2cba8523660125e1418f8739751face3e201850810b33e12018508a2772`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c7a392ce69e2a28b5414a8a3d0b06875b4cb0753394f2b09cba2389f86f88`  
		Last Modified: Thu, 25 Jul 2024 23:09:25 GMT  
		Size: 317.9 MB (317884934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf83efb7beb6cd08c1ddc0ef1e6a6389145d0bfb88ffc574a37db2dcf799de3`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.1-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8625ee711ee5ad8aa3e1d2b47a9387e5b2fed26a284a6d6209a5aa54f67f9fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ed6125f96ce604b3bfff8eaff6d68ffad6dd39ea1408485ad3f7093c5dd364`

```dockerfile
```

-	Layers:
	-	`sha256:e376ff396db5635fbe144f18d9ac43c9b52888b37b58152a84a43df89051c8bd`  
		Last Modified: Thu, 25 Jul 2024 23:09:19 GMT  
		Size: 4.2 MB (4206697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50dfec08a82dfdd4ff92ec8e946049e6cb67b82a3fcee3ef600c682f04870df`  
		Last Modified: Thu, 25 Jul 2024 23:09:18 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2`

**does not exist** (yet?)

## `spark:3.5.2-java17`

**does not exist** (yet?)

## `spark:3.5.2-java17-python3`

**does not exist** (yet?)

## `spark:3.5.2-java17-r`

**does not exist** (yet?)

## `spark:3.5.2-java17-scala`

**does not exist** (yet?)

## `spark:3.5.2-python3`

**does not exist** (yet?)

## `spark:3.5.2-r`

**does not exist** (yet?)

## `spark:3.5.2-scala`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java11-python3-r-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java11-python3-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java11-r-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java11-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java17-python3-r-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java17-python3-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java17-r-ubuntu`

**does not exist** (yet?)

## `spark:3.5.2-scala2.12-java17-ubuntu`

**does not exist** (yet?)

## `spark:4.0.0-preview1`

**does not exist** (yet?)

## `spark:4.0.0-preview1-python3`

**does not exist** (yet?)

## `spark:4.0.0-preview1-r`

**does not exist** (yet?)

## `spark:4.0.0-preview1-scala`

**does not exist** (yet?)

## `spark:4.0.0-preview1-scala2.13-java17-python3-r-ubuntu`

**does not exist** (yet?)

## `spark:4.0.0-preview1-scala2.13-java17-python3-ubuntu`

**does not exist** (yet?)

## `spark:4.0.0-preview1-scala2.13-java17-r-ubuntu`

**does not exist** (yet?)

## `spark:4.0.0-preview1-scala2.13-java17-ubuntu`

**does not exist** (yet?)

## `spark:latest`

```console
$ docker pull spark@sha256:9291bed1233be27509a09daa3073808b25836a55605db534840f13b812403751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:51633c52796e1725c58203cb69b46787e02c1d0c8c992ab43edf564578be011f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535846627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52157708d29726c2b779251b4a61e997a33273a859b2319468baa6d5d0830ad`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f210ebfd01cb0f676e99fdfe04fcf77e5190f3c6313c18b42be17bae03ef5`  
		Last Modified: Thu, 25 Jul 2024 19:07:10 GMT  
		Size: 24.3 MB (24280020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c30ffc7237fdf0a2772cf0ab4e0653340710b378b37d8f7d073d76a176ed`  
		Last Modified: Thu, 25 Jul 2024 19:07:15 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b491555d55f14b0ddb2ff4617a2c45f9d896b13a2e4a09e6cdfd9247c9a47`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110c67a5b62ce3885d1edd714706f5e89d7d73cc0d776d613e6da7244cbee6c0`  
		Last Modified: Thu, 25 Jul 2024 20:09:20 GMT  
		Size: 94.4 MB (94376224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:2f66bbf2ba48f6a11afa6172dade7f34cb9cf9f74de70ed1024db6e687d8ee8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea204d4c86be154903e0c64d0428a8c5d0ce1fbb586f0948e3d97ac0c20da2f`

```dockerfile
```

-	Layers:
	-	`sha256:98e35564159905e155961b64e950e068bde4bf0d33a712b4e8a63a0df1cd0808`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de0b1840010452e5012e09e6bfab0a3d3b9c66f7f9d989d5785a389345d0f29`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 11.5 KB (11529 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2819035b4f43d2fab7ca77b77b0eb01494d599827d7384f14225c89e1a5d03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525357491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185c8743966c5fc1acefe0d6889341e7197f00a97a15d607b8dbd4dcd0c63e9f`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6635e889bf3aeeae03c0654915849286347d17fae5c687f30ba538c7aaf9db`  
		Last Modified: Thu, 25 Jul 2024 23:01:15 GMT  
		Size: 324.5 MB (324482963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954e0031f1fa9967f96f51cb96ff1417d2a8f62eddfd807efb69ba7bb637421`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fdf99e025920826cd3564c57e3362a715d278abb5dbc371517d59dc470ca19`  
		Last Modified: Fri, 26 Jul 2024 00:55:38 GMT  
		Size: 87.3 MB (87324299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:7852f56c3de666c617a561d16ac25f56156a8ac23856286b7d23d60d0ab6040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bbaa8f986c97ca2f0e106f77ec87f35b299244a40d6bcb3d745ef80d561385`

```dockerfile
```

-	Layers:
	-	`sha256:b39b84483ca05f23c4542a97bd36fc1762d8138e733444a0f405e32ce654e7e7`  
		Last Modified: Fri, 26 Jul 2024 00:55:36 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e07db44504d0fa64e64681dc8c4db36a9d734036fbdd49c0522774bd948a87a`  
		Last Modified: Fri, 26 Jul 2024 00:55:35 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:9291bed1233be27509a09daa3073808b25836a55605db534840f13b812403751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:51633c52796e1725c58203cb69b46787e02c1d0c8c992ab43edf564578be011f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535846627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52157708d29726c2b779251b4a61e997a33273a859b2319468baa6d5d0830ad`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f210ebfd01cb0f676e99fdfe04fcf77e5190f3c6313c18b42be17bae03ef5`  
		Last Modified: Thu, 25 Jul 2024 19:07:10 GMT  
		Size: 24.3 MB (24280020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c30ffc7237fdf0a2772cf0ab4e0653340710b378b37d8f7d073d76a176ed`  
		Last Modified: Thu, 25 Jul 2024 19:07:15 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b491555d55f14b0ddb2ff4617a2c45f9d896b13a2e4a09e6cdfd9247c9a47`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110c67a5b62ce3885d1edd714706f5e89d7d73cc0d776d613e6da7244cbee6c0`  
		Last Modified: Thu, 25 Jul 2024 20:09:20 GMT  
		Size: 94.4 MB (94376224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:2f66bbf2ba48f6a11afa6172dade7f34cb9cf9f74de70ed1024db6e687d8ee8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea204d4c86be154903e0c64d0428a8c5d0ce1fbb586f0948e3d97ac0c20da2f`

```dockerfile
```

-	Layers:
	-	`sha256:98e35564159905e155961b64e950e068bde4bf0d33a712b4e8a63a0df1cd0808`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 8.9 MB (8937716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de0b1840010452e5012e09e6bfab0a3d3b9c66f7f9d989d5785a389345d0f29`  
		Last Modified: Thu, 25 Jul 2024 20:09:19 GMT  
		Size: 11.5 KB (11529 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2819035b4f43d2fab7ca77b77b0eb01494d599827d7384f14225c89e1a5d03cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525357491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185c8743966c5fc1acefe0d6889341e7197f00a97a15d607b8dbd4dcd0c63e9f`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6635e889bf3aeeae03c0654915849286347d17fae5c687f30ba538c7aaf9db`  
		Last Modified: Thu, 25 Jul 2024 23:01:15 GMT  
		Size: 324.5 MB (324482963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954e0031f1fa9967f96f51cb96ff1417d2a8f62eddfd807efb69ba7bb637421`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fdf99e025920826cd3564c57e3362a715d278abb5dbc371517d59dc470ca19`  
		Last Modified: Fri, 26 Jul 2024 00:55:38 GMT  
		Size: 87.3 MB (87324299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:7852f56c3de666c617a561d16ac25f56156a8ac23856286b7d23d60d0ab6040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bbaa8f986c97ca2f0e106f77ec87f35b299244a40d6bcb3d745ef80d561385`

```dockerfile
```

-	Layers:
	-	`sha256:b39b84483ca05f23c4542a97bd36fc1762d8138e733444a0f405e32ce654e7e7`  
		Last Modified: Fri, 26 Jul 2024 00:55:36 GMT  
		Size: 8.9 MB (8941646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e07db44504d0fa64e64681dc8c4db36a9d734036fbdd49c0522774bd948a87a`  
		Last Modified: Fri, 26 Jul 2024 00:55:35 GMT  
		Size: 12.0 KB (11986 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:f62025eed8b803193186e4f8a25d73a2cee03f41dba584f9ab2bd1e83eca1cef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:17f945959bb62af8e083ff2885095fb8f7f34e8fd7c10ef1bef7bed79a9c2bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558242624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bee114d49083fabcc885dbc8c8da5ca2dd0d979d0f05949babdb948565343e`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae1f070b0bb7e1a00ef8e0d0578b66d09c74e62e792064fd9ba312213b12337`  
		Last Modified: Thu, 25 Jul 2024 19:07:59 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf378bcfc2bc044f1e92f3ce613ccccfeb57e2e0fd79e16a21763399dad112a`  
		Last Modified: Thu, 25 Jul 2024 19:08:00 GMT  
		Size: 24.9 MB (24895362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44060edff215e1462f66690e944137c879404b696973b52722e7d7b7f81c594e`  
		Last Modified: Thu, 25 Jul 2024 19:08:04 GMT  
		Size: 324.5 MB (324482963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335d102aaf9e3def5dd22fc8664b89fd54a34761dbf62b59ec5b1f1fdc94321`  
		Last Modified: Thu, 25 Jul 2024 19:08:00 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4d8ea28d3b7eeb39c4e8b22173742e064aded34acecc5c7ec935f121e45a88`  
		Last Modified: Thu, 25 Jul 2024 20:09:46 GMT  
		Size: 118.3 MB (118267580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:024985d20f48fc546895df4ffe8d5522f8d5b8851433a9762923e4f4a62348e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc35bedba3f3ad527546c723e9c70b45264fbbd4062b76f7060ed0d4763affe`

```dockerfile
```

-	Layers:
	-	`sha256:1a0d7bd14c6bbea38e0568c5f868f2b0adf0fa9aa7d91b1266a6cf29cd5a0a2e`  
		Last Modified: Thu, 25 Jul 2024 20:09:45 GMT  
		Size: 9.7 MB (9738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11beaf8bc11fe5b7379a1bc64ba6767fbc6cbd7476f4bad8694215881b40a9b`  
		Last Modified: Thu, 25 Jul 2024 20:09:43 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9e6bc3e09e219e17af861e7f750e45d95e628e33a6add0b5ccc0ea6d45d568c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.3 MB (551313382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272141b75480fedcfba07f6821e16f8c30a5a1aa6b6ab2de67c54b5ff049d73b`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52898087e9570653942a6d962598f830e90af4b4f588a9a9237223f3aa042784`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3d496557c3b69bfd76ad385fdc78dc82f6f0acb901f19dfd004e39f2af807b`  
		Last Modified: Thu, 25 Jul 2024 22:58:53 GMT  
		Size: 24.6 MB (24560618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a03c236c07e35dae6dc0e470f222454785d1ba7e9a68986c038f686319be25`  
		Last Modified: Thu, 25 Jul 2024 22:58:59 GMT  
		Size: 324.5 MB (324482959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3646ae7c68099326408b315ccdeed9aeb4d661ac1c5cf2c07c35ed4efc4b16f`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2988afda8f4d9f351841c73ebd242eee6afc0ed520d6728bf1933bacff1d064`  
		Last Modified: Fri, 26 Jul 2024 00:52:18 GMT  
		Size: 114.3 MB (114303723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:3f188b5b61328bb3970a0b3af5abd9ca410ce1dd9074b3b0f2e9b27ced8f0cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130066ea96d5cbcc916ccbb596f37f4122c8057bac7c3d4c00fef7da78fa8213`

```dockerfile
```

-	Layers:
	-	`sha256:86134186df1fa96674683c8341923f6b76d7d7928d71c85fd65bfbd400b471fd`  
		Last Modified: Fri, 26 Jul 2024 00:52:16 GMT  
		Size: 9.7 MB (9733543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7baed3d231afc5c3adaec35630e8e0589586ba8495506e078ab4bc69291b494f`  
		Last Modified: Fri, 26 Jul 2024 00:52:15 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:cf52f8e45574790c82688ab8b1f56848e499ab0024fe5a559cc4d4efcb706136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:39b8fca5c4cb8aef424dee564c5c74318b6417620a81860feead5aa279fa9a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673768649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5cac70236b2611121e54a3f6c06e6259916cbdbcf7ddb07ddb820535a4ea6c`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f210ebfd01cb0f676e99fdfe04fcf77e5190f3c6313c18b42be17bae03ef5`  
		Last Modified: Thu, 25 Jul 2024 19:07:10 GMT  
		Size: 24.3 MB (24280020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c30ffc7237fdf0a2772cf0ab4e0653340710b378b37d8f7d073d76a176ed`  
		Last Modified: Thu, 25 Jul 2024 19:07:15 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b491555d55f14b0ddb2ff4617a2c45f9d896b13a2e4a09e6cdfd9247c9a47`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d071c277834c14238c2e092148fe085f03a5adc64861879affb64b67891afe`  
		Last Modified: Thu, 25 Jul 2024 20:10:02 GMT  
		Size: 232.3 MB (232298246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:79ccfe7985d77fba12b0324f21cbe45f4ed7e7ebfc22713680f4b4f50cb09466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4ac51a3d0b15f675011e1bc7f1cc2f67bb9383f307f38f520021a8837d9344`

```dockerfile
```

-	Layers:
	-	`sha256:72cc0dc43acbfc63c1be222c43793bf591a4ed125760d6d51c73d3a8535b6a13`  
		Last Modified: Thu, 25 Jul 2024 20:09:58 GMT  
		Size: 11.1 MB (11093057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c38f560d6ef0ca24abbdf701ca381f02a1a3f35c6c7091a01cbc20bc796e6f3`  
		Last Modified: Thu, 25 Jul 2024 20:09:58 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:149e42743a78c080d817c16774e18af074e315353a85e5298776925f2bd40e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.5 MB (651547225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539fdace92a08118084c87fe9f516bafc18ed40569b635a979c06b3f1de2d5ba`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6635e889bf3aeeae03c0654915849286347d17fae5c687f30ba538c7aaf9db`  
		Last Modified: Thu, 25 Jul 2024 23:01:15 GMT  
		Size: 324.5 MB (324482963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954e0031f1fa9967f96f51cb96ff1417d2a8f62eddfd807efb69ba7bb637421`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc32397a5b6a0ff5459caad620b1ac0fa526b1dae47d55429fce3083bc0e726`  
		Last Modified: Fri, 26 Jul 2024 00:57:25 GMT  
		Size: 213.5 MB (213514033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:305b1e4627657f5b1311658bd662ef3ebe69878ca6e3637bb52c4f493e149554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11088859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d671d59f582f8bf7185f95ab2e535b43c0e2704e9cd7fc50c7213fdd3bb8cc5d`

```dockerfile
```

-	Layers:
	-	`sha256:e7b000ff8bb32c5e0d6ac86bbefb47748aa3000482a64b6427c57cbfdb95c365`  
		Last Modified: Fri, 26 Jul 2024 00:57:20 GMT  
		Size: 11.1 MB (11077508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7e0008dd77efa86df710b6404893158abc3af0e733cd725672ea9aa96ca184`  
		Last Modified: Fri, 26 Jul 2024 00:57:20 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:a6f79f0daa5dc41a5e5b3f619442c8e10f6628da76303b1b01ff7ace526308d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:7b0b1407557b8342cf17e54fc3209eab9dfc6e9559c69a64a1e735d9876cd9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441470403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43de83fef4b431add8b242ef9bd36f9176a408d48b2091714935980c685df69`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecab76ee79a449f376fd9a635c69707d229ca22d4e1bd611361e77f662291c8`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f210ebfd01cb0f676e99fdfe04fcf77e5190f3c6313c18b42be17bae03ef5`  
		Last Modified: Thu, 25 Jul 2024 19:07:10 GMT  
		Size: 24.3 MB (24280020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c30ffc7237fdf0a2772cf0ab4e0653340710b378b37d8f7d073d76a176ed`  
		Last Modified: Thu, 25 Jul 2024 19:07:15 GMT  
		Size: 324.5 MB (324482901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b491555d55f14b0ddb2ff4617a2c45f9d896b13a2e4a09e6cdfd9247c9a47`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:e8a1bbdda9d478ef7fc01618880e72a98373e1f88089aecea3b0b0268fcd031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31224db9bd6e4cff4055420f02cce61312224f9b54e25cb94b4df27f87fe6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:56c31d3ebd0d2cd68e5c4aa25864902bc1b1a0ca40caa07e5601fa786bc08e12`  
		Last Modified: Thu, 25 Jul 2024 19:07:10 GMT  
		Size: 4.2 MB (4215603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c6b7efb38644fb85011cea6339d6765097baa8455e7aed08a44049377c4d9e`  
		Last Modified: Thu, 25 Jul 2024 19:07:09 GMT  
		Size: 22.7 KB (22701 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:8c239753e94f58ede149a136cad56326946015fb4862b3dc9536160b3d7f3c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438033192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5d3d2fd71a34a02700b4bc6fbfbec9867bfd8fa4f1fa19a1a6ceb596a00be5`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8ad0305ba2158da42f012f170939388aa6bd09940f465fdce46960318b253`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0346f441eaa5a631130dfd34c30def886be0c916a9bd7602cc0df3b3dc8bde`  
		Last Modified: Thu, 25 Jul 2024 23:01:09 GMT  
		Size: 24.0 MB (24005147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6635e889bf3aeeae03c0654915849286347d17fae5c687f30ba538c7aaf9db`  
		Last Modified: Thu, 25 Jul 2024 23:01:15 GMT  
		Size: 324.5 MB (324482963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954e0031f1fa9967f96f51cb96ff1417d2a8f62eddfd807efb69ba7bb637421`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:f4337e4aa3a02ef8cf29651d9f5ae63a61a559958f6c2be163caab84344dc09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05960a4426da1ab32cefd2b0fc322458adb5228f49509cac93d54214991174d1`

```dockerfile
```

-	Layers:
	-	`sha256:c35cc742b3768007cd3f235ef0a62e51dd1ce17892d0a415578a4d8091905a26`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 4.2 MB (4215906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1ce15573a6257a54356b270cf4ac3922bd17b980a2e8c1681bcb7bd92f9a75`  
		Last Modified: Thu, 25 Jul 2024 23:01:08 GMT  
		Size: 23.0 KB (23005 bytes)  
		MIME: application/vnd.in-toto+json
