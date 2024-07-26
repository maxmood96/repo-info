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
$ docker pull spark@sha256:080b138bb7ea40357d4e87a81c9ce536a695005c526e2bfb40f4562385dfb49b
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
$ docker pull spark@sha256:080b138bb7ea40357d4e87a81c9ce536a695005c526e2bfb40f4562385dfb49b
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
$ docker pull spark@sha256:af0cce88f62affe83f2d71280bb32c4dace03beb3ce652b591ec59d359d37f33
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
$ docker pull spark@sha256:3825a4204f70bb7a9dfa458c7e54726d57608ef3541ea14e3c7bb3aeec6fcd4e
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
$ docker pull spark@sha256:080b138bb7ea40357d4e87a81c9ce536a695005c526e2bfb40f4562385dfb49b
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
$ docker pull spark@sha256:af0cce88f62affe83f2d71280bb32c4dace03beb3ce652b591ec59d359d37f33
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

## `spark:3.5.0`

```console
$ docker pull spark@sha256:06d4e6bd38a39f8169c4b117f06eda53496ff52e0784780daf6e1b9a55b990a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0` - linux; amd64

```console
$ docker pull spark@sha256:ffee0db0650f0ba6198a8b2ca380adfaf100e8cc828d2700a611b3b9d624b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535790927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca01114f9168da2c05bb4d708aa2e9978d106a8d46240f3ee2ec16f02fb3ef8`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16b4519eaf4404652ecce8d1c74c51f74d0ea0ac8e3a7cd51201a23a7be5f6a`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 94.4 MB (94376174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0` - unknown; unknown

```console
$ docker pull spark@sha256:6de1b9161e5a95cbab9c962f2653569d6a0459f18c94276f884f6043a2b24e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ffa17309f5dc90f4b9fabea3fda5d86f65b3f858acaf1c01763dda716c6af`

```dockerfile
```

-	Layers:
	-	`sha256:295524fcc12682644a8a8b3e932f69080623bff04b62eaddebd460adaed66660`  
		Last Modified: Thu, 25 Jul 2024 20:09:24 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95685f189ee5c7723dac53cef870e1c1fd56d9b44cdc80c931e8df296863f07`  
		Last Modified: Thu, 25 Jul 2024 20:09:23 GMT  
		Size: 10.9 KB (10935 bytes)  
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
$ docker pull spark@sha256:f8581d13ebc80ecda88a107042cf0dd2511553e7522bfbbe02639dfe5e95c579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17` - linux; amd64

```console
$ docker pull spark@sha256:b6c289c43dd712911b76f92741df0e45d2361be886b00bda85e422ace137c0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558186305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239f4bffdd106eadcf484693018ed9ade2f65a608e15c48cf2b7fbde107420a2`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c810dadfafd1ee7390021545ec8b3d99d38d8b21105f395066eb2756799214`  
		Last Modified: Thu, 25 Jul 2024 21:01:32 GMT  
		Size: 118.3 MB (118267090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17` - unknown; unknown

```console
$ docker pull spark@sha256:ba99c6001995755606ccaff96c655a467e347e8eb183ec524c9b99290235e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6479ef28d8d7e03575edb4324950ea795249ae407cbceef3ca43f86a89b029a1`

```dockerfile
```

-	Layers:
	-	`sha256:fa36f406d6bf02e9626028e7213744121d193678b3526a89147370ff9a9750e2`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca15d7d406712ad8ac6578c97d3128eb1d81519806ba71fbb290710b3954f248`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
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
$ docker pull spark@sha256:f8581d13ebc80ecda88a107042cf0dd2511553e7522bfbbe02639dfe5e95c579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:b6c289c43dd712911b76f92741df0e45d2361be886b00bda85e422ace137c0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558186305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239f4bffdd106eadcf484693018ed9ade2f65a608e15c48cf2b7fbde107420a2`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c810dadfafd1ee7390021545ec8b3d99d38d8b21105f395066eb2756799214`  
		Last Modified: Thu, 25 Jul 2024 21:01:32 GMT  
		Size: 118.3 MB (118267090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:ba99c6001995755606ccaff96c655a467e347e8eb183ec524c9b99290235e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6479ef28d8d7e03575edb4324950ea795249ae407cbceef3ca43f86a89b029a1`

```dockerfile
```

-	Layers:
	-	`sha256:fa36f406d6bf02e9626028e7213744121d193678b3526a89147370ff9a9750e2`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca15d7d406712ad8ac6578c97d3128eb1d81519806ba71fbb290710b3954f248`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
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
$ docker pull spark@sha256:d9fb68ff0d4d1e28b46cb0e2a1f910d38c2ffb751319ac9fb56861476a2dc174
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:16e2bba01e0c94fba21f7c2c4cd0ec080af92aa575648b5dc5d3e1d0c93ca92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763750785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4dd46b71bdc16eeed1b57b436b00fcfde8d1ae371ee71f4e188b149ae56a65e`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf66a7dc9a2fb0ee11f6c015c3dd59246c43b15f4243c28afe32b5bc81bf78f`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 323.8 MB (323831570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:c9c29e7151d799813090c82c09b42df6a5cb69bb030783727d9ec9526f1b3f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9292e6fda4225ca5b1099350a79084c4e9eb6bc493159e2063fa7b5f2eb9d6`

```dockerfile
```

-	Layers:
	-	`sha256:7dcc37ad6a895a7f2b1f365de73cdaa5c848ceb6c0c27b6c9cb3402b0ea142f9`  
		Last Modified: Thu, 25 Jul 2024 21:02:09 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:679c93c572e7c4c5e2d4db16d992c332d8bba102f255609b9b291c0adb5aaf56`  
		Last Modified: Thu, 25 Jul 2024 21:02:09 GMT  
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
$ docker pull spark@sha256:1c72a3d4f0a9634f09bc0d7d6a2fc03653b0bfbb9f34bca2ddf0a4a726abbd49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:42ac70865593ea93dea10d53dfb7af871307378956534432d0d994937617602a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439919215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891faad8b5986754d45d7595f5f38d9fe8789cf16d2227f42123747a453b9465`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:e3b288e4c9dab90223b21c8311cf6a0972e2006ae3e15cd814821b8f0747f2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e1c55be4f62fce1f2a721a011cf2f1f1421b64d1429dc87363e603ca451685`

```dockerfile
```

-	Layers:
	-	`sha256:5995092599e0b9911490c0ce10f93aa365f724cedcb523cb824a648fe35aede3`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401abdac17ed26e7492abb0181994849dfc4a481cbff8ffd6860d256471395ee`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5447cefa36750cb18fd5714f39efcf220467067cb4039386af043b0e27db7b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436953847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0c57516e6ff4d06ee7d1e071326a6a340f0676a84668b5cdd134b3e971d7c`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:81c5a7bc2ae40c6c2852155eada223b85c4591227a95631b68cba9fe0e565132`  
		Last Modified: Thu, 25 Jul 2024 23:02:42 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ed3c105cdf5403992111a8cfee5051e6978c78e746432c14fe0568cf745073`  
		Last Modified: Thu, 25 Jul 2024 23:02:35 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:4b80800d14a193a8526cdc3f5b7f7c4a6ff3f5191966ea5b42370a05a3897863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743b722082d6402268060f4455b0ef41d816b46082d6d15ec248cca0973c5290`

```dockerfile
```

-	Layers:
	-	`sha256:9edd559d8a6df8d8e8c4f9289a81e9e75d9dd6cbbf022012512d6eed776b048d`  
		Last Modified: Thu, 25 Jul 2024 23:02:36 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b710c55de8b07f7f04bb405d630d37e990c61935ca9dab30b9ec40931209acdd`  
		Last Modified: Thu, 25 Jul 2024 23:02:35 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-python3`

```console
$ docker pull spark@sha256:06d4e6bd38a39f8169c4b117f06eda53496ff52e0784780daf6e1b9a55b990a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-python3` - linux; amd64

```console
$ docker pull spark@sha256:ffee0db0650f0ba6198a8b2ca380adfaf100e8cc828d2700a611b3b9d624b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535790927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca01114f9168da2c05bb4d708aa2e9978d106a8d46240f3ee2ec16f02fb3ef8`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16b4519eaf4404652ecce8d1c74c51f74d0ea0ac8e3a7cd51201a23a7be5f6a`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 94.4 MB (94376174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-python3` - unknown; unknown

```console
$ docker pull spark@sha256:6de1b9161e5a95cbab9c962f2653569d6a0459f18c94276f884f6043a2b24e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ffa17309f5dc90f4b9fabea3fda5d86f65b3f858acaf1c01763dda716c6af`

```dockerfile
```

-	Layers:
	-	`sha256:295524fcc12682644a8a8b3e932f69080623bff04b62eaddebd460adaed66660`  
		Last Modified: Thu, 25 Jul 2024 20:09:24 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95685f189ee5c7723dac53cef870e1c1fd56d9b44cdc80c931e8df296863f07`  
		Last Modified: Thu, 25 Jul 2024 20:09:23 GMT  
		Size: 10.9 KB (10935 bytes)  
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
$ docker pull spark@sha256:31380e93a671f54fc67300a7c9eb612629e63ff80f8c9ef31bc858f52d4b4772
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-r` - linux; amd64

```console
$ docker pull spark@sha256:bf9f7347998806c2d99d1da756200e4b2b7fdf97971d057ef6096219ed33478e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673713489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ba5f24419d681b38e95791206dcd11c1dd464415c39570da1f0579e1bb8da`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d081ecee3232540d67a207c03bd1634d08cdc2308234ab452621b2f74887d17`  
		Last Modified: Thu, 25 Jul 2024 20:09:53 GMT  
		Size: 232.3 MB (232298736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-r` - unknown; unknown

```console
$ docker pull spark@sha256:676f0c1a38248f781a945d978ebf69848588ec53f8531f96b5f297ed89b56142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf6d9f797356d80f27119db57b35ccb0aec17e36a21be40e0c6726a4fcaf98d`

```dockerfile
```

-	Layers:
	-	`sha256:f3da557b801cbfb155a88a7f168ef56cdea84f1b2bc6f7f5c413af728a4c4f58`  
		Last Modified: Thu, 25 Jul 2024 20:09:51 GMT  
		Size: 11.1 MB (11092771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417386ad70011891a37049a942deca760d1322a25785a4dc35aea2c985ab4b05`  
		Last Modified: Thu, 25 Jul 2024 20:09:50 GMT  
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
$ docker pull spark@sha256:92e128de89971944ac5fc1e619b90d9b8baa7e2a3cf275085a2d12a90179838e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala` - linux; amd64

```console
$ docker pull spark@sha256:310470dab82f7fbef7723c40033deb1872c253079bd15fb2d9337d9465a7073a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441414753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc1de2982419a4d7d8ddfe5d8cfb3002ba0fa0ecc5ef9fdfe3e529aa3dcf569`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:d7828054d16a88ce3c5dd7814e4c559b3886628823116f023470f2a6f943e2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93fffa1af85cc193e3675f1ac41503abab52df7bf304ecb812b7869b50c1c1f`

```dockerfile
```

-	Layers:
	-	`sha256:e5159ae41c50f3c506bcb45bb46fc05d2564e8a4f9b308168a8f2c570c41af02`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 4.2 MB (4215309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649ea10a612d659ab969edfff36dccf75995d0b27f037d88357af9b31aba406a`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:bbe308ee2e697f6415f4caaa8f4ef6d218c6b849e188ddc4cf57ed477448d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437977399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a951e8f762732ebfd3f8cf6808c87c852f6b3c28cbf6f9530e1b063d62b8d11`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:faf3737bb2de950b752d5ad5057eba851effb0592b3229c23db7f4efe8d3ed8d`  
		Last Modified: Thu, 25 Jul 2024 23:04:19 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb990f807278d7197e6bbe0fc24dfe9c4a7af06ee7b72e2e262873c4a30041c`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f66293bcaf4b99579c0a71cb75c6f76432dfe0b3eab26872c6e4413358538ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b818ce33b3580befe1f6a7d7dd81d4725a7323fbf1ddd63b096de1b4f16d3e0`

```dockerfile
```

-	Layers:
	-	`sha256:0c1099ccb8dd2e35ed559c95c6d93f098ca23d5bb0e0cb56be182df8574d1e24`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 4.2 MB (4215600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa248df4dbfbafcee6391cfca87d71e1cf17eb166c98574d66cd16dcfa23a560`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:742f9f2100434bc89a65f4d4a6684d7055fe6fd6789d4ab4cb8a9f891baaa0b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:06d842705dbe9f8871ee9f1dd58b3a565b020d700dae24854116f2177a599dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 MB (695348444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e17a9c160373dc06d279fb2fc0f7f36f5ac07ecb7d4f6289d513c8fe9423897`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dc16e38c8405977d3a51dec8459f1ffe03d988b725498bed9553e79ca77e04`  
		Last Modified: Thu, 25 Jul 2024 20:10:00 GMT  
		Size: 253.9 MB (253933691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:95115529985b2ee5267704d5d3b0b810474da565c6b3c006af92ab3104fa25c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d796c0ce78e5ddd00f4c88bfdec5f3f5cdcf4689debe2ae95b204d3cbebb16f`

```dockerfile
```

-	Layers:
	-	`sha256:b031131b19ea5a9e5a0f4947deb592e3f86d356e4fe876e057149527441407c7`  
		Last Modified: Thu, 25 Jul 2024 20:09:56 GMT  
		Size: 12.2 MB (12215947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc623472edc1b0b0e2148e309afe325f8f94b59acfc1b381bab1323cf1512398`  
		Last Modified: Thu, 25 Jul 2024 20:09:56 GMT  
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
$ docker pull spark@sha256:06d4e6bd38a39f8169c4b117f06eda53496ff52e0784780daf6e1b9a55b990a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:ffee0db0650f0ba6198a8b2ca380adfaf100e8cc828d2700a611b3b9d624b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.8 MB (535790927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca01114f9168da2c05bb4d708aa2e9978d106a8d46240f3ee2ec16f02fb3ef8`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16b4519eaf4404652ecce8d1c74c51f74d0ea0ac8e3a7cd51201a23a7be5f6a`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 94.4 MB (94376174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6de1b9161e5a95cbab9c962f2653569d6a0459f18c94276f884f6043a2b24e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ffa17309f5dc90f4b9fabea3fda5d86f65b3f858acaf1c01763dda716c6af`

```dockerfile
```

-	Layers:
	-	`sha256:295524fcc12682644a8a8b3e932f69080623bff04b62eaddebd460adaed66660`  
		Last Modified: Thu, 25 Jul 2024 20:09:24 GMT  
		Size: 8.9 MB (8937122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95685f189ee5c7723dac53cef870e1c1fd56d9b44cdc80c931e8df296863f07`  
		Last Modified: Thu, 25 Jul 2024 20:09:23 GMT  
		Size: 10.9 KB (10935 bytes)  
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
$ docker pull spark@sha256:31380e93a671f54fc67300a7c9eb612629e63ff80f8c9ef31bc858f52d4b4772
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bf9f7347998806c2d99d1da756200e4b2b7fdf97971d057ef6096219ed33478e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673713489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ba5f24419d681b38e95791206dcd11c1dd464415c39570da1f0579e1bb8da`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d081ecee3232540d67a207c03bd1634d08cdc2308234ab452621b2f74887d17`  
		Last Modified: Thu, 25 Jul 2024 20:09:53 GMT  
		Size: 232.3 MB (232298736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:676f0c1a38248f781a945d978ebf69848588ec53f8531f96b5f297ed89b56142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf6d9f797356d80f27119db57b35ccb0aec17e36a21be40e0c6726a4fcaf98d`

```dockerfile
```

-	Layers:
	-	`sha256:f3da557b801cbfb155a88a7f168ef56cdea84f1b2bc6f7f5c413af728a4c4f58`  
		Last Modified: Thu, 25 Jul 2024 20:09:51 GMT  
		Size: 11.1 MB (11092771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417386ad70011891a37049a942deca760d1322a25785a4dc35aea2c985ab4b05`  
		Last Modified: Thu, 25 Jul 2024 20:09:50 GMT  
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
$ docker pull spark@sha256:92e128de89971944ac5fc1e619b90d9b8baa7e2a3cf275085a2d12a90179838e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:310470dab82f7fbef7723c40033deb1872c253079bd15fb2d9337d9465a7073a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441414753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc1de2982419a4d7d8ddfe5d8cfb3002ba0fa0ecc5ef9fdfe3e529aa3dcf569`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f2e266b66ab637fc0b10d83ab1ade408047588f9eee56772e03be9ce7a610`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4773a806a0c94b9f2431f932b77ef4b3c6370e46f7512c273a7f28b805653a33`  
		Last Modified: Thu, 25 Jul 2024 19:07:33 GMT  
		Size: 24.3 MB (24280101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c415f2e64a50f79c91d8f87834f6ca435cc451b553440357ef32e4c8682bf`  
		Last Modified: Thu, 25 Jul 2024 19:07:38 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32592ec41923c1cdf121e09679f88b8406fc1a66289753f44fc2a112707314`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d7828054d16a88ce3c5dd7814e4c559b3886628823116f023470f2a6f943e2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93fffa1af85cc193e3675f1ac41503abab52df7bf304ecb812b7869b50c1c1f`

```dockerfile
```

-	Layers:
	-	`sha256:e5159ae41c50f3c506bcb45bb46fc05d2564e8a4f9b308168a8f2c570c41af02`  
		Last Modified: Thu, 25 Jul 2024 19:07:32 GMT  
		Size: 4.2 MB (4215309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649ea10a612d659ab969edfff36dccf75995d0b27f037d88357af9b31aba406a`  
		Last Modified: Thu, 25 Jul 2024 19:07:31 GMT  
		Size: 22.4 KB (22407 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:bbe308ee2e697f6415f4caaa8f4ef6d218c6b849e188ddc4cf57ed477448d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437977399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a951e8f762732ebfd3f8cf6808c87c852f6b3c28cbf6f9530e1b063d62b8d11`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:faf3737bb2de950b752d5ad5057eba851effb0592b3229c23db7f4efe8d3ed8d`  
		Last Modified: Thu, 25 Jul 2024 23:04:19 GMT  
		Size: 324.4 MB (324427172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb990f807278d7197e6bbe0fc24dfe9c4a7af06ee7b72e2e262873c4a30041c`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f66293bcaf4b99579c0a71cb75c6f76432dfe0b3eab26872c6e4413358538ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b818ce33b3580befe1f6a7d7dd81d4725a7323fbf1ddd63b096de1b4f16d3e0`

```dockerfile
```

-	Layers:
	-	`sha256:0c1099ccb8dd2e35ed559c95c6d93f098ca23d5bb0e0cb56be182df8574d1e24`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 4.2 MB (4215600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa248df4dbfbafcee6391cfca87d71e1cf17eb166c98574d66cd16dcfa23a560`  
		Last Modified: Thu, 25 Jul 2024 23:04:12 GMT  
		Size: 22.7 KB (22700 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:797d853cba59aeb764ee31657d70edf2ef093d0b63d15c6c0d38d952563b685c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fb25a781d319a6ed57a9b159c4b4460bddfd9dac7a75ed9e705054d5a73191f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.5 MB (778464936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef4654bb43af6463ad8bed1de1dcbbdf66370fafe81be43944cc28731033022`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b6be2c015fbec69ab2e1db0de1576479861de48f156095079e465b37c51516`  
		Last Modified: Thu, 25 Jul 2024 21:02:35 GMT  
		Size: 338.5 MB (338545721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:69db48eac2062d8bb1b8bd071d053b7299c779765057ba1850e3da27eb329bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff734e12d8a2f36fa12567df7d8f15636a9d668ccde4c53d8b94185f7b873e40`

```dockerfile
```

-	Layers:
	-	`sha256:d9d46d1bc6727cbb6b582bf0b955f50bcb7f838abeb02aeca0791ff5c9ab2d03`  
		Last Modified: Thu, 25 Jul 2024 21:02:30 GMT  
		Size: 18.8 MB (18775974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7272d45953054d1d453ff55dd0a9fc25073ccd3804f1881ce88488b7400b041`  
		Last Modified: Thu, 25 Jul 2024 21:02:29 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:93c889ef12d74dfdce69e56a8aaed075d10eeeab91962fdeaf52dc5d78e6cfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 MB (759998145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664473195e6a7a92a943f4152580787b6761aa4453e080ecfaebbcaa39d0d2a3`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:81c5a7bc2ae40c6c2852155eada223b85c4591227a95631b68cba9fe0e565132`  
		Last Modified: Thu, 25 Jul 2024 23:02:42 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ed3c105cdf5403992111a8cfee5051e6978c78e746432c14fe0568cf745073`  
		Last Modified: Thu, 25 Jul 2024 23:02:35 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c412b2488b1051e7bfb49b35bfa54074b5def07155fded8e29589739629e9e`  
		Last Modified: Fri, 26 Jul 2024 00:47:14 GMT  
		Size: 323.0 MB (323044298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:25b627b0cd86f52110d962d348bae179e1a57cd9350414f881157f5e55cf9c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18753245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5193e452eec43f13510c80add4f3bbe20f5ba9e76c1a24d5e3e5462ed389c2`

```dockerfile
```

-	Layers:
	-	`sha256:f884427339c3b530da3692ebf1eb8039abe3de14d013c0b118735206c143359e`  
		Last Modified: Fri, 26 Jul 2024 00:47:07 GMT  
		Size: 18.7 MB (18742326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c025ad9a1e2118b958abbda96e52ce36dc5c66a51049ec0f5b54199359a59732`  
		Last Modified: Fri, 26 Jul 2024 00:47:06 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.0-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:f8581d13ebc80ecda88a107042cf0dd2511553e7522bfbbe02639dfe5e95c579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:b6c289c43dd712911b76f92741df0e45d2361be886b00bda85e422ace137c0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558186305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239f4bffdd106eadcf484693018ed9ade2f65a608e15c48cf2b7fbde107420a2`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c810dadfafd1ee7390021545ec8b3d99d38d8b21105f395066eb2756799214`  
		Last Modified: Thu, 25 Jul 2024 21:01:32 GMT  
		Size: 118.3 MB (118267090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ba99c6001995755606ccaff96c655a467e347e8eb183ec524c9b99290235e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6479ef28d8d7e03575edb4324950ea795249ae407cbceef3ca43f86a89b029a1`

```dockerfile
```

-	Layers:
	-	`sha256:fa36f406d6bf02e9626028e7213744121d193678b3526a89147370ff9a9750e2`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
		Size: 9.7 MB (9738165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca15d7d406712ad8ac6578c97d3128eb1d81519806ba71fbb290710b3954f248`  
		Last Modified: Thu, 25 Jul 2024 21:01:29 GMT  
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
$ docker pull spark@sha256:d9fb68ff0d4d1e28b46cb0e2a1f910d38c2ffb751319ac9fb56861476a2dc174
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:16e2bba01e0c94fba21f7c2c4cd0ec080af92aa575648b5dc5d3e1d0c93ca92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763750785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4dd46b71bdc16eeed1b57b436b00fcfde8d1ae371ee71f4e188b149ae56a65e`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf66a7dc9a2fb0ee11f6c015c3dd59246c43b15f4243c28afe32b5bc81bf78f`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 323.8 MB (323831570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c9c29e7151d799813090c82c09b42df6a5cb69bb030783727d9ec9526f1b3f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9292e6fda4225ca5b1099350a79084c4e9eb6bc493159e2063fa7b5f2eb9d6`

```dockerfile
```

-	Layers:
	-	`sha256:7dcc37ad6a895a7f2b1f365de73cdaa5c848ceb6c0c27b6c9cb3402b0ea142f9`  
		Last Modified: Thu, 25 Jul 2024 21:02:09 GMT  
		Size: 17.8 MB (17764054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:679c93c572e7c4c5e2d4db16d992c332d8bba102f255609b9b291c0adb5aaf56`  
		Last Modified: Thu, 25 Jul 2024 21:02:09 GMT  
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
$ docker pull spark@sha256:1c72a3d4f0a9634f09bc0d7d6a2fc03653b0bfbb9f34bca2ddf0a4a726abbd49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:42ac70865593ea93dea10d53dfb7af871307378956534432d0d994937617602a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439919215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891faad8b5986754d45d7595f5f38d9fe8789cf16d2227f42123747a453b9465`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:7a766b524f93fc88caa1b159425e3cd85009f6be4f7d82b83bc58f8d9863b435`  
		Last Modified: Thu, 25 Jul 2024 17:30:38 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a494011e97ce018cccc93c358914e744ddc73677651bdf487b7b12b18afd17`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404c6fbde8bcce36811a2159a4d6cf9872f644379f62c810674866b53db80aa`  
		Last Modified: Thu, 25 Jul 2024 20:09:22 GMT  
		Size: 24.9 MB (24895373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b07427c7a1c5702adcac962039e6b1bff42611e9dec4ae801e7abcbe6db9e`  
		Last Modified: Thu, 25 Jul 2024 20:09:27 GMT  
		Size: 324.4 MB (324427124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd4e5d6152c8a249f0831e9d8f7acf76d5d3585d74551eabe00bacdf0f9f8c`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e3b288e4c9dab90223b21c8311cf6a0972e2006ae3e15cd814821b8f0747f2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e1c55be4f62fce1f2a721a011cf2f1f1421b64d1429dc87363e603ca451685`

```dockerfile
```

-	Layers:
	-	`sha256:5995092599e0b9911490c0ce10f93aa365f724cedcb523cb824a648fe35aede3`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401abdac17ed26e7492abb0181994849dfc4a481cbff8ffd6860d256471395ee`  
		Last Modified: Thu, 25 Jul 2024 20:09:21 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.0-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5447cefa36750cb18fd5714f39efcf220467067cb4039386af043b0e27db7b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436953847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0c57516e6ff4d06ee7d1e071326a6a340f0676a84668b5cdd134b3e971d7c`
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
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:81c5a7bc2ae40c6c2852155eada223b85c4591227a95631b68cba9fe0e565132`  
		Last Modified: Thu, 25 Jul 2024 23:02:42 GMT  
		Size: 324.4 MB (324427150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ed3c105cdf5403992111a8cfee5051e6978c78e746432c14fe0568cf745073`  
		Last Modified: Thu, 25 Jul 2024 23:02:35 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.0-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4b80800d14a193a8526cdc3f5b7f7c4a6ff3f5191966ea5b42370a05a3897863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743b722082d6402268060f4455b0ef41d816b46082d6d15ec248cca0973c5290`

```dockerfile
```

-	Layers:
	-	`sha256:9edd559d8a6df8d8e8c4f9289a81e9e75d9dd6cbbf022012512d6eed776b048d`  
		Last Modified: Thu, 25 Jul 2024 23:02:36 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b710c55de8b07f7f04bb405d630d37e990c61935ca9dab30b9ec40931209acdd`  
		Last Modified: Thu, 25 Jul 2024 23:02:35 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1`

```console
$ docker pull spark@sha256:69168af92f1f825bcd1453cccc79114a8fc5f4c86c6bc6fbde3dd33cde61666a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1` - linux; amd64

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

### `spark:3.5.1` - unknown; unknown

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
$ docker pull spark@sha256:3c214bac2e2fac9799ec65dd00c0ecbd7c74de375108d3d279b310b6e363e83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17` - linux; amd64

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

### `spark:3.5.1-java17` - unknown; unknown

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
$ docker pull spark@sha256:3c214bac2e2fac9799ec65dd00c0ecbd7c74de375108d3d279b310b6e363e83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-python3` - linux; amd64

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

### `spark:3.5.1-java17-python3` - unknown; unknown

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
$ docker pull spark@sha256:875b91e2734dca2e7c944f7270fc855e8ea3f5da771d8943315eaf4ed0cc619d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:f91a273bb8fec97db75d003c814dd47942b0017c1bdc106452ac4a8f403abc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763806043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c650e7cbbcbfa5f67486f197a8d1e7f41eb2383d5d27e0c57a6f6cbe51b1091e`
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
	-	`sha256:cbb623492f862e9b8cfabea40a94a78cf2ddeed6d6f8d934acebc029c5a69930`  
		Last Modified: Thu, 25 Jul 2024 20:10:17 GMT  
		Size: 323.8 MB (323830999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:c502b288d6828249baceb54f51c37f5db91ba694820ce5575f48a4dfea6a2a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bdd61a5481c7a3cc4572b8a0400b08daf6d17aff2f0a0c6e845e0f3952e344`

```dockerfile
```

-	Layers:
	-	`sha256:50b21bb7105743b26ad9136917f9691ac3ffda46e04175658d5257d0f87ecf79`  
		Last Modified: Thu, 25 Jul 2024 20:10:13 GMT  
		Size: 17.8 MB (17764080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dc441f565736f7710de78f06d94264bcafc2bb6e5f0d6ec6af8d6df9a6f6ff`  
		Last Modified: Thu, 25 Jul 2024 20:10:12 GMT  
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
$ docker pull spark@sha256:0db7831ca121277ac7077edff506d52d17413da4a3ed7f2f7957a4dc7d6cb5fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:cfad58eb143243657a5e2cd7a03eafa8f2e04daee84f225d87ec74272fa86006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 MB (439975044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d6f39fa988af769653beec425d6141db10a003b3d586e11a7db8a1b5d9d40`
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

### `spark:3.5.1-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:5fcf4bf0b947ee3203b8406e1b8b237b3506eeda6d7e1ab413e57a285d9ee244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d23a95ac2ea144b8173de2b060c4508134c53338cbb8a24fe5e07a9ca432f`

```dockerfile
```

-	Layers:
	-	`sha256:700b482ccf75480bfdc8e1ef2daaf0a3baada0d5874f3cb01304b4b91c7a6a17`  
		Last Modified: Thu, 25 Jul 2024 19:08:00 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c945a87cffbad50a1fb2b520cb3fb6520dd67992638460acfb12ea4b3d9106`  
		Last Modified: Thu, 25 Jul 2024 19:07:59 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f7c73fb592809144685304841c5ec0479ae4dded6e080b17c7f098b37820b727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (437009659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22d8f8ecbef40b60cb453b00c5b6c86db4da2a069980db5ba330f752ed164c`
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

### `spark:3.5.1-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:76e72e15f878b2f460fd148931570609b1f41f202666d777b716991ff496a091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3222de6c7b1b9dedac9a91b54f9432c914358fced75cda56a95e226ecc8a294`

```dockerfile
```

-	Layers:
	-	`sha256:6fd6a5f43aba852936b0910016f7c45f4e3f8c0fddf7a609deb776e45cb66f22`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457414ec40a447ddf0e8678a5c0a7819dc110c8f33ebd7c06f3c313fcc846f5d`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-python3`

```console
$ docker pull spark@sha256:69168af92f1f825bcd1453cccc79114a8fc5f4c86c6bc6fbde3dd33cde61666a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-python3` - linux; amd64

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

### `spark:3.5.1-python3` - unknown; unknown

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
$ docker pull spark@sha256:0490120cd277dfba934a0a1fab7518e8396727a5bd7ee0e0419c0822f95f8b5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-r` - linux; amd64

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

### `spark:3.5.1-r` - unknown; unknown

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
$ docker pull spark@sha256:a6f79f0daa5dc41a5e5b3f619442c8e10f6628da76303b1b01ff7ace526308d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala` - linux; amd64

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

### `spark:3.5.1-scala` - unknown; unknown

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

### `spark:3.5.1-scala` - linux; arm64 variant v8

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

### `spark:3.5.1-scala` - unknown; unknown

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

## `spark:3.5.1-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:30ba16c704d4ced86cd5832b71cfe759e3b8a32048f3f0b6ddf4f51c0fadeea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:894daf2a3be9e6890991353e308251005e908cbbcb06bfecc4f7480f01819fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.4 MB (695403150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce73c8381ae3c31819b956dc175e6964c1c3c62305c68dc51cbe8a96b773e71`
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
	-	`sha256:0d4b28c0acd673b88840985bfd22b24c34c0eb003d4d9c8adc0babb406c46028`  
		Last Modified: Thu, 25 Jul 2024 20:09:57 GMT  
		Size: 253.9 MB (253932747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f76ce6661a9b268e4d5a35a8c80cef8481a14579e225e6f47b880f837e0467f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12226457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c9258814cc7306259c91d01d9f839c0e89c7e873f98506779f8a2513fc0cc7`

```dockerfile
```

-	Layers:
	-	`sha256:7eba41589d99385a550980b38ebfec432dfc1229395b721cb5d1a50849efda04`  
		Last Modified: Thu, 25 Jul 2024 20:09:55 GMT  
		Size: 12.2 MB (12215947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d6c92ecd082ab2362b20670d63c768c9326917fd846775e7bf4237bb50052b`  
		Last Modified: Thu, 25 Jul 2024 20:09:54 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ab3511c141b3d9f40dcd5aa85c895019570cb89a452398138770ab7b0372a2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.2 MB (673175005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014ec11a833e248b683480064f51170a2ee963b125ac31c730caf58aae975f4f`
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
	-	`sha256:1723c5074c614031d0bd4b405b6e549785c513aa17b53a26e2a39c3fe0f2f52d`  
		Last Modified: Fri, 26 Jul 2024 00:44:49 GMT  
		Size: 235.1 MB (235141813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:eddba80309b9af612062c7b5336b3f258c04b0f6f31376bd62172f752f0ebb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12211359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac37ba272b0cba3edfdf6d3eff5737aa504b02d1b40e380b1f876e433099d5c5`

```dockerfile
```

-	Layers:
	-	`sha256:b8b150a3b4d0c5daf00b875b6cb5deb1172ef837994ccb597d71893cb28428fe`  
		Last Modified: Fri, 26 Jul 2024 00:44:44 GMT  
		Size: 12.2 MB (12200441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9900b675b1403ce9a0a3bcf80c2348de3e391de5fe6958ebc41e561433e453a`  
		Last Modified: Fri, 26 Jul 2024 00:44:43 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:69168af92f1f825bcd1453cccc79114a8fc5f4c86c6bc6fbde3dd33cde61666a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - linux; amd64

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

### `spark:3.5.1-scala2.12-java11-python3-ubuntu` - unknown; unknown

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
$ docker pull spark@sha256:0490120cd277dfba934a0a1fab7518e8396727a5bd7ee0e0419c0822f95f8b5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - linux; amd64

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

### `spark:3.5.1-scala2.12-java11-r-ubuntu` - unknown; unknown

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
$ docker pull spark@sha256:a6f79f0daa5dc41a5e5b3f619442c8e10f6628da76303b1b01ff7ace526308d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java11-ubuntu` - linux; amd64

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

### `spark:3.5.1-scala2.12-java11-ubuntu` - unknown; unknown

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

### `spark:3.5.1-scala2.12-java11-ubuntu` - linux; arm64 variant v8

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

### `spark:3.5.1-scala2.12-java11-ubuntu` - unknown; unknown

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

## `spark:3.5.1-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:b74157c5b61121b46d675a1a9963624b2d63ec1a99a2022d6d9c6fb907e15c11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0794e0bc23a4f9e35862d75ec5d09e21c0085f7f1611c770386c7cc9548c6540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.5 MB (778520758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0043c4e9edbc647c6e2b0859ce838702a4ec500802e48896424c83cf1aef5e75`
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
	-	`sha256:0d171b3c71448cce0d45fc732832e580ece4df6da57775df3f648cd1a3a6bd93`  
		Last Modified: Thu, 25 Jul 2024 20:10:22 GMT  
		Size: 338.5 MB (338545714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8fa5c5119f343445550b3c5648353f9a71ef79e11786658211e0f41fc60e4d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6c1bb098a238957aea2c4811ae81f3f5ab2f228a480c5104aba8fb7ce3278f`

```dockerfile
```

-	Layers:
	-	`sha256:69c2fb0c92ec5a8207d0cbf94dbf1ecf2f2009809366e9529cdba453d1757206`  
		Last Modified: Thu, 25 Jul 2024 20:10:18 GMT  
		Size: 18.8 MB (18775974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61820bd9ad670850d3e720dd46ef29d212ca59c433a69cb07dec372b19cc2c8e`  
		Last Modified: Thu, 25 Jul 2024 20:10:17 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d8e3d89d00b54b9769dfaf7db89e690c5db16b44c2c2c81b3def481b4de19ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.1 MB (760054077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca259f05d0fab858b71676c665128f37c52ebf00e71fde047270ba93f1d54cc`
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
	-	`sha256:a2d363b2128323684a52987eacbda12a0860852c758531a50d00632627f1cc6b`  
		Last Modified: Fri, 26 Jul 2024 00:38:40 GMT  
		Size: 323.0 MB (323044418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:1dbd3a4e4ea4350c174c78462f9981ef066ef0481f547e1ef0e961ceeb7c9928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18753271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75850a3d0e0c8291111199c920558b75486efc0d5936ac25f2b1616609a594e`

```dockerfile
```

-	Layers:
	-	`sha256:fef856846930b7dac557d72c4549b0832d00d07e0124286ab485a9673f341320`  
		Last Modified: Fri, 26 Jul 2024 00:38:34 GMT  
		Size: 18.7 MB (18742352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306c27b2c08eab045b8469d31a8bbb050c01b2bd8ebd62e9e8e161a2ce9766c5`  
		Last Modified: Fri, 26 Jul 2024 00:38:33 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.1-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:3c214bac2e2fac9799ec65dd00c0ecbd7c74de375108d3d279b310b6e363e83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - linux; amd64

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

### `spark:3.5.1-scala2.12-java17-python3-ubuntu` - unknown; unknown

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
$ docker pull spark@sha256:875b91e2734dca2e7c944f7270fc855e8ea3f5da771d8943315eaf4ed0cc619d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:f91a273bb8fec97db75d003c814dd47942b0017c1bdc106452ac4a8f403abc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.8 MB (763806043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c650e7cbbcbfa5f67486f197a8d1e7f41eb2383d5d27e0c57a6f6cbe51b1091e`
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
	-	`sha256:cbb623492f862e9b8cfabea40a94a78cf2ddeed6d6f8d934acebc029c5a69930`  
		Last Modified: Thu, 25 Jul 2024 20:10:17 GMT  
		Size: 323.8 MB (323830999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.1-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c502b288d6828249baceb54f51c37f5db91ba694820ce5575f48a4dfea6a2a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bdd61a5481c7a3cc4572b8a0400b08daf6d17aff2f0a0c6e845e0f3952e344`

```dockerfile
```

-	Layers:
	-	`sha256:50b21bb7105743b26ad9136917f9691ac3ffda46e04175658d5257d0f87ecf79`  
		Last Modified: Thu, 25 Jul 2024 20:10:13 GMT  
		Size: 17.8 MB (17764080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dc441f565736f7710de78f06d94264bcafc2bb6e5f0d6ec6af8d6df9a6f6ff`  
		Last Modified: Thu, 25 Jul 2024 20:10:12 GMT  
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
$ docker pull spark@sha256:0db7831ca121277ac7077edff506d52d17413da4a3ed7f2f7957a4dc7d6cb5fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.1-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:cfad58eb143243657a5e2cd7a03eafa8f2e04daee84f225d87ec74272fa86006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 MB (439975044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d6f39fa988af769653beec425d6141db10a003b3d586e11a7db8a1b5d9d40`
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

### `spark:3.5.1-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5fcf4bf0b947ee3203b8406e1b8b237b3506eeda6d7e1ab413e57a285d9ee244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d23a95ac2ea144b8173de2b060c4508134c53338cbb8a24fe5e07a9ca432f`

```dockerfile
```

-	Layers:
	-	`sha256:700b482ccf75480bfdc8e1ef2daaf0a3baada0d5874f3cb01304b4b91c7a6a17`  
		Last Modified: Thu, 25 Jul 2024 19:08:00 GMT  
		Size: 4.2 MB (4217794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c945a87cffbad50a1fb2b520cb3fb6520dd67992638460acfb12ea4b3d9106`  
		Last Modified: Thu, 25 Jul 2024 19:07:59 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.1-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f7c73fb592809144685304841c5ec0479ae4dded6e080b17c7f098b37820b727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (437009659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22d8f8ecbef40b60cb453b00c5b6c86db4da2a069980db5ba330f752ed164c`
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

### `spark:3.5.1-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:76e72e15f878b2f460fd148931570609b1f41f202666d777b716991ff496a091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3222de6c7b1b9dedac9a91b54f9432c914358fced75cda56a95e226ecc8a294`

```dockerfile
```

-	Layers:
	-	`sha256:6fd6a5f43aba852936b0910016f7c45f4e3f8c0fddf7a609deb776e45cb66f22`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 4.2 MB (4218109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457414ec40a447ddf0e8678a5c0a7819dc110c8f33ebd7c06f3c313fcc846f5d`  
		Last Modified: Thu, 25 Jul 2024 22:58:52 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:69168af92f1f825bcd1453cccc79114a8fc5f4c86c6bc6fbde3dd33cde61666a
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
$ docker pull spark@sha256:69168af92f1f825bcd1453cccc79114a8fc5f4c86c6bc6fbde3dd33cde61666a
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
$ docker pull spark@sha256:3c214bac2e2fac9799ec65dd00c0ecbd7c74de375108d3d279b310b6e363e83d
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
$ docker pull spark@sha256:0490120cd277dfba934a0a1fab7518e8396727a5bd7ee0e0419c0822f95f8b5f
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
