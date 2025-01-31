<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spark`

-	[`spark:3.4.4`](#spark344)
-	[`spark:3.4.4-python3`](#spark344-python3)
-	[`spark:3.4.4-r`](#spark344-r)
-	[`spark:3.4.4-scala`](#spark344-scala)
-	[`spark:3.4.4-scala2.12-java11-python3-r-ubuntu`](#spark344-scala212-java11-python3-r-ubuntu)
-	[`spark:3.4.4-scala2.12-java11-python3-ubuntu`](#spark344-scala212-java11-python3-ubuntu)
-	[`spark:3.4.4-scala2.12-java11-r-ubuntu`](#spark344-scala212-java11-r-ubuntu)
-	[`spark:3.4.4-scala2.12-java11-ubuntu`](#spark344-scala212-java11-ubuntu)
-	[`spark:3.5.4`](#spark354)
-	[`spark:3.5.4-java17`](#spark354-java17)
-	[`spark:3.5.4-java17-python3`](#spark354-java17-python3)
-	[`spark:3.5.4-java17-r`](#spark354-java17-r)
-	[`spark:3.5.4-java17-scala`](#spark354-java17-scala)
-	[`spark:3.5.4-python3`](#spark354-python3)
-	[`spark:3.5.4-r`](#spark354-r)
-	[`spark:3.5.4-scala`](#spark354-scala)
-	[`spark:3.5.4-scala2.12-java11-python3-r-ubuntu`](#spark354-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.4-scala2.12-java11-python3-ubuntu`](#spark354-scala212-java11-python3-ubuntu)
-	[`spark:3.5.4-scala2.12-java11-r-ubuntu`](#spark354-scala212-java11-r-ubuntu)
-	[`spark:3.5.4-scala2.12-java11-ubuntu`](#spark354-scala212-java11-ubuntu)
-	[`spark:3.5.4-scala2.12-java17-python3-r-ubuntu`](#spark354-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.4-scala2.12-java17-python3-ubuntu`](#spark354-scala212-java17-python3-ubuntu)
-	[`spark:3.5.4-scala2.12-java17-r-ubuntu`](#spark354-scala212-java17-r-ubuntu)
-	[`spark:3.5.4-scala2.12-java17-ubuntu`](#spark354-scala212-java17-ubuntu)
-	[`spark:4.0.0-preview2`](#spark400-preview2)
-	[`spark:4.0.0-preview2-java21`](#spark400-preview2-java21)
-	[`spark:4.0.0-preview2-java21-python3`](#spark400-preview2-java21-python3)
-	[`spark:4.0.0-preview2-java21-r`](#spark400-preview2-java21-r)
-	[`spark:4.0.0-preview2-java21-scala`](#spark400-preview2-java21-scala)
-	[`spark:4.0.0-preview2-python3`](#spark400-preview2-python3)
-	[`spark:4.0.0-preview2-r`](#spark400-preview2-r)
-	[`spark:4.0.0-preview2-scala`](#spark400-preview2-scala)
-	[`spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu`](#spark400-preview2-scala213-java17-python3-r-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu`](#spark400-preview2-scala213-java17-python3-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java17-r-ubuntu`](#spark400-preview2-scala213-java17-r-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java17-ubuntu`](#spark400-preview2-scala213-java17-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu`](#spark400-preview2-scala213-java21-python3-r-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu`](#spark400-preview2-scala213-java21-python3-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java21-r-ubuntu`](#spark400-preview2-scala213-java21-r-ubuntu)
-	[`spark:4.0.0-preview2-scala2.13-java21-ubuntu`](#spark400-preview2-scala213-java21-ubuntu)
-	[`spark:latest`](#sparklatest)
-	[`spark:python3`](#sparkpython3)
-	[`spark:python3-java17`](#sparkpython3-java17)
-	[`spark:r`](#sparkr)
-	[`spark:scala`](#sparkscala)

## `spark:3.4.4`

```console
$ docker pull spark@sha256:dd9768d30b606796e96856274ce920ccf39ba32dadf18b3293e178eada4d67d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4` - linux; amd64

```console
$ docker pull spark@sha256:5ed3f7b1e5e63812d86bec89430cdc296eee2ff054d54282f1d2cf8769cd5d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528543479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a890e79c9c93de465b252c01319e70c43702556c71dcd95847817d3ee5137c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b305749987c7b41a50b3616d9b8c020fb7674ae03ebe06a66fa380fcffb4a145`  
		Last Modified: Fri, 31 Jan 2025 03:12:39 GMT  
		Size: 94.4 MB (94373553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4` - unknown; unknown

```console
$ docker pull spark@sha256:0eeaa199f92710f50bf11ed3d4e066eeddfc3c299f3edebd7f7cdcce33a54809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9075203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfbcb0366b178e616914eba43e1c5de9b8dcf9f437a04b895173c6b81ba7253`

```dockerfile
```

-	Layers:
	-	`sha256:8b6d2139ccb8fe381dd2b985270c2a909ebffe0df612cbe3e3dfedf8baeff06c`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 9.1 MB (9064234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b527078066c461d4a1bd3f45b17bb8f178c2ff070c3cab115e3a11327dde`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7677fb1834d708b9de26c2a0c69e14ffde894270c748f64d11088993e100100b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.9 MB (517889717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19c4c30e3337eae2bd1a6884d7da1c9df95d9151d4aa3537716e756ba2dbaf5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cb2958a5fd78134c636f67a6b7b7e62fc9c5071bcdde17bb8ebd4344f0add6`  
		Last Modified: Fri, 31 Jan 2025 06:10:27 GMT  
		Size: 87.3 MB (87316669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4` - unknown; unknown

```console
$ docker pull spark@sha256:8e700f35874a62b9d6d64e96a707f6b3c51bb771a940a45fd8144b6d5b4afdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208f641b057fb1fba8602332e12496765eb7e67cd5be04e31afadd96e48407ad`

```dockerfile
```

-	Layers:
	-	`sha256:9677ba85da3c15aad7c0f51d2e8f5f61dbba26d0f6b6dd7743604498bdb1476e`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 9.1 MB (9069905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a330806aeaeacfe72ab26f96fedf239c6a510310f4732f3c0874e5528f1e6a38`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-python3`

```console
$ docker pull spark@sha256:dd9768d30b606796e96856274ce920ccf39ba32dadf18b3293e178eada4d67d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-python3` - linux; amd64

```console
$ docker pull spark@sha256:5ed3f7b1e5e63812d86bec89430cdc296eee2ff054d54282f1d2cf8769cd5d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528543479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a890e79c9c93de465b252c01319e70c43702556c71dcd95847817d3ee5137c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b305749987c7b41a50b3616d9b8c020fb7674ae03ebe06a66fa380fcffb4a145`  
		Last Modified: Fri, 31 Jan 2025 03:12:39 GMT  
		Size: 94.4 MB (94373553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-python3` - unknown; unknown

```console
$ docker pull spark@sha256:0eeaa199f92710f50bf11ed3d4e066eeddfc3c299f3edebd7f7cdcce33a54809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9075203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfbcb0366b178e616914eba43e1c5de9b8dcf9f437a04b895173c6b81ba7253`

```dockerfile
```

-	Layers:
	-	`sha256:8b6d2139ccb8fe381dd2b985270c2a909ebffe0df612cbe3e3dfedf8baeff06c`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 9.1 MB (9064234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b527078066c461d4a1bd3f45b17bb8f178c2ff070c3cab115e3a11327dde`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7677fb1834d708b9de26c2a0c69e14ffde894270c748f64d11088993e100100b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.9 MB (517889717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19c4c30e3337eae2bd1a6884d7da1c9df95d9151d4aa3537716e756ba2dbaf5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cb2958a5fd78134c636f67a6b7b7e62fc9c5071bcdde17bb8ebd4344f0add6`  
		Last Modified: Fri, 31 Jan 2025 06:10:27 GMT  
		Size: 87.3 MB (87316669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-python3` - unknown; unknown

```console
$ docker pull spark@sha256:8e700f35874a62b9d6d64e96a707f6b3c51bb771a940a45fd8144b6d5b4afdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208f641b057fb1fba8602332e12496765eb7e67cd5be04e31afadd96e48407ad`

```dockerfile
```

-	Layers:
	-	`sha256:9677ba85da3c15aad7c0f51d2e8f5f61dbba26d0f6b6dd7743604498bdb1476e`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 9.1 MB (9069905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a330806aeaeacfe72ab26f96fedf239c6a510310f4732f3c0874e5528f1e6a38`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-r`

```console
$ docker pull spark@sha256:f859abeb7b8dbb5e876b2292c1cb5bab33a25a0f744b1eadff96629efa142f18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-r` - linux; amd64

```console
$ docker pull spark@sha256:507888cba41681701c049a77d36fad03eb60c22b8c6681d79a0a924d5a6d7013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666452283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f062f9d15bea1be726fb7ba1bab79d9def0eb25c71cc4f71c5582db167cadf2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77701238ac1ec73ae00ddfc233405225b140810699429c1b7854f1620fc99a8d`  
		Last Modified: Fri, 31 Jan 2025 03:13:12 GMT  
		Size: 232.3 MB (232282357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-r` - unknown; unknown

```console
$ docker pull spark@sha256:6564a0cc3e516f2774370226ef942aa838cb418047c6898b8c630a2961ab8077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11247559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d16cc183a12db646fec9c184739f3c2e673083484878e53982ad48c8828f3a`

```dockerfile
```

-	Layers:
	-	`sha256:9e6ef89afeebe162a78fb231279d0ca21a4012a0c1f52e85531d4a9d2c4a8477`  
		Last Modified: Fri, 31 Jan 2025 03:13:09 GMT  
		Size: 11.2 MB (11236893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e07942b627a9fb597e4be79457fcf60841b9fdf5934604787102aa8c5884d45`  
		Last Modified: Fri, 31 Jan 2025 03:13:09 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e673e573778e263a9be7c47d82f47a88f2b2c3afc23ad7171c1cff4e7e01d28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644076178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30600d093656830b04f6326811dbf6a65b5585baa7b6f74efdbf63473bddbb1c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234e84cba87035bf7dfe3be827223476701cf4bf255fde1f9c0a1cf41a62dd8`  
		Last Modified: Fri, 31 Jan 2025 06:12:07 GMT  
		Size: 213.5 MB (213503130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-r` - unknown; unknown

```console
$ docker pull spark@sha256:08229c400f0080e9accc6b6c8a97bd90ec69b25b10215938f948ee985bbebca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5f9a4891a17410fd850f535b1db220810744b683689e12d7df0c7e199ac4c`

```dockerfile
```

-	Layers:
	-	`sha256:e4cd99aae3fcca7be7ed79752de02a00e62a8ea336ddd3967163ecbde84d126b`  
		Last Modified: Fri, 31 Jan 2025 06:12:02 GMT  
		Size: 11.2 MB (11222922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98ee6b9bd193caadfeeda3d0cb35a75c701a25eaaa9cb8b85659dfd31f47f13`  
		Last Modified: Fri, 31 Jan 2025 06:12:00 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-scala`

```console
$ docker pull spark@sha256:f414535e9bb077d7fb50886504090f07e6f6d0ee2ad578e31687bb0e4b834f70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-scala` - linux; amd64

```console
$ docker pull spark@sha256:25fef261029783f975be10d5705080e098524161d59a03b25e82bdc3565ba4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434169926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d26e008bbf26c3423938643b932287c54007bedd29885585d7f47637de671c2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala` - unknown; unknown

```console
$ docker pull spark@sha256:06c5c85b904cac3ebba63b2d5c9e9578e1f9b08c9ebddb2b2c344a65cb9af906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796e486b341095e5442eb39bb3fa00fda8063fdef82f100898591e71fe63ae71`

```dockerfile
```

-	Layers:
	-	`sha256:6b09846cb808813871ece793a7961efc195a387773f8a9ece945d50a2d1c9400`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 4.3 MB (4340259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31aabc7167971acda4dde00cc968e565069704dc6dbf08f6b5c4b0cdc8d0b636`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 22.9 KB (22853 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1b3dcc12f8302c96fa125fe8a78cd62e9c82d143e40bdd343bdc8c57bd1c3980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430573048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e31bcb9c9627eccb648539d5e1be2357fc640e8754b48209bd1771a0c04b115`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala` - unknown; unknown

```console
$ docker pull spark@sha256:bbc17b25e3a35920e0003fd6841400168181adf28327992d280272dff4fa4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03324e51f9ea8e2fc65c816e896f5220505ac78596d87f27dbbe8f1a8268ee14`

```dockerfile
```

-	Layers:
	-	`sha256:937a299bd2697eeb47bd0cbc50f8c648b9ecb2a4f4896f2d03e7af100adb6dc9`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 4.3 MB (4342427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a277d83765190838c570c469f24fbd307a8933e47add33f298e0d3a7ca9a82`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 23.0 KB (22964 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:1ac1191e1c2155cfe3c0d87b9c3573b404f8e4e7fee893ac4af6ca6e986af58d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:49df3161ac76dcc42bebcdc49f1f0be2e33897d3d450798cc33046d208c4fbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.1 MB (688078780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706d777ea4b8dda2c7e7ea5abdcc8af526ecbfcd2b59284e0f4001cc54153ae`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5d795d469b03ccc1e0e5da0877aaaca4c98fae572f019cd1eb7a9c55d8eec`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 253.9 MB (253908854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9755c495fe28a0a43ccb30761fe5179c19fcdea7ddafb3c0868d63d9dac2d619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12371680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3bcb3444deb7e073cb114c3474de77ddbbf77ecbae8cf3d7e9dd3c1395aad3`

```dockerfile
```

-	Layers:
	-	`sha256:ad69b30fb15efe565e32975e98d5b1e369261e941eed2d7431369373c62b22d6`  
		Last Modified: Fri, 31 Jan 2025 03:13:18 GMT  
		Size: 12.4 MB (12361136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4011f51f13138ca1edb7323272b2808715ff5dd0f8c7dd6a2ea946ea455319bb`  
		Last Modified: Fri, 31 Jan 2025 03:13:17 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9ea092874187bc236add02874933b946cea631cc19168a13615f6f52a05bfd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.7 MB (665718053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae786af0f0c3737cb612d4ee5f9efb511bf073bb0eed67608c00f49937548ba`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46f839d90526f66b84569320cc864f726a11caf74b074eb6eff1a41727d0995`  
		Last Modified: Fri, 31 Jan 2025 05:56:03 GMT  
		Size: 235.1 MB (235145005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6e91ca4040eb155c778537d77f4b95d799c5ca43d1e18d865eb3c43491311073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12357832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d76dcde4b1059c2c440ac1e2f6fc3e0b9be5b4a35207e89ec2efcbd392624b`

```dockerfile
```

-	Layers:
	-	`sha256:026a2996c1f8546479d87fb5b1b194ab9ea2ab42e22d6e67811a7cd7a914d494`  
		Last Modified: Fri, 31 Jan 2025 05:55:58 GMT  
		Size: 12.3 MB (12347220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed32aecde5e74467470e70f74b702c8c8ae8646a62944217b8752b4c4fdce5`  
		Last Modified: Fri, 31 Jan 2025 05:55:57 GMT  
		Size: 10.6 KB (10612 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:dd9768d30b606796e96856274ce920ccf39ba32dadf18b3293e178eada4d67d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:5ed3f7b1e5e63812d86bec89430cdc296eee2ff054d54282f1d2cf8769cd5d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528543479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a890e79c9c93de465b252c01319e70c43702556c71dcd95847817d3ee5137c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b305749987c7b41a50b3616d9b8c020fb7674ae03ebe06a66fa380fcffb4a145`  
		Last Modified: Fri, 31 Jan 2025 03:12:39 GMT  
		Size: 94.4 MB (94373553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0eeaa199f92710f50bf11ed3d4e066eeddfc3c299f3edebd7f7cdcce33a54809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9075203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfbcb0366b178e616914eba43e1c5de9b8dcf9f437a04b895173c6b81ba7253`

```dockerfile
```

-	Layers:
	-	`sha256:8b6d2139ccb8fe381dd2b985270c2a909ebffe0df612cbe3e3dfedf8baeff06c`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 9.1 MB (9064234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b527078066c461d4a1bd3f45b17bb8f178c2ff070c3cab115e3a11327dde`  
		Last Modified: Fri, 31 Jan 2025 03:12:38 GMT  
		Size: 11.0 KB (10969 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:7677fb1834d708b9de26c2a0c69e14ffde894270c748f64d11088993e100100b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.9 MB (517889717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19c4c30e3337eae2bd1a6884d7da1c9df95d9151d4aa3537716e756ba2dbaf5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cb2958a5fd78134c636f67a6b7b7e62fc9c5071bcdde17bb8ebd4344f0add6`  
		Last Modified: Fri, 31 Jan 2025 06:10:27 GMT  
		Size: 87.3 MB (87316669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8e700f35874a62b9d6d64e96a707f6b3c51bb771a940a45fd8144b6d5b4afdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9080966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208f641b057fb1fba8602332e12496765eb7e67cd5be04e31afadd96e48407ad`

```dockerfile
```

-	Layers:
	-	`sha256:9677ba85da3c15aad7c0f51d2e8f5f61dbba26d0f6b6dd7743604498bdb1476e`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 9.1 MB (9069905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a330806aeaeacfe72ab26f96fedf239c6a510310f4732f3c0874e5528f1e6a38`  
		Last Modified: Fri, 31 Jan 2025 06:10:24 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:f859abeb7b8dbb5e876b2292c1cb5bab33a25a0f744b1eadff96629efa142f18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:507888cba41681701c049a77d36fad03eb60c22b8c6681d79a0a924d5a6d7013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666452283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f062f9d15bea1be726fb7ba1bab79d9def0eb25c71cc4f71c5582db167cadf2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77701238ac1ec73ae00ddfc233405225b140810699429c1b7854f1620fc99a8d`  
		Last Modified: Fri, 31 Jan 2025 03:13:12 GMT  
		Size: 232.3 MB (232282357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6564a0cc3e516f2774370226ef942aa838cb418047c6898b8c630a2961ab8077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11247559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d16cc183a12db646fec9c184739f3c2e673083484878e53982ad48c8828f3a`

```dockerfile
```

-	Layers:
	-	`sha256:9e6ef89afeebe162a78fb231279d0ca21a4012a0c1f52e85531d4a9d2c4a8477`  
		Last Modified: Fri, 31 Jan 2025 03:13:09 GMT  
		Size: 11.2 MB (11236893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e07942b627a9fb597e4be79457fcf60841b9fdf5934604787102aa8c5884d45`  
		Last Modified: Fri, 31 Jan 2025 03:13:09 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e673e573778e263a9be7c47d82f47a88f2b2c3afc23ad7171c1cff4e7e01d28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644076178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30600d093656830b04f6326811dbf6a65b5585baa7b6f74efdbf63473bddbb1c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
USER root
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV R_HOME=/usr/lib/R
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234e84cba87035bf7dfe3be827223476701cf4bf255fde1f9c0a1cf41a62dd8`  
		Last Modified: Fri, 31 Jan 2025 06:12:07 GMT  
		Size: 213.5 MB (213503130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:08229c400f0080e9accc6b6c8a97bd90ec69b25b10215938f948ee985bbebca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a5f9a4891a17410fd850f535b1db220810744b683689e12d7df0c7e199ac4c`

```dockerfile
```

-	Layers:
	-	`sha256:e4cd99aae3fcca7be7ed79752de02a00e62a8ea336ddd3967163ecbde84d126b`  
		Last Modified: Fri, 31 Jan 2025 06:12:02 GMT  
		Size: 11.2 MB (11222922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98ee6b9bd193caadfeeda3d0cb35a75c701a25eaaa9cb8b85659dfd31f47f13`  
		Last Modified: Fri, 31 Jan 2025 06:12:00 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.4-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:f414535e9bb077d7fb50886504090f07e6f6d0ee2ad578e31687bb0e4b834f70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.4-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:25fef261029783f975be10d5705080e098524161d59a03b25e82bdc3565ba4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434169926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d26e008bbf26c3423938643b932287c54007bedd29885585d7f47637de671c2`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703f3157e04f09a0e29e539a4bf42e54f0dae3258eb351228bcf1904a6a5066`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2ee6cbfeeff4adfdbaffa326262035ab90f791be050e587be34a138ec009`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c1cd5fb69d4f426cca43f8848da3581b4fa6df4fa34dd167a4dab11fb70d73`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 318.6 MB (318551944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12998ec048a33919bc33d0b484eafb38e35399175aace452a680b073e1fab`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:06c5c85b904cac3ebba63b2d5c9e9578e1f9b08c9ebddb2b2c344a65cb9af906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796e486b341095e5442eb39bb3fa00fda8063fdef82f100898591e71fe63ae71`

```dockerfile
```

-	Layers:
	-	`sha256:6b09846cb808813871ece793a7961efc195a387773f8a9ece945d50a2d1c9400`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 4.3 MB (4340259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31aabc7167971acda4dde00cc968e565069704dc6dbf08f6b5c4b0cdc8d0b636`  
		Last Modified: Fri, 31 Jan 2025 02:17:44 GMT  
		Size: 22.9 KB (22853 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.4-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1b3dcc12f8302c96fa125fe8a78cd62e9c82d143e40bdd343bdc8c57bd1c3980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430573048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e31bcb9c9627eccb648539d5e1be2357fc640e8754b48209bd1771a0c04b115`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Oct 2024 07:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Oct 2024 07:49:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 27 Oct 2024 07:49:23 GMT
ARG spark_uid=185
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.4/spark-3.4.4-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Sun, 27 Oct 2024 07:49:23 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 27 Oct 2024 07:49:23 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 27 Oct 2024 07:49:23 GMT
WORKDIR /opt/spark/work-dir
# Sun, 27 Oct 2024 07:49:23 GMT
USER spark
# Sun, 27 Oct 2024 07:49:23 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce955d3ddda97837b5c9d5c373bb0a41555d2b5e7936cf51b22b8e7a9ad416`  
		Last Modified: Fri, 31 Jan 2025 04:19:36 GMT  
		Size: 318.6 MB (318551918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3053a9463a205c136654de2dfa038093e3efd9d298db8a6c181e9f82c8cb7`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.4-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:bbc17b25e3a35920e0003fd6841400168181adf28327992d280272dff4fa4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03324e51f9ea8e2fc65c816e896f5220505ac78596d87f27dbbe8f1a8268ee14`

```dockerfile
```

-	Layers:
	-	`sha256:937a299bd2697eeb47bd0cbc50f8c648b9ecb2a4f4896f2d03e7af100adb6dc9`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 4.3 MB (4342427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a277d83765190838c570c469f24fbd307a8933e47add33f298e0d3a7ca9a82`  
		Last Modified: Fri, 31 Jan 2025 04:19:28 GMT  
		Size: 23.0 KB (22964 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4`

```console
$ docker pull spark@sha256:9c89501658cf8051f26a7156108245a1c128a8447d5b88e195f63e57f3ef7b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4` - linux; amd64

```console
$ docker pull spark@sha256:886a198dbcc19ed8debb05d53adb42ce8482d896bf72f2ddeec5597afbebb2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.9 MB (534893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908cada5243a3cbaaed9663871209f94f4a1494d8295575de158cd1735096de`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65562d4e36cf032078e3e7a22b283a882606acaebcbb6da874525f52cd4d9a07`  
		Last Modified: Fri, 31 Jan 2025 03:12:34 GMT  
		Size: 94.4 MB (94374134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4` - unknown; unknown

```console
$ docker pull spark@sha256:6bf91d20f8e5cadd06a266208e4fe9993a03a22fafaf67876675ef7e40a918b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9086133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f84642d1cfed441b76b10552b1211c8f89c5d4ff4aaab2529563c8606eba9`

```dockerfile
```

-	Layers:
	-	`sha256:31ec2dbde6aacada546abe304fd328616f596cb04eb6d603276954d7baed0011`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 9.1 MB (9074570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e914d424e086fc494cc4b1a20826c9ce52b661c50e94baf44a265bb332c039`  
		Last Modified: Fri, 31 Jan 2025 03:12:32 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49cadd84c9108c41d656748a6ceeb837be2694da7fbc803a0bb25e0c7f2f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524240196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e4d315310353f4daad37b33f1b44faa3eaa3ccdd5973cd9dc1639b27851ec9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c9f920fc07078b9a1e0ae471b76d758717ece2429a04f85e8e6d79275c2a`  
		Last Modified: Fri, 31 Jan 2025 06:07:29 GMT  
		Size: 87.3 MB (87317317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4` - unknown; unknown

```console
$ docker pull spark@sha256:6ac2cc9df80a940059df674017b44946a2093eb9d91527d3f362cb57e9c32dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9091944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3d7eefeb7d586ced21ace0a174e158fe8b6569f91ee85b4cc552833aea5ba`

```dockerfile
```

-	Layers:
	-	`sha256:b634c3c799883509bce1b89c75c2ead96d659b0dfaf13e9b735c718e00c54000`  
		Last Modified: Fri, 31 Jan 2025 06:07:26 GMT  
		Size: 9.1 MB (9080265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6cacc0203203bb5e2b0dc5b58eea283236dd387f6380115979003d44d231d`  
		Last Modified: Fri, 31 Jan 2025 06:07:25 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-java17`

```console
$ docker pull spark@sha256:f536843be0fef2545bb8db1ce210ccfd6966eff87c9f519922f21cca1cfc4a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-java17` - linux; amd64

```console
$ docker pull spark@sha256:383b3411722669803b7d54d31c368db921fd6ac00a172347bad13838df864f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655400658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080370b103d53102913defc47db299cf8c84a0dcdfc1114e258d5338009c575b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa771bc14209e0ddd4129308701f44b374c3905bb86c3c95e805637191c179`  
		Last Modified: Fri, 31 Jan 2025 03:12:47 GMT  
		Size: 113.7 MB (113725771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17` - unknown; unknown

```console
$ docker pull spark@sha256:6c7d2f3194ed18184e25862d81ddff116f3fe15c205b4303d05dfd75a69fc856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9960679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce619a89f730e1709f79d1f25800907be8ee57992cf57673189c475cd4e2021`

```dockerfile
```

-	Layers:
	-	`sha256:f498d72f3532c8330f46721d5375ac45e80b30ebeff414c30f3aeeda997d142c`  
		Last Modified: Fri, 31 Jan 2025 03:12:46 GMT  
		Size: 9.9 MB (9949367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680087c13487029bd68cbc70beb360f462e2167dac1ec9c721f99c881ff12ecf`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0035a0f37dacf7ad863461eba7b6108420164ef095141df232ecc4bec9dec823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.7 MB (647722618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf011250ad3089b06baae753527141ab7d762629d7529560da2242024663be6b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce5be925d803291ff779168f5a37bf8decd84fab19dd5de2a221bdaa1b1cb6`  
		Last Modified: Fri, 31 Jan 2025 06:29:56 GMT  
		Size: 108.3 MB (108282160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17` - unknown; unknown

```console
$ docker pull spark@sha256:73c314022843f8a8ffedb5bb0caf95f0b91554c00c30be8caa64032772ae30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9957117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205ae0a5b5162ee14246fca50ee83b08cc7c899d4864a800a0b4e03c5fe29ad7`

```dockerfile
```

-	Layers:
	-	`sha256:25a13257f4dc2380e2dbf2e58417ec2dda7ad6fd631466385c12af1c7a200aa3`  
		Last Modified: Fri, 31 Jan 2025 06:29:55 GMT  
		Size: 9.9 MB (9945701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76f02694597ce6d986a2d3bdc174ab3e3dc7e3204b2a0963f2990ebe19e82d8`  
		Last Modified: Fri, 31 Jan 2025 06:29:53 GMT  
		Size: 11.4 KB (11416 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-java17-python3`

```console
$ docker pull spark@sha256:f536843be0fef2545bb8db1ce210ccfd6966eff87c9f519922f21cca1cfc4a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:383b3411722669803b7d54d31c368db921fd6ac00a172347bad13838df864f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655400658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080370b103d53102913defc47db299cf8c84a0dcdfc1114e258d5338009c575b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa771bc14209e0ddd4129308701f44b374c3905bb86c3c95e805637191c179`  
		Last Modified: Fri, 31 Jan 2025 03:12:47 GMT  
		Size: 113.7 MB (113725771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:6c7d2f3194ed18184e25862d81ddff116f3fe15c205b4303d05dfd75a69fc856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9960679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce619a89f730e1709f79d1f25800907be8ee57992cf57673189c475cd4e2021`

```dockerfile
```

-	Layers:
	-	`sha256:f498d72f3532c8330f46721d5375ac45e80b30ebeff414c30f3aeeda997d142c`  
		Last Modified: Fri, 31 Jan 2025 03:12:46 GMT  
		Size: 9.9 MB (9949367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680087c13487029bd68cbc70beb360f462e2167dac1ec9c721f99c881ff12ecf`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0035a0f37dacf7ad863461eba7b6108420164ef095141df232ecc4bec9dec823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.7 MB (647722618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf011250ad3089b06baae753527141ab7d762629d7529560da2242024663be6b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce5be925d803291ff779168f5a37bf8decd84fab19dd5de2a221bdaa1b1cb6`  
		Last Modified: Fri, 31 Jan 2025 06:29:56 GMT  
		Size: 108.3 MB (108282160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:73c314022843f8a8ffedb5bb0caf95f0b91554c00c30be8caa64032772ae30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9957117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205ae0a5b5162ee14246fca50ee83b08cc7c899d4864a800a0b4e03c5fe29ad7`

```dockerfile
```

-	Layers:
	-	`sha256:25a13257f4dc2380e2dbf2e58417ec2dda7ad6fd631466385c12af1c7a200aa3`  
		Last Modified: Fri, 31 Jan 2025 06:29:55 GMT  
		Size: 9.9 MB (9945701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76f02694597ce6d986a2d3bdc174ab3e3dc7e3204b2a0963f2990ebe19e82d8`  
		Last Modified: Fri, 31 Jan 2025 06:29:53 GMT  
		Size: 11.4 KB (11416 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-java17-r`

```console
$ docker pull spark@sha256:4f694db01bb17cc09b6238c64ccff5b01e87d9fa562b208f8ebc97d809ed0f14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:515d835b12967a7fa353d58d5f31a0c2973741e254dee33bd82795543a732659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.0 MB (860977435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e12c97462625a858891d26aa149f73ae883ac97c627dc708d2f239d59a20c2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef74374a613c754d3509247356545e60a97765aeaac8b814d2f47bdcf35f673`  
		Last Modified: Fri, 31 Jan 2025 03:13:31 GMT  
		Size: 319.3 MB (319302548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:e88f04979f612362f60a782b84cbfed68e4562dfaabf0c972f172b652092ece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18002912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57b3d821ed92a82f88f8a370b59269063a9b111693d1cd2faf6d4cb4dfdf`

```dockerfile
```

-	Layers:
	-	`sha256:bc6c85b9f6311d653926ae4a83df1b883773b4b3b58dadbb06806686aee1e2ae`  
		Last Modified: Fri, 31 Jan 2025 03:13:27 GMT  
		Size: 18.0 MB (17992230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf2ea6bac999d3dbc1b5055110e543234a77ecb05c2d801a10da2c9a24a5cf6`  
		Last Modified: Fri, 31 Jan 2025 03:13:27 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:710f0918b36cbb6ced2fa2ee2113ea9798fbe43bd3ff19045d4ba9b5c9e4c537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.9 MB (841941529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ca21e7af981b7d07af4d3ac25be67601a156995039c3288b734774c0321545`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2251e69c651925e20d7d3660ebd8741eb1f8f056f0344b5f427170ed91b936`  
		Last Modified: Fri, 31 Jan 2025 06:06:11 GMT  
		Size: 302.5 MB (302501071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:bee74b7fd320a06c59897796d9ee11520c0f5e909914890ba5fc21ef2b799cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17970290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd57d3bfe9c473a135005faf0b28244f613b23821ada0b200866ed26278d1e1`

```dockerfile
```

-	Layers:
	-	`sha256:f789c1604512e67468300537383713f684eb2255a3bd645e707000bfd41766da`  
		Last Modified: Fri, 31 Jan 2025 06:06:05 GMT  
		Size: 18.0 MB (17959528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b5224c5657f8ceffc3491b12553f6d9ad6d2493d25f52e1e1ed61cbe47ef87`  
		Last Modified: Fri, 31 Jan 2025 06:06:04 GMT  
		Size: 10.8 KB (10762 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-java17-scala`

```console
$ docker pull spark@sha256:aa55470bc90149c3455593a7be515872893dad4db17f7da5e00b44e003d324eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:a33e68a39aa35b6fe01f134f9aa130e1dd51c9a06b3b4f52527db670008510fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.7 MB (541674887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6e96d8a284679b2ae06849d5442ffa0031126b0c15c388cdffb3729dcf7cd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:5ea3453a4eee92c0b3d7602664a70ad98e455df5b3807bc58159f5e9a34b3374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e8d50adc2b2eeb9a86f367e7e3e2a2f2b31f2aa6c1049b2d5d0efe360d7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:13c980d78b8e0bece816d09f471e7f8af37c440691d4085882249563874313e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 4.6 MB (4582213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec481b4372dcd17f6e40bee42d99229b38dcc9c448a1df1bafc5f00bf2d4811`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1f9030dc5f9a1077b6442105b5a4717d3d3bb1165e6bce6ef72c8f2ae7706d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539440458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd60fc0780bc9191b17c7ecc4609ab4f9908ef98fe2ccf98056339bc76efe0`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:9ef0798d7ef50c4f62bca963389a2caf9a2127a6ea39e96db02ff082bd4d5b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4702564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b548cb3c8b09794ebc9a15d17e3cc1d47097e23efb9af26e56c0035eb44b4042`

```dockerfile
```

-	Layers:
	-	`sha256:e5932b522efc822741671bbd24a0a11d4c0c608ff7ceaec23e0d473d8a0a3e98`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 4.7 MB (4679588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86dc5e2d1e08bf62753fce1c877fd94c076d8cf13da1be541a4250f261892ce`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-python3`

```console
$ docker pull spark@sha256:9c89501658cf8051f26a7156108245a1c128a8447d5b88e195f63e57f3ef7b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-python3` - linux; amd64

```console
$ docker pull spark@sha256:886a198dbcc19ed8debb05d53adb42ce8482d896bf72f2ddeec5597afbebb2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.9 MB (534893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908cada5243a3cbaaed9663871209f94f4a1494d8295575de158cd1735096de`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65562d4e36cf032078e3e7a22b283a882606acaebcbb6da874525f52cd4d9a07`  
		Last Modified: Fri, 31 Jan 2025 03:12:34 GMT  
		Size: 94.4 MB (94374134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-python3` - unknown; unknown

```console
$ docker pull spark@sha256:6bf91d20f8e5cadd06a266208e4fe9993a03a22fafaf67876675ef7e40a918b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9086133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f84642d1cfed441b76b10552b1211c8f89c5d4ff4aaab2529563c8606eba9`

```dockerfile
```

-	Layers:
	-	`sha256:31ec2dbde6aacada546abe304fd328616f596cb04eb6d603276954d7baed0011`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 9.1 MB (9074570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e914d424e086fc494cc4b1a20826c9ce52b661c50e94baf44a265bb332c039`  
		Last Modified: Fri, 31 Jan 2025 03:12:32 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49cadd84c9108c41d656748a6ceeb837be2694da7fbc803a0bb25e0c7f2f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524240196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e4d315310353f4daad37b33f1b44faa3eaa3ccdd5973cd9dc1639b27851ec9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c9f920fc07078b9a1e0ae471b76d758717ece2429a04f85e8e6d79275c2a`  
		Last Modified: Fri, 31 Jan 2025 06:07:29 GMT  
		Size: 87.3 MB (87317317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-python3` - unknown; unknown

```console
$ docker pull spark@sha256:6ac2cc9df80a940059df674017b44946a2093eb9d91527d3f362cb57e9c32dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9091944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3d7eefeb7d586ced21ace0a174e158fe8b6569f91ee85b4cc552833aea5ba`

```dockerfile
```

-	Layers:
	-	`sha256:b634c3c799883509bce1b89c75c2ead96d659b0dfaf13e9b735c718e00c54000`  
		Last Modified: Fri, 31 Jan 2025 06:07:26 GMT  
		Size: 9.1 MB (9080265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6cacc0203203bb5e2b0dc5b58eea283236dd387f6380115979003d44d231d`  
		Last Modified: Fri, 31 Jan 2025 06:07:25 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-r`

```console
$ docker pull spark@sha256:711e655338d4505d0020cce26e08e784c0f6d3d80230094c7d80ad2f1f807261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-r` - linux; amd64

```console
$ docker pull spark@sha256:7e103effb7ea0ab23fe748ffa3e236e2a49169a08e675f3ee0044ecd6bfd251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672801837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d28dd4d61661ea383398aa9d7a9fad0212bd576e8e525fa83b997fa08bae2f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0931c9e72f8c3f7940d5aa8a47dd3c9101ec0d7760f0461a14839a0769b2d8`  
		Last Modified: Fri, 31 Jan 2025 03:13:06 GMT  
		Size: 232.3 MB (232282129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-r` - unknown; unknown

```console
$ docker pull spark@sha256:e32a05356942029fc314bf649323a540d5c79a0ab5d0bf5b1dfe92edfbd84c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11257873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f69539d718fa7468a9c166c88c09b10404c0d4aed665db08fb7fa33c7127218`

```dockerfile
```

-	Layers:
	-	`sha256:5cdac46d202e4f40c143e4f3bf4457902eb39788d7759275f9d9d5419a936162`  
		Last Modified: Fri, 31 Jan 2025 03:13:01 GMT  
		Size: 11.2 MB (11246921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b22ee0b9c13541f0651c1e3a507321f5150e4dc877a778509bbab533b1c4e2`  
		Last Modified: Fri, 31 Jan 2025 03:13:00 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e99af981e7162a1109c399fa0537359b501bba123ca3e9de9393965c2cdd12fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650426491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8fb3954d3200df24ee66b0120a4839a3a17993e26c049bdb4fe0944934eec4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be0505553c3c7b0e1b999754845da0a0d6fb4616156e098e53425008f0cf369`  
		Last Modified: Fri, 31 Jan 2025 06:09:14 GMT  
		Size: 213.5 MB (213503612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-r` - unknown; unknown

```console
$ docker pull spark@sha256:0b6e02423cfde442a732c3dd76193dc5d3195dcf7de531f01af9e706886a71e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11244006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feffeaeb96bc21ca9879d28e3ca6e42aa10a8c5a363c7d50b5b81142978de673`

```dockerfile
```

-	Layers:
	-	`sha256:cf869baee8c2b16fc27b9467e1dde7ad12c8d3a94fafedd906d3feda7a11db1c`  
		Last Modified: Fri, 31 Jan 2025 06:09:10 GMT  
		Size: 11.2 MB (11232962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab248c4f2b15ec3a2e52acc30ee1424f2b525bdd88fb32cb58b33df1db4f4d7`  
		Last Modified: Fri, 31 Jan 2025 06:09:09 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala`

```console
$ docker pull spark@sha256:d2c03185a189d96bf4425f636604f4a31016c64e155d96f9f4222545d262ddbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala` - linux; amd64

```console
$ docker pull spark@sha256:4e9ff2eb29b80929345417fd19f89ddf103c2d71572d007c6a63bd4f360d2824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440519708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189cc83771793b7a8da07f6a61c4773fef494a8dacce818c2bfa2180b5c1ca30`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala` - unknown; unknown

```console
$ docker pull spark@sha256:019b44e11a351add66d984ad7c99d2f9cdd0ed7f00b35918e8ed55bb461c164f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944c6a0287ca22e1868c4ce3c776617bd4d307bb225f96d95b07a26143e846e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2754cb3b5f97101cdbbbd6f53ebb42c650037ff3b69e040abd64de7a78db11`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 4.4 MB (4350295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713161fd8d106a444f41e50fa79658de15c26684958d58407b81262ef8f9645f`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:00fbb5aa059226b5ce13a8fb908611522ca762877d27d8e51c6b8a71692f1941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436922879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93208192d1ee1ecd53fbdfb430f3610a448b2580c26cfee0bd3e2801e087954`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f4736964a74326185067144f205071de11a2be31ea9c553c22fd1d1394d85e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f11782d877094b9fb430dfc0725714f47e5d56136bcc064a835100131df25e`

```dockerfile
```

-	Layers:
	-	`sha256:9c1941de307e486fe65d9b7fb916b9619c08e7cbfdfc8308ac459aff33f73a75`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 4.4 MB (4352475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120fb5f184566419d9e9386d1ad72d83f9419f04a344ceaabb6d1f16b5a9eb23`  
		Last Modified: Fri, 31 Jan 2025 04:17:54 GMT  
		Size: 23.3 KB (23270 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:e2b830a3fb051cb4c7157dd8e23f6138acc72981d6f566af9cb53505a4922984
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0883ec65e57bc5af6108c25c3ac36f5686f927e24c986e444feb2561f1da3a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 MB (694428914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958af6805265712ac6948fc34a0873a7b84baff73540444119940fe0fe0b1d05`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54e21b3638efc383cbce95487e05aa1f481a5dd5837eca08ed1fe74fe3aea5e`  
		Last Modified: Fri, 31 Jan 2025 03:13:32 GMT  
		Size: 253.9 MB (253909206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e7f350bbe94f09c5f4862278663e24c147d5390349c000773aa2700f71577954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12381422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0214a5f447d19ca20dba60173eb187411ce1eeba4bd5aafccd9cf008f9441a30`

```dockerfile
```

-	Layers:
	-	`sha256:2d3c8af147c04b47ac1817cc22cc6ca274dd6154f6960ec706535097bc5fadbb`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 12.4 MB (12370878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517970c00b9ecdba6871d4b338df2714f99d4b4995d30e0d62348e23f8318c2b`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d2810ac190c1affbbf1f522d656c487e105392997f55ebe3d5342e41bda716bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.1 MB (672067131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65229b1b452047e89046233ec6527d27478e02acb85488c22bbd07fc1acc3a7`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c817a7e14335253c0db718f4ddb216e7ae5cfe666d5b70db89904b5fc95a49`  
		Last Modified: Fri, 31 Jan 2025 05:54:03 GMT  
		Size: 235.1 MB (235144252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:dbb0712ba9e2b43634c387b4d3f550090ae5d6d4e765b5bada1bd82c7cdfdbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12367574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9970549925d8637fca175e26db0802252b0b98fe60db0b442785d180cbd642a3`

```dockerfile
```

-	Layers:
	-	`sha256:974944df6c77a848c35e4b7e116d409f6052cc544ec4009a56263386b7f5837c`  
		Last Modified: Fri, 31 Jan 2025 05:53:58 GMT  
		Size: 12.4 MB (12356962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a5f9ada831c098bb2a4cbb48d62903b7ae1bb1c0d9b2d2133128c0f16723d91`  
		Last Modified: Fri, 31 Jan 2025 05:53:57 GMT  
		Size: 10.6 KB (10612 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:9c89501658cf8051f26a7156108245a1c128a8447d5b88e195f63e57f3ef7b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:886a198dbcc19ed8debb05d53adb42ce8482d896bf72f2ddeec5597afbebb2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.9 MB (534893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908cada5243a3cbaaed9663871209f94f4a1494d8295575de158cd1735096de`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65562d4e36cf032078e3e7a22b283a882606acaebcbb6da874525f52cd4d9a07`  
		Last Modified: Fri, 31 Jan 2025 03:12:34 GMT  
		Size: 94.4 MB (94374134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6bf91d20f8e5cadd06a266208e4fe9993a03a22fafaf67876675ef7e40a918b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9086133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f84642d1cfed441b76b10552b1211c8f89c5d4ff4aaab2529563c8606eba9`

```dockerfile
```

-	Layers:
	-	`sha256:31ec2dbde6aacada546abe304fd328616f596cb04eb6d603276954d7baed0011`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 9.1 MB (9074570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e914d424e086fc494cc4b1a20826c9ce52b661c50e94baf44a265bb332c039`  
		Last Modified: Fri, 31 Jan 2025 03:12:32 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49cadd84c9108c41d656748a6ceeb837be2694da7fbc803a0bb25e0c7f2f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524240196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e4d315310353f4daad37b33f1b44faa3eaa3ccdd5973cd9dc1639b27851ec9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c9f920fc07078b9a1e0ae471b76d758717ece2429a04f85e8e6d79275c2a`  
		Last Modified: Fri, 31 Jan 2025 06:07:29 GMT  
		Size: 87.3 MB (87317317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6ac2cc9df80a940059df674017b44946a2093eb9d91527d3f362cb57e9c32dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9091944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3d7eefeb7d586ced21ace0a174e158fe8b6569f91ee85b4cc552833aea5ba`

```dockerfile
```

-	Layers:
	-	`sha256:b634c3c799883509bce1b89c75c2ead96d659b0dfaf13e9b735c718e00c54000`  
		Last Modified: Fri, 31 Jan 2025 06:07:26 GMT  
		Size: 9.1 MB (9080265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6cacc0203203bb5e2b0dc5b58eea283236dd387f6380115979003d44d231d`  
		Last Modified: Fri, 31 Jan 2025 06:07:25 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:711e655338d4505d0020cce26e08e784c0f6d3d80230094c7d80ad2f1f807261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:7e103effb7ea0ab23fe748ffa3e236e2a49169a08e675f3ee0044ecd6bfd251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672801837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d28dd4d61661ea383398aa9d7a9fad0212bd576e8e525fa83b997fa08bae2f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0931c9e72f8c3f7940d5aa8a47dd3c9101ec0d7760f0461a14839a0769b2d8`  
		Last Modified: Fri, 31 Jan 2025 03:13:06 GMT  
		Size: 232.3 MB (232282129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e32a05356942029fc314bf649323a540d5c79a0ab5d0bf5b1dfe92edfbd84c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11257873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f69539d718fa7468a9c166c88c09b10404c0d4aed665db08fb7fa33c7127218`

```dockerfile
```

-	Layers:
	-	`sha256:5cdac46d202e4f40c143e4f3bf4457902eb39788d7759275f9d9d5419a936162`  
		Last Modified: Fri, 31 Jan 2025 03:13:01 GMT  
		Size: 11.2 MB (11246921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b22ee0b9c13541f0651c1e3a507321f5150e4dc877a778509bbab533b1c4e2`  
		Last Modified: Fri, 31 Jan 2025 03:13:00 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e99af981e7162a1109c399fa0537359b501bba123ca3e9de9393965c2cdd12fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650426491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8fb3954d3200df24ee66b0120a4839a3a17993e26c049bdb4fe0944934eec4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be0505553c3c7b0e1b999754845da0a0d6fb4616156e098e53425008f0cf369`  
		Last Modified: Fri, 31 Jan 2025 06:09:14 GMT  
		Size: 213.5 MB (213503612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0b6e02423cfde442a732c3dd76193dc5d3195dcf7de531f01af9e706886a71e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11244006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feffeaeb96bc21ca9879d28e3ca6e42aa10a8c5a363c7d50b5b81142978de673`

```dockerfile
```

-	Layers:
	-	`sha256:cf869baee8c2b16fc27b9467e1dde7ad12c8d3a94fafedd906d3feda7a11db1c`  
		Last Modified: Fri, 31 Jan 2025 06:09:10 GMT  
		Size: 11.2 MB (11232962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab248c4f2b15ec3a2e52acc30ee1424f2b525bdd88fb32cb58b33df1db4f4d7`  
		Last Modified: Fri, 31 Jan 2025 06:09:09 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:d2c03185a189d96bf4425f636604f4a31016c64e155d96f9f4222545d262ddbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:4e9ff2eb29b80929345417fd19f89ddf103c2d71572d007c6a63bd4f360d2824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440519708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189cc83771793b7a8da07f6a61c4773fef494a8dacce818c2bfa2180b5c1ca30`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:019b44e11a351add66d984ad7c99d2f9cdd0ed7f00b35918e8ed55bb461c164f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944c6a0287ca22e1868c4ce3c776617bd4d307bb225f96d95b07a26143e846e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2754cb3b5f97101cdbbbd6f53ebb42c650037ff3b69e040abd64de7a78db11`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 4.4 MB (4350295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713161fd8d106a444f41e50fa79658de15c26684958d58407b81262ef8f9645f`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:00fbb5aa059226b5ce13a8fb908611522ca762877d27d8e51c6b8a71692f1941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436922879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93208192d1ee1ecd53fbdfb430f3610a448b2580c26cfee0bd3e2801e087954`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f4736964a74326185067144f205071de11a2be31ea9c553c22fd1d1394d85e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f11782d877094b9fb430dfc0725714f47e5d56136bcc064a835100131df25e`

```dockerfile
```

-	Layers:
	-	`sha256:9c1941de307e486fe65d9b7fb916b9619c08e7cbfdfc8308ac459aff33f73a75`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 4.4 MB (4352475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120fb5f184566419d9e9386d1ad72d83f9419f04a344ceaabb6d1f16b5a9eb23`  
		Last Modified: Fri, 31 Jan 2025 04:17:54 GMT  
		Size: 23.3 KB (23270 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:ec7ca1925a4b0d8db6b00450f88ad21ebcb31beed1c241919e8be4a4259c0df0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6c837566ac4cc497b769bf8b99f2b05505b11ae217439dcf3e45f2a31e61b524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 MB (875668456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114ce1a8282d841b0062e64b393fefe995fba47546fa329ca3ea4c9c7f768478`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b87d5cbc852078a10585dcee6072444e920f290b9f66215e6df981d8220d13`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 334.0 MB (333993569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e9d4843f75d7bb83d7703461df6327c7a71e176e7df1ccc1737c72c0b33dfe46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19015284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08924a650a1ea0515c918915c5fb2411b0ad0f08c57633da7a3b6bc87677727c`

```dockerfile
```

-	Layers:
	-	`sha256:d9e206f90f5cc6a914470bdefc61874f76c8143eea0c249883abffe024519d2e`  
		Last Modified: Fri, 31 Jan 2025 03:13:18 GMT  
		Size: 19.0 MB (19004738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acc6d4623e08b37a5302ab43e226f0016b60c6e5b392d171f66be05bfbc7af0`  
		Last Modified: Fri, 31 Jan 2025 03:13:17 GMT  
		Size: 10.5 KB (10546 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:360db66d8dfd69d6aff32ad990feb8a6cb12e84e0aaee0795967daea8a2f5123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.5 MB (856460489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556832cd3e25fecb998d8060bd37873344e9982823692550edfecf6c12f572ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51755573c1cf2889798ba8a4208462f6658c2174460f855a60f884bd4e10e676`  
		Last Modified: Fri, 31 Jan 2025 05:49:17 GMT  
		Size: 317.0 MB (317020031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:04241e4a51287139e7b058cf63a504564aa59f7139c5b1793f98ce545128a6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18982662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c56a324fc552327977fc4b66265461933d722e4c4e192b62f114cb2331fff27`

```dockerfile
```

-	Layers:
	-	`sha256:8a402893cb6558c361459447d007e0577ec2c0db6a1fb380aa0496fb4156e8ab`  
		Last Modified: Fri, 31 Jan 2025 05:49:09 GMT  
		Size: 19.0 MB (18972048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56b7886702ae088664c33178a92394243e8562705023dc41e9bc8f861a8f690`  
		Last Modified: Fri, 31 Jan 2025 05:49:08 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:f536843be0fef2545bb8db1ce210ccfd6966eff87c9f519922f21cca1cfc4a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:383b3411722669803b7d54d31c368db921fd6ac00a172347bad13838df864f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655400658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080370b103d53102913defc47db299cf8c84a0dcdfc1114e258d5338009c575b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa771bc14209e0ddd4129308701f44b374c3905bb86c3c95e805637191c179`  
		Last Modified: Fri, 31 Jan 2025 03:12:47 GMT  
		Size: 113.7 MB (113725771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6c7d2f3194ed18184e25862d81ddff116f3fe15c205b4303d05dfd75a69fc856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9960679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce619a89f730e1709f79d1f25800907be8ee57992cf57673189c475cd4e2021`

```dockerfile
```

-	Layers:
	-	`sha256:f498d72f3532c8330f46721d5375ac45e80b30ebeff414c30f3aeeda997d142c`  
		Last Modified: Fri, 31 Jan 2025 03:12:46 GMT  
		Size: 9.9 MB (9949367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680087c13487029bd68cbc70beb360f462e2167dac1ec9c721f99c881ff12ecf`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0035a0f37dacf7ad863461eba7b6108420164ef095141df232ecc4bec9dec823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.7 MB (647722618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf011250ad3089b06baae753527141ab7d762629d7529560da2242024663be6b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce5be925d803291ff779168f5a37bf8decd84fab19dd5de2a221bdaa1b1cb6`  
		Last Modified: Fri, 31 Jan 2025 06:29:56 GMT  
		Size: 108.3 MB (108282160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:73c314022843f8a8ffedb5bb0caf95f0b91554c00c30be8caa64032772ae30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9957117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205ae0a5b5162ee14246fca50ee83b08cc7c899d4864a800a0b4e03c5fe29ad7`

```dockerfile
```

-	Layers:
	-	`sha256:25a13257f4dc2380e2dbf2e58417ec2dda7ad6fd631466385c12af1c7a200aa3`  
		Last Modified: Fri, 31 Jan 2025 06:29:55 GMT  
		Size: 9.9 MB (9945701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76f02694597ce6d986a2d3bdc174ab3e3dc7e3204b2a0963f2990ebe19e82d8`  
		Last Modified: Fri, 31 Jan 2025 06:29:53 GMT  
		Size: 11.4 KB (11416 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:4f694db01bb17cc09b6238c64ccff5b01e87d9fa562b208f8ebc97d809ed0f14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:515d835b12967a7fa353d58d5f31a0c2973741e254dee33bd82795543a732659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.0 MB (860977435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e12c97462625a858891d26aa149f73ae883ac97c627dc708d2f239d59a20c2e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef74374a613c754d3509247356545e60a97765aeaac8b814d2f47bdcf35f673`  
		Last Modified: Fri, 31 Jan 2025 03:13:31 GMT  
		Size: 319.3 MB (319302548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e88f04979f612362f60a782b84cbfed68e4562dfaabf0c972f172b652092ece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18002912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57b3d821ed92a82f88f8a370b59269063a9b111693d1cd2faf6d4cb4dfdf`

```dockerfile
```

-	Layers:
	-	`sha256:bc6c85b9f6311d653926ae4a83df1b883773b4b3b58dadbb06806686aee1e2ae`  
		Last Modified: Fri, 31 Jan 2025 03:13:27 GMT  
		Size: 18.0 MB (17992230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf2ea6bac999d3dbc1b5055110e543234a77ecb05c2d801a10da2c9a24a5cf6`  
		Last Modified: Fri, 31 Jan 2025 03:13:27 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:710f0918b36cbb6ced2fa2ee2113ea9798fbe43bd3ff19045d4ba9b5c9e4c537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.9 MB (841941529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ca21e7af981b7d07af4d3ac25be67601a156995039c3288b734774c0321545`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2251e69c651925e20d7d3660ebd8741eb1f8f056f0344b5f427170ed91b936`  
		Last Modified: Fri, 31 Jan 2025 06:06:11 GMT  
		Size: 302.5 MB (302501071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:bee74b7fd320a06c59897796d9ee11520c0f5e909914890ba5fc21ef2b799cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17970290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd57d3bfe9c473a135005faf0b28244f613b23821ada0b200866ed26278d1e1`

```dockerfile
```

-	Layers:
	-	`sha256:f789c1604512e67468300537383713f684eb2255a3bd645e707000bfd41766da`  
		Last Modified: Fri, 31 Jan 2025 06:06:05 GMT  
		Size: 18.0 MB (17959528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b5224c5657f8ceffc3491b12553f6d9ad6d2493d25f52e1e1ed61cbe47ef87`  
		Last Modified: Fri, 31 Jan 2025 06:06:04 GMT  
		Size: 10.8 KB (10762 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.4-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:aa55470bc90149c3455593a7be515872893dad4db17f7da5e00b44e003d324eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.4-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:a33e68a39aa35b6fe01f134f9aa130e1dd51c9a06b3b4f52527db670008510fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.7 MB (541674887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6e96d8a284679b2ae06849d5442ffa0031126b0c15c388cdffb3729dcf7cd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5ea3453a4eee92c0b3d7602664a70ad98e455df5b3807bc58159f5e9a34b3374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e8d50adc2b2eeb9a86f367e7e3e2a2f2b31f2aa6c1049b2d5d0efe360d7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:13c980d78b8e0bece816d09f471e7f8af37c440691d4085882249563874313e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 4.6 MB (4582213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec481b4372dcd17f6e40bee42d99229b38dcc9c448a1df1bafc5f00bf2d4811`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 22.9 KB (22866 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.4-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1f9030dc5f9a1077b6442105b5a4717d3d3bb1165e6bce6ef72c8f2ae7706d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539440458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd60fc0780bc9191b17c7ecc4609ab4f9908ef98fe2ccf98056339bc76efe0`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.4-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9ef0798d7ef50c4f62bca963389a2caf9a2127a6ea39e96db02ff082bd4d5b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4702564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b548cb3c8b09794ebc9a15d17e3cc1d47097e23efb9af26e56c0035eb44b4042`

```dockerfile
```

-	Layers:
	-	`sha256:e5932b522efc822741671bbd24a0a11d4c0c608ff7ceaec23e0d473d8a0a3e98`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 4.7 MB (4679588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86dc5e2d1e08bf62753fce1c877fd94c076d8cf13da1be541a4250f261892ce`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 23.0 KB (22976 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2`

```console
$ docker pull spark@sha256:73d083cc6908131fc29b3d362b1ef14631419b91fbea4aee82da29253ad71be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2` - linux; amd64

```console
$ docker pull spark@sha256:6fb9140123f8938807035510598061d438f7100b68961fc89942aa22622e3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.5 MB (774531108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3775cb316ab2e6e825b5c0015364722575082d4c1f402a1bd059e0997d66e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0201827a071859012c3648deae8b4dbd11d4fb8e745349c51c32463a501ca1`  
		Last Modified: Fri, 31 Jan 2025 03:12:42 GMT  
		Size: 113.7 MB (113725939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:ea06d51cc88663a56f0dee91c25759eed8ff97e6fc181eea8ca1ab08e3bcae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10102275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba780891b445e12b34d8dd793a19059ef1c85a473a7c21ee4f8f36da83bd4c7`

```dockerfile
```

-	Layers:
	-	`sha256:f8da92c89dd28bf6f288d796b268a12cc31d9be09038a0dca0ea10aa9c2a783e`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 10.1 MB (10091176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742202c808479132c23d8b41d54b8ff325a7d9a7a3386b5efc598cdaeafc0fb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4aeb18d84684b2bf5cf2ee9aa07b09b9aee83b0d742e70d2cfa4299ef021e5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.9 MB (766853090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d6ff7c96cdead87bff0dab7588c4952f52172cd59b3c7359bf02a8e5585387`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a671e07db9e3446969cda82be99425cb5de174a8fa7b6db528f4489f4d1236`  
		Last Modified: Fri, 31 Jan 2025 06:01:25 GMT  
		Size: 108.3 MB (108282377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:215979ff616475580d304a55dae45499fc3dc9585c0a701b608aeb8ff10e85f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10098691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b85271052a6440fdf172c169555cb8d4be138fe5f178801435b4ec9f95d8e`

```dockerfile
```

-	Layers:
	-	`sha256:54c9f6a0d23dbd8d94391698716e020cc928812aa172c6c3a3fc7be95d8e8851`  
		Last Modified: Fri, 31 Jan 2025 06:01:23 GMT  
		Size: 10.1 MB (10087498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c741764cfa2be1b51bd312a659e3276be740f6db8b74d0ab7c532501529983b7`  
		Last Modified: Fri, 31 Jan 2025 06:01:21 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21`

```console
$ docker pull spark@sha256:7e26c70dd25e2d456f5cfb2e56e1ac4f0cd721a10ad68a5580ad0cbe74953561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21` - linux; amd64

```console
$ docker pull spark@sha256:3279443088e8ac2de4a1fcdaab60830e542c9f279cab097a79a15dbef398a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.5 MB (787546092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b5de806e65904fa32f64535aa0d708ca84457bdeb9a5879caa738b2113523`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51740300a4e69293a67f110761bed098584900c28f26e7df782dffe9bb32907d`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 113.7 MB (113725665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:94da715f5db44ee208c84ad7711b5613b6b9a03e96e613a902393d934b2f4730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10105434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a72254b93d46689815c676f7f9c471e52f2046c9e4def5a16db2b9729bb2a4`

```dockerfile
```

-	Layers:
	-	`sha256:d7f41a55ff616cb053f8c187ec6971a3818c818c886ccdd5421916f973566280`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 10.1 MB (10094306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bcf1000c066d20d94a5619e4a77f2b0b5da8753007b85d317809b8a56b416e`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 11.1 KB (11128 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ecc77940fdb0b8599a727129bf3a7cec879ff60e14a9c3277bed990ba12d3bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.3 MB (779259202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edf05d12a041929997daaee4c4bcac972a08cad74a9d206bdb832bd75c489cf`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576928512179f3bfc8f6cb34680a8dff4c9a7c73f37d532f24e2a13c8fd47fe7`  
		Last Modified: Fri, 31 Jan 2025 05:57:33 GMT  
		Size: 108.3 MB (108282178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:15527f9ad5577312924ba36fb347cb6fc2fcc668b2be04350b2b9715d562a26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10101848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178abb47dad607688c3e34505bca3c0b94dd7bd21ea7ffba5511932a7c5bd5f5`

```dockerfile
```

-	Layers:
	-	`sha256:fd0155c1873624b45ca41e6bd33d076aa351546b6bb57570277331dbc8b567a7`  
		Last Modified: Fri, 31 Jan 2025 05:57:30 GMT  
		Size: 10.1 MB (10090628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b30996772ebd45c7f38bc0cffa8cd1d58257ff933f7deb34d4b36ba4a1a256`  
		Last Modified: Fri, 31 Jan 2025 05:57:29 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-python3`

```console
$ docker pull spark@sha256:7e26c70dd25e2d456f5cfb2e56e1ac4f0cd721a10ad68a5580ad0cbe74953561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-python3` - linux; amd64

```console
$ docker pull spark@sha256:3279443088e8ac2de4a1fcdaab60830e542c9f279cab097a79a15dbef398a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.5 MB (787546092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b5de806e65904fa32f64535aa0d708ca84457bdeb9a5879caa738b2113523`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51740300a4e69293a67f110761bed098584900c28f26e7df782dffe9bb32907d`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 113.7 MB (113725665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:94da715f5db44ee208c84ad7711b5613b6b9a03e96e613a902393d934b2f4730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10105434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a72254b93d46689815c676f7f9c471e52f2046c9e4def5a16db2b9729bb2a4`

```dockerfile
```

-	Layers:
	-	`sha256:d7f41a55ff616cb053f8c187ec6971a3818c818c886ccdd5421916f973566280`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 10.1 MB (10094306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bcf1000c066d20d94a5619e4a77f2b0b5da8753007b85d317809b8a56b416e`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 11.1 KB (11128 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ecc77940fdb0b8599a727129bf3a7cec879ff60e14a9c3277bed990ba12d3bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.3 MB (779259202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edf05d12a041929997daaee4c4bcac972a08cad74a9d206bdb832bd75c489cf`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576928512179f3bfc8f6cb34680a8dff4c9a7c73f37d532f24e2a13c8fd47fe7`  
		Last Modified: Fri, 31 Jan 2025 05:57:33 GMT  
		Size: 108.3 MB (108282178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:15527f9ad5577312924ba36fb347cb6fc2fcc668b2be04350b2b9715d562a26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10101848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178abb47dad607688c3e34505bca3c0b94dd7bd21ea7ffba5511932a7c5bd5f5`

```dockerfile
```

-	Layers:
	-	`sha256:fd0155c1873624b45ca41e6bd33d076aa351546b6bb57570277331dbc8b567a7`  
		Last Modified: Fri, 31 Jan 2025 05:57:30 GMT  
		Size: 10.1 MB (10090628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b30996772ebd45c7f38bc0cffa8cd1d58257ff933f7deb34d4b36ba4a1a256`  
		Last Modified: Fri, 31 Jan 2025 05:57:29 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-r`

```console
$ docker pull spark@sha256:dcd84a3389da7a1b60bb4d065745a30cfd3a8920795fef942a610ba3a6e75139
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-r` - linux; amd64

```console
$ docker pull spark@sha256:671e8dac3136136002a7aa60cb2a74e87c5264d04ba2719c6cbdf2d6a98f4170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.1 MB (993122257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a994bb6a36892a9418af5da2b166881c2c1f042cae3e5bc06525c16bbd28f39`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3152321ec231dde2fbfdc408ed7fd52592577b1e428682c518f44010db2ae8`  
		Last Modified: Fri, 31 Jan 2025 03:13:35 GMT  
		Size: 319.3 MB (319301830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:41adc53819c0c4000f1f981d424235386176e5331138684f4a5e0b4d517717c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18148255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65b525af75b95c443df0786e631b7b61d73de31c2ef2618fc8e852e457d7b04`

```dockerfile
```

-	Layers:
	-	`sha256:e4e1d9d3d2f44cefb38a9ad9963a4edaa2b4663795e6115f282c27981fed3eae`  
		Last Modified: Fri, 31 Jan 2025 03:13:30 GMT  
		Size: 18.1 MB (18137463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922495f3be6c0fc79e1770d91899c5e3357d5ba809345c2bdad175a94406fdc2`  
		Last Modified: Fri, 31 Jan 2025 03:13:30 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a1f1fb3cc7f6d7fed8638a0f184fb898bb11748d65b032663d96c0112b78894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.5 MB (973477655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1cdb6eab53286ba083b89151b8f0608461de9e268a027ae099d4127e35d5ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629bf29bcb08a1568f9aeb52d6ab8e159d75a48e8b04652c2b03f8f6db278e8`  
		Last Modified: Fri, 31 Jan 2025 05:59:53 GMT  
		Size: 302.5 MB (302500631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:364beded3600bb986419ac17c214cabc724b50d9cda099dda7f50d909e7bb89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18115633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935b6799052fc363dbeb60c1221c9aed622fbe5df3fc1a27f34a38913c1d36d7`

```dockerfile
```

-	Layers:
	-	`sha256:67d8ec32a87b231ef6bf8d2c2b790a23602f17c989485c912082b140ca624f69`  
		Last Modified: Fri, 31 Jan 2025 05:59:47 GMT  
		Size: 18.1 MB (18104761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ed68c40cb215a1b65e28ec382415fde719d3710593fca64f3edc75c0d5dc33`  
		Last Modified: Fri, 31 Jan 2025 05:59:46 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-scala`

```console
$ docker pull spark@sha256:1c000f799bc392dd43d0e17edc2fcbeabfc9937834de64302fcc7041a5a7e382
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-scala` - linux; amd64

```console
$ docker pull spark@sha256:3672f141908998d618f948610da3326ac61032251b50c3ac6db3993c52236b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673820427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10b04498b3184815d7300ac710a631ce32ed1344c063921bf71636e63708f14`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:50cda567a7c70fa0e45cbb43ccbff9948b11e6f8fee8bfb1b7c640dc848e44ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4750456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559cf96695e40f976b3d640b892fbaf982ce36c2c863c6a11acfeadcea3c8c2`

```dockerfile
```

-	Layers:
	-	`sha256:bf893f364c94566e79d787d2ea83027312e4399ec9e9bd314776c4978b35a34d`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 4.7 MB (4727446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d7ead9a63f051d79be4c2cb5cf730f6d0cf16436864182ee836838194d799f`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 23.0 KB (23010 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:76dc9359fb4233eb83f3d04509c098b2e463836c0c2469e212529439b9f4e404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.0 MB (670977024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8078c6857b299a32f78b37302f25fb710584b63f68be8a08b3c381be37934236`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f1b8c3a072c9662715773a0707a94400f678e5a9431b7bed0888e1a2b20648d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4847941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06825b087556f5566003b97b0a0084d3c77652d7e624d587f2af06adf7d8f438`

```dockerfile
```

-	Layers:
	-	`sha256:5adea023c11b8e31458ca94e7c3f0a8699130ddb503894bcfe620e7baa9a182f`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 4.8 MB (4824821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180650592ad303cedbe052028d6387cca97349fc3eaa8486a63d85eccf2ceeda`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-python3`

```console
$ docker pull spark@sha256:73d083cc6908131fc29b3d362b1ef14631419b91fbea4aee82da29253ad71be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-python3` - linux; amd64

```console
$ docker pull spark@sha256:6fb9140123f8938807035510598061d438f7100b68961fc89942aa22622e3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.5 MB (774531108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3775cb316ab2e6e825b5c0015364722575082d4c1f402a1bd059e0997d66e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0201827a071859012c3648deae8b4dbd11d4fb8e745349c51c32463a501ca1`  
		Last Modified: Fri, 31 Jan 2025 03:12:42 GMT  
		Size: 113.7 MB (113725939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:ea06d51cc88663a56f0dee91c25759eed8ff97e6fc181eea8ca1ab08e3bcae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10102275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba780891b445e12b34d8dd793a19059ef1c85a473a7c21ee4f8f36da83bd4c7`

```dockerfile
```

-	Layers:
	-	`sha256:f8da92c89dd28bf6f288d796b268a12cc31d9be09038a0dca0ea10aa9c2a783e`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 10.1 MB (10091176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742202c808479132c23d8b41d54b8ff325a7d9a7a3386b5efc598cdaeafc0fb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4aeb18d84684b2bf5cf2ee9aa07b09b9aee83b0d742e70d2cfa4299ef021e5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.9 MB (766853090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d6ff7c96cdead87bff0dab7588c4952f52172cd59b3c7359bf02a8e5585387`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a671e07db9e3446969cda82be99425cb5de174a8fa7b6db528f4489f4d1236`  
		Last Modified: Fri, 31 Jan 2025 06:01:25 GMT  
		Size: 108.3 MB (108282377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:215979ff616475580d304a55dae45499fc3dc9585c0a701b608aeb8ff10e85f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10098691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b85271052a6440fdf172c169555cb8d4be138fe5f178801435b4ec9f95d8e`

```dockerfile
```

-	Layers:
	-	`sha256:54c9f6a0d23dbd8d94391698716e020cc928812aa172c6c3a3fc7be95d8e8851`  
		Last Modified: Fri, 31 Jan 2025 06:01:23 GMT  
		Size: 10.1 MB (10087498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c741764cfa2be1b51bd312a659e3276be740f6db8b74d0ab7c532501529983b7`  
		Last Modified: Fri, 31 Jan 2025 06:01:21 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-r`

```console
$ docker pull spark@sha256:0096802d6d418bd624c75d7875bdb7850073cf139884300c02f3fe6a75c6603f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-r` - linux; amd64

```console
$ docker pull spark@sha256:c39381336448484fd3d4188d32780812bbf168e3f3ea78b30af9c68f43a928c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.1 MB (980107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd51058b7873e516606b58ab322c7741140ed2186ec9d4fa00fec278ad6ab83`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4f9417b43233dc4718c471c3548886a447e15499a0c58c03101d59369e1adb`  
		Last Modified: Fri, 31 Jan 2025 03:13:26 GMT  
		Size: 319.3 MB (319301957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:5b16a74ceb7d5b041afb3fe41b8bbf6e5d8548bcdfde434fa8bc3bc0afa5d980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18145126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190185f995b8bef9634a10e7ee52f3894ed9d276952437b21e6ad619ca417acb`

```dockerfile
```

-	Layers:
	-	`sha256:1ca6aec93ab211e1194bae0f0353e04ed8055b6d58e31a494c01bc790bdfd715`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 18.1 MB (18134347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5348deaf0a465bdba0ae7261dad7735b3c6e86f512e8c11b64d0cdc5af4c835`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9735c38bf235bc9a35abe3c9b2bf8864ee249c0d0ecdb15b6ad7ae126e01dcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961072058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e829dab44cf037c885e26a0bd2a73013a8dfde25a464ed2e78aefdb3431f09`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f704340a1075c1c26eae26eb81a9be2b04c3ef9b0f7944dab5daf59301d99f`  
		Last Modified: Fri, 31 Jan 2025 06:03:46 GMT  
		Size: 302.5 MB (302501345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:db44d53186a85e5f4439f740bb65b0f818c68aeca0f833959e3a7baff24d6a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18112504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a674731ca35781ef5b27edb76a4b86362f8eb83c2e9ff21f60ea5d8952cf0`

```dockerfile
```

-	Layers:
	-	`sha256:981af188964a740670f71a5b56eb9adb9d8d13aea5771a3badce256dd6eafbff`  
		Last Modified: Fri, 31 Jan 2025 06:03:40 GMT  
		Size: 18.1 MB (18101645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d2dc8a6a6716f9f86d2e11c18438c5cef76c93d0930a447d4d9aaeb1b4469c`  
		Last Modified: Fri, 31 Jan 2025 06:03:39 GMT  
		Size: 10.9 KB (10859 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala`

```console
$ docker pull spark@sha256:102073f3e868cd6deeacf0cb1f0b711afe745876c91f6c3720e2ef703adaa1f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala` - linux; amd64

```console
$ docker pull spark@sha256:9cca5d79650b90e07390868cad61f425a2128e77377990d26403ed5ac503b32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.8 MB (660805169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdab3abe970b582b083922ba7857ffbb2c4691f3dc99e523f75fb66fb370f82b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:704ffd1d3b9c4e5db625834cd07765528e6cc621a34f825015e8e730cb583ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4747328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d8166755103f512e250632ba1a140b8bb921ec99841067457e23c7f08e7ee2`

```dockerfile
```

-	Layers:
	-	`sha256:15981321cce19850be2405eb99ba64dedf7948e3e8c0b6d64cf491b030639eda`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 4.7 MB (4724330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71fad860f06ec9ac455eea16d63a62e0fdd7d3b9b5a9447e1ea1674725c00bf`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 23.0 KB (22998 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07cf425f8ff91ed3244175f15cc3b7e16a1a6bab4722fc73e754702f0d9526e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 MB (658570713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b70fdac17ea99113e7db601eec72371ae8f9e9f73aa33a9364d30c38bbd0b12`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:151c244c8ca7b3ef6a7e3627e96dcdb78c6ba76cff540b864d8fd738ad2b447c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4844814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5a3a1df413b1b911d91a5963b4cfa0f41200ccf5fba7176f71cd0d9deda38`

```dockerfile
```

-	Layers:
	-	`sha256:819f16acc6dd920cec221768dbef4af966afc762a16141b379a44ff8eef6d1e8`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 4.8 MB (4821705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925d554be5e32e2ef1aa6625dd6b0e536beae40d612945e2677a12b447bbb808`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:9ba32b25a800d795a25f5d6b81fbd851d90c8f659b2c7882d2bd2febbea8cf67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:045e966edcc9ddf9af8f74fea75eee4d919899f2e07f4997efc7410d472f48e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 MB (994799052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262d4ac41009a2941abb2b66124d8ad9d1ae5fdad835ad606837b0b7844815b1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402b39372b3ef1bebbdce053b2013bf9c9a156fbee720a2eee4764bcdfe47b0f`  
		Last Modified: Fri, 31 Jan 2025 03:13:30 GMT  
		Size: 334.0 MB (333993883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d11d24190d412c877870ef4fdc519b0a241495aea9be01fc0b227a272c78fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19157490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604e49588beebe2ea661ddb55e408e84bce74dd5a1177a0538efc7f13079b66d`

```dockerfile
```

-	Layers:
	-	`sha256:e36dc27d4c763ec3523ec4eeb10a55521462094956e4083f38de0510b9f0d3e0`  
		Last Modified: Fri, 31 Jan 2025 03:13:24 GMT  
		Size: 19.1 MB (19146851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdd6cbb91aa52ef713d4fe110606bd268ea0463f71515d30e8f38e7dc0fa7e8`  
		Last Modified: Fri, 31 Jan 2025 03:13:23 GMT  
		Size: 10.6 KB (10639 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fb94ce2a7ad9f7db3cc5846c17185d9d7a56b185b2e5420077aeee2ba42a8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.6 MB (975589915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68e21d9dba9a2a84a652620c463cae2bb386c6575fd3170fa5e79b045a67ea4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918a8842898e5d2397a81550fe63e4009cfba76b90dc203e6149f98c8b008dca`  
		Last Modified: Fri, 31 Jan 2025 05:46:43 GMT  
		Size: 317.0 MB (317019202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a9e181dcd92e22f388ebde7ecadd46cb35216a874a4c90a84c63d46b3b238ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19124868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639870547c645c17ea67d4b9831f9c24eb2c9724c40c13ec3d5263a841891380`

```dockerfile
```

-	Layers:
	-	`sha256:ad86d2e1503c5e72aee15586277be9b8ce17a8087871395f8875830dfa45ea27`  
		Last Modified: Fri, 31 Jan 2025 05:46:37 GMT  
		Size: 19.1 MB (19114161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f231e1e715a618acebeb0e6640219bd1abcb107a02a15656e05fe46dfd1f0ee`  
		Last Modified: Fri, 31 Jan 2025 05:46:36 GMT  
		Size: 10.7 KB (10707 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:73d083cc6908131fc29b3d362b1ef14631419b91fbea4aee82da29253ad71be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:6fb9140123f8938807035510598061d438f7100b68961fc89942aa22622e3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.5 MB (774531108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3775cb316ab2e6e825b5c0015364722575082d4c1f402a1bd059e0997d66e`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0201827a071859012c3648deae8b4dbd11d4fb8e745349c51c32463a501ca1`  
		Last Modified: Fri, 31 Jan 2025 03:12:42 GMT  
		Size: 113.7 MB (113725939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ea06d51cc88663a56f0dee91c25759eed8ff97e6fc181eea8ca1ab08e3bcae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10102275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba780891b445e12b34d8dd793a19059ef1c85a473a7c21ee4f8f36da83bd4c7`

```dockerfile
```

-	Layers:
	-	`sha256:f8da92c89dd28bf6f288d796b268a12cc31d9be09038a0dca0ea10aa9c2a783e`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 10.1 MB (10091176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742202c808479132c23d8b41d54b8ff325a7d9a7a3386b5efc598cdaeafc0fb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:4aeb18d84684b2bf5cf2ee9aa07b09b9aee83b0d742e70d2cfa4299ef021e5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.9 MB (766853090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d6ff7c96cdead87bff0dab7588c4952f52172cd59b3c7359bf02a8e5585387`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a671e07db9e3446969cda82be99425cb5de174a8fa7b6db528f4489f4d1236`  
		Last Modified: Fri, 31 Jan 2025 06:01:25 GMT  
		Size: 108.3 MB (108282377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:215979ff616475580d304a55dae45499fc3dc9585c0a701b608aeb8ff10e85f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10098691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b85271052a6440fdf172c169555cb8d4be138fe5f178801435b4ec9f95d8e`

```dockerfile
```

-	Layers:
	-	`sha256:54c9f6a0d23dbd8d94391698716e020cc928812aa172c6c3a3fc7be95d8e8851`  
		Last Modified: Fri, 31 Jan 2025 06:01:23 GMT  
		Size: 10.1 MB (10087498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c741764cfa2be1b51bd312a659e3276be740f6db8b74d0ab7c532501529983b7`  
		Last Modified: Fri, 31 Jan 2025 06:01:21 GMT  
		Size: 11.2 KB (11193 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu`

```console
$ docker pull spark@sha256:0096802d6d418bd624c75d7875bdb7850073cf139884300c02f3fe6a75c6603f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:c39381336448484fd3d4188d32780812bbf168e3f3ea78b30af9c68f43a928c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.1 MB (980107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd51058b7873e516606b58ab322c7741140ed2186ec9d4fa00fec278ad6ab83`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4f9417b43233dc4718c471c3548886a447e15499a0c58c03101d59369e1adb`  
		Last Modified: Fri, 31 Jan 2025 03:13:26 GMT  
		Size: 319.3 MB (319301957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5b16a74ceb7d5b041afb3fe41b8bbf6e5d8548bcdfde434fa8bc3bc0afa5d980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18145126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190185f995b8bef9634a10e7ee52f3894ed9d276952437b21e6ad619ca417acb`

```dockerfile
```

-	Layers:
	-	`sha256:1ca6aec93ab211e1194bae0f0353e04ed8055b6d58e31a494c01bc790bdfd715`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 18.1 MB (18134347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5348deaf0a465bdba0ae7261dad7735b3c6e86f512e8c11b64d0cdc5af4c835`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9735c38bf235bc9a35abe3c9b2bf8864ee249c0d0ecdb15b6ad7ae126e01dcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961072058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e829dab44cf037c885e26a0bd2a73013a8dfde25a464ed2e78aefdb3431f09`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f704340a1075c1c26eae26eb81a9be2b04c3ef9b0f7944dab5daf59301d99f`  
		Last Modified: Fri, 31 Jan 2025 06:03:46 GMT  
		Size: 302.5 MB (302501345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:db44d53186a85e5f4439f740bb65b0f818c68aeca0f833959e3a7baff24d6a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18112504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a674731ca35781ef5b27edb76a4b86362f8eb83c2e9ff21f60ea5d8952cf0`

```dockerfile
```

-	Layers:
	-	`sha256:981af188964a740670f71a5b56eb9adb9d8d13aea5771a3badce256dd6eafbff`  
		Last Modified: Fri, 31 Jan 2025 06:03:40 GMT  
		Size: 18.1 MB (18101645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d2dc8a6a6716f9f86d2e11c18438c5cef76c93d0930a447d4d9aaeb1b4469c`  
		Last Modified: Fri, 31 Jan 2025 06:03:39 GMT  
		Size: 10.9 KB (10859 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-ubuntu`

```console
$ docker pull spark@sha256:102073f3e868cd6deeacf0cb1f0b711afe745876c91f6c3720e2ef703adaa1f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:9cca5d79650b90e07390868cad61f425a2128e77377990d26403ed5ac503b32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.8 MB (660805169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdab3abe970b582b083922ba7857ffbb2c4691f3dc99e523f75fb66fb370f82b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceccd43eb730c5072319f6801925b9c42bc757ebf1e3c0fc5ba36073a03a4058`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3466318310fd61c231b0e770dfdb0b25246c9f3a2a54b96899ce85e5caddd`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 22.0 MB (21971128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b4ef10b74805cca0dca0fdda7af4520b6955b15d309b544d79dfeb12dbfe8`  
		Last Modified: Fri, 31 Jan 2025 02:18:01 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a8b97403c05ba9b757497701461a93a8d79c07a1e6fe93af2cc4666ad21d`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:704ffd1d3b9c4e5db625834cd07765528e6cc621a34f825015e8e730cb583ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4747328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d8166755103f512e250632ba1a140b8bb921ec99841067457e23c7f08e7ee2`

```dockerfile
```

-	Layers:
	-	`sha256:15981321cce19850be2405eb99ba64dedf7948e3e8c0b6d64cf491b030639eda`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 4.7 MB (4724330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71fad860f06ec9ac455eea16d63a62e0fdd7d3b9b5a9447e1ea1674725c00bf`  
		Last Modified: Fri, 31 Jan 2025 02:17:48 GMT  
		Size: 23.0 KB (22998 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:07cf425f8ff91ed3244175f15cc3b7e16a1a6bab4722fc73e754702f0d9526e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 MB (658570713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b70fdac17ea99113e7db601eec72371ae8f9e9f73aa33a9364d30c38bbd0b12`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58406ba3916cf817ed0d0f46762fb9e48b6a8350dead79fd685fe1e65f673408`  
		Last Modified: Fri, 31 Jan 2025 04:10:37 GMT  
		Size: 444.0 MB (444032001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9756790d3aee6e34b1acd9b6c2484ba8a6b92b8144f531d7431bc4b7d41c5c`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:151c244c8ca7b3ef6a7e3627e96dcdb78c6ba76cff540b864d8fd738ad2b447c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4844814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5a3a1df413b1b911d91a5963b4cfa0f41200ccf5fba7176f71cd0d9deda38`

```dockerfile
```

-	Layers:
	-	`sha256:819f16acc6dd920cec221768dbef4af966afc762a16141b379a44ff8eef6d1e8`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 4.8 MB (4821705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925d554be5e32e2ef1aa6625dd6b0e536beae40d612945e2677a12b447bbb808`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu`

```console
$ docker pull spark@sha256:a05ce703b765e677692d888846e15f4f8edebc97bcf96ce4b790b62afcaba0e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:cf73adfba6784c80542f4e704f32f4dbca7ccb5225a9c8d19bfca60369959f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007813941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493e8579e3f788bb160c9ef710411e96ac07a1012ea480f8ac997a260db310db`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b573ef79689703c243fcc28d8ce669cde1565cd02ab37dfb0512e15d689e88e9`  
		Last Modified: Fri, 31 Jan 2025 03:13:27 GMT  
		Size: 334.0 MB (333993514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8f0f6d7867615416a82bf5816ffb74a51ab1fb1e03a1814e9f78c6ef61a05efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19160591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9070e859870f778e35515bd11042ea39eb54c13860fe8d351e019c08eabf83b4`

```dockerfile
```

-	Layers:
	-	`sha256:76d43031c3d5d1a7544d361154f087195163690b4ec83f4029487bc2b13bf7f0`  
		Last Modified: Fri, 31 Jan 2025 03:13:23 GMT  
		Size: 19.1 MB (19149953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1386dcc1a0ceed3660357f08804920ea4d8af34bf2aee2ba236c32e183856b03`  
		Last Modified: Fri, 31 Jan 2025 03:13:23 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1a28c1fdb4e045863f79926d82a069358ed534402f015993bfc915adcbf3b4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (987997417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca78d5dd8cdd557ac263684f3f599529b2d8d58a702f8e167e91a201fb4c7c5`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b1b029945530d362dbdd6af3cbd58f99463e87d285f6a8f250e235abd8de8f`  
		Last Modified: Fri, 31 Jan 2025 05:43:55 GMT  
		Size: 317.0 MB (317020393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0b77acf51124f84c7d211e561769c8ac4a2e3892832fe454b7fa51dacc62ae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19127969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b820ffe77538a6ae604aecc5b4e1fc17bb96db0801d9dcdc6fff260fab60fff`

```dockerfile
```

-	Layers:
	-	`sha256:467b6721b65841016886349370ef981439edcbef0f13c933f09a2cca3fa2dcf3`  
		Last Modified: Fri, 31 Jan 2025 05:43:48 GMT  
		Size: 19.1 MB (19117263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e9d8d08c76b0e4ae735ab64bb5c22ff77da550c1dfce538d702d6a60cc5d61`  
		Last Modified: Fri, 31 Jan 2025 05:43:47 GMT  
		Size: 10.7 KB (10706 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu`

```console
$ docker pull spark@sha256:7e26c70dd25e2d456f5cfb2e56e1ac4f0cd721a10ad68a5580ad0cbe74953561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3279443088e8ac2de4a1fcdaab60830e542c9f279cab097a79a15dbef398a28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.5 MB (787546092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b5de806e65904fa32f64535aa0d708ca84457bdeb9a5879caa738b2113523`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51740300a4e69293a67f110761bed098584900c28f26e7df782dffe9bb32907d`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 113.7 MB (113725665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:94da715f5db44ee208c84ad7711b5613b6b9a03e96e613a902393d934b2f4730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10105434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a72254b93d46689815c676f7f9c471e52f2046c9e4def5a16db2b9729bb2a4`

```dockerfile
```

-	Layers:
	-	`sha256:d7f41a55ff616cb053f8c187ec6971a3818c818c886ccdd5421916f973566280`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 10.1 MB (10094306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bcf1000c066d20d94a5619e4a77f2b0b5da8753007b85d317809b8a56b416e`  
		Last Modified: Fri, 31 Jan 2025 03:12:31 GMT  
		Size: 11.1 KB (11128 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ecc77940fdb0b8599a727129bf3a7cec879ff60e14a9c3277bed990ba12d3bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.3 MB (779259202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edf05d12a041929997daaee4c4bcac972a08cad74a9d206bdb832bd75c489cf`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576928512179f3bfc8f6cb34680a8dff4c9a7c73f37d532f24e2a13c8fd47fe7`  
		Last Modified: Fri, 31 Jan 2025 05:57:33 GMT  
		Size: 108.3 MB (108282178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:15527f9ad5577312924ba36fb347cb6fc2fcc668b2be04350b2b9715d562a26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10101848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178abb47dad607688c3e34505bca3c0b94dd7bd21ea7ffba5511932a7c5bd5f5`

```dockerfile
```

-	Layers:
	-	`sha256:fd0155c1873624b45ca41e6bd33d076aa351546b6bb57570277331dbc8b567a7`  
		Last Modified: Fri, 31 Jan 2025 05:57:30 GMT  
		Size: 10.1 MB (10090628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b30996772ebd45c7f38bc0cffa8cd1d58257ff933f7deb34d4b36ba4a1a256`  
		Last Modified: Fri, 31 Jan 2025 05:57:29 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu`

```console
$ docker pull spark@sha256:dcd84a3389da7a1b60bb4d065745a30cfd3a8920795fef942a610ba3a6e75139
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:671e8dac3136136002a7aa60cb2a74e87c5264d04ba2719c6cbdf2d6a98f4170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.1 MB (993122257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a994bb6a36892a9418af5da2b166881c2c1f042cae3e5bc06525c16bbd28f39`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3152321ec231dde2fbfdc408ed7fd52592577b1e428682c518f44010db2ae8`  
		Last Modified: Fri, 31 Jan 2025 03:13:35 GMT  
		Size: 319.3 MB (319301830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:41adc53819c0c4000f1f981d424235386176e5331138684f4a5e0b4d517717c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18148255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65b525af75b95c443df0786e631b7b61d73de31c2ef2618fc8e852e457d7b04`

```dockerfile
```

-	Layers:
	-	`sha256:e4e1d9d3d2f44cefb38a9ad9963a4edaa2b4663795e6115f282c27981fed3eae`  
		Last Modified: Fri, 31 Jan 2025 03:13:30 GMT  
		Size: 18.1 MB (18137463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922495f3be6c0fc79e1770d91899c5e3357d5ba809345c2bdad175a94406fdc2`  
		Last Modified: Fri, 31 Jan 2025 03:13:30 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a1f1fb3cc7f6d7fed8638a0f184fb898bb11748d65b032663d96c0112b78894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.5 MB (973477655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1cdb6eab53286ba083b89151b8f0608461de9e268a027ae099d4127e35d5ed`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
USER root
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV R_HOME=/usr/lib/R
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629bf29bcb08a1568f9aeb52d6ab8e159d75a48e8b04652c2b03f8f6db278e8`  
		Last Modified: Fri, 31 Jan 2025 05:59:53 GMT  
		Size: 302.5 MB (302500631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:364beded3600bb986419ac17c214cabc724b50d9cda099dda7f50d909e7bb89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18115633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935b6799052fc363dbeb60c1221c9aed622fbe5df3fc1a27f34a38913c1d36d7`

```dockerfile
```

-	Layers:
	-	`sha256:67d8ec32a87b231ef6bf8d2c2b790a23602f17c989485c912082b140ca624f69`  
		Last Modified: Fri, 31 Jan 2025 05:59:47 GMT  
		Size: 18.1 MB (18104761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ed68c40cb215a1b65e28ec382415fde719d3710593fca64f3edc75c0d5dc33`  
		Last Modified: Fri, 31 Jan 2025 05:59:46 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-ubuntu`

```console
$ docker pull spark@sha256:1c000f799bc392dd43d0e17edc2fcbeabfc9937834de64302fcc7041a5a7e382
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:3672f141908998d618f948610da3326ac61032251b50c3ac6db3993c52236b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673820427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10b04498b3184815d7300ac710a631ce32ed1344c063921bf71636e63708f14`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2ed84f024d9162c6f2f1d20802e6a3b58c2d37150df54c152579e8ee12846`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3641e4e513bd7c7a4f46fde7a55c32dd57c02f441beb8cdfd730eaed6de4ddb`  
		Last Modified: Fri, 31 Jan 2025 02:17:14 GMT  
		Size: 22.0 MB (21971145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526dd2473efe6ef23616b92f2bea9773e167c8a984186a7220bad7cbe291a11`  
		Last Modified: Fri, 31 Jan 2025 02:17:21 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0a04ccd7a3f9e3f77f0a9e3b67830bf22e97b4a37b85a0d41c064a6ab4572`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:50cda567a7c70fa0e45cbb43ccbff9948b11e6f8fee8bfb1b7c640dc848e44ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4750456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559cf96695e40f976b3d640b892fbaf982ce36c2c863c6a11acfeadcea3c8c2`

```dockerfile
```

-	Layers:
	-	`sha256:bf893f364c94566e79d787d2ea83027312e4399ec9e9bd314776c4978b35a34d`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 4.7 MB (4727446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d7ead9a63f051d79be4c2cb5cf730f6d0cf16436864182ee836838194d799f`  
		Last Modified: Fri, 31 Jan 2025 02:17:13 GMT  
		Size: 23.0 KB (23010 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:76dc9359fb4233eb83f3d04509c098b2e463836c0c2469e212529439b9f4e404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.0 MB (670977024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8078c6857b299a32f78b37302f25fb710584b63f68be8a08b3c381be37934236`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 09:12:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 09:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Oct 2024 09:12:28 GMT
CMD ["jshell"]
# Tue, 08 Oct 2024 09:12:28 GMT
ARG spark_uid=185
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-4.0.0-preview2/spark-4.0.0-preview2-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 08 Oct 2024 09:12:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 08 Oct 2024 09:12:28 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 08 Oct 2024 09:12:28 GMT
WORKDIR /opt/spark/work-dir
# Tue, 08 Oct 2024 09:12:28 GMT
USER spark
# Tue, 08 Oct 2024 09:12:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab58ad8385dbc4983b8b4865156bc2d38d4767f38f95371bcc5b8247fcf73b`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa971839d96c3a6ac285be51568dcb82ee133e0ada6b29b7b7c49e889f1c4b`  
		Last Modified: Fri, 31 Jan 2025 04:08:16 GMT  
		Size: 21.6 MB (21639009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f969d865755e5fdff787d11b7c2ca319217a935f078f41261eeb1e5607c6e4e`  
		Last Modified: Fri, 31 Jan 2025 04:08:24 GMT  
		Size: 444.0 MB (444032014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac6197f13b126e8731fdc97856094e9f7a33e2c73712105541f819fd5ec9ac`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f1b8c3a072c9662715773a0707a94400f678e5a9431b7bed0888e1a2b20648d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4847941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06825b087556f5566003b97b0a0084d3c77652d7e624d587f2af06adf7d8f438`

```dockerfile
```

-	Layers:
	-	`sha256:5adea023c11b8e31458ca94e7c3f0a8699130ddb503894bcfe620e7baa9a182f`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 4.8 MB (4824821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180650592ad303cedbe052028d6387cca97349fc3eaa8486a63d85eccf2ceeda`  
		Last Modified: Fri, 31 Jan 2025 04:08:15 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:9c89501658cf8051f26a7156108245a1c128a8447d5b88e195f63e57f3ef7b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:886a198dbcc19ed8debb05d53adb42ce8482d896bf72f2ddeec5597afbebb2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.9 MB (534893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908cada5243a3cbaaed9663871209f94f4a1494d8295575de158cd1735096de`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65562d4e36cf032078e3e7a22b283a882606acaebcbb6da874525f52cd4d9a07`  
		Last Modified: Fri, 31 Jan 2025 03:12:34 GMT  
		Size: 94.4 MB (94374134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:6bf91d20f8e5cadd06a266208e4fe9993a03a22fafaf67876675ef7e40a918b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9086133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f84642d1cfed441b76b10552b1211c8f89c5d4ff4aaab2529563c8606eba9`

```dockerfile
```

-	Layers:
	-	`sha256:31ec2dbde6aacada546abe304fd328616f596cb04eb6d603276954d7baed0011`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 9.1 MB (9074570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e914d424e086fc494cc4b1a20826c9ce52b661c50e94baf44a265bb332c039`  
		Last Modified: Fri, 31 Jan 2025 03:12:32 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49cadd84c9108c41d656748a6ceeb837be2694da7fbc803a0bb25e0c7f2f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524240196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e4d315310353f4daad37b33f1b44faa3eaa3ccdd5973cd9dc1639b27851ec9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c9f920fc07078b9a1e0ae471b76d758717ece2429a04f85e8e6d79275c2a`  
		Last Modified: Fri, 31 Jan 2025 06:07:29 GMT  
		Size: 87.3 MB (87317317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:6ac2cc9df80a940059df674017b44946a2093eb9d91527d3f362cb57e9c32dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9091944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3d7eefeb7d586ced21ace0a174e158fe8b6569f91ee85b4cc552833aea5ba`

```dockerfile
```

-	Layers:
	-	`sha256:b634c3c799883509bce1b89c75c2ead96d659b0dfaf13e9b735c718e00c54000`  
		Last Modified: Fri, 31 Jan 2025 06:07:26 GMT  
		Size: 9.1 MB (9080265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6cacc0203203bb5e2b0dc5b58eea283236dd387f6380115979003d44d231d`  
		Last Modified: Fri, 31 Jan 2025 06:07:25 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:9c89501658cf8051f26a7156108245a1c128a8447d5b88e195f63e57f3ef7b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:886a198dbcc19ed8debb05d53adb42ce8482d896bf72f2ddeec5597afbebb2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.9 MB (534893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908cada5243a3cbaaed9663871209f94f4a1494d8295575de158cd1735096de`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65562d4e36cf032078e3e7a22b283a882606acaebcbb6da874525f52cd4d9a07`  
		Last Modified: Fri, 31 Jan 2025 03:12:34 GMT  
		Size: 94.4 MB (94374134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:6bf91d20f8e5cadd06a266208e4fe9993a03a22fafaf67876675ef7e40a918b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9086133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f84642d1cfed441b76b10552b1211c8f89c5d4ff4aaab2529563c8606eba9`

```dockerfile
```

-	Layers:
	-	`sha256:31ec2dbde6aacada546abe304fd328616f596cb04eb6d603276954d7baed0011`  
		Last Modified: Fri, 31 Jan 2025 03:12:33 GMT  
		Size: 9.1 MB (9074570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e914d424e086fc494cc4b1a20826c9ce52b661c50e94baf44a265bb332c039`  
		Last Modified: Fri, 31 Jan 2025 03:12:32 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:a49cadd84c9108c41d656748a6ceeb837be2694da7fbc803a0bb25e0c7f2f1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.2 MB (524240196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e4d315310353f4daad37b33f1b44faa3eaa3ccdd5973cd9dc1639b27851ec9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c9f920fc07078b9a1e0ae471b76d758717ece2429a04f85e8e6d79275c2a`  
		Last Modified: Fri, 31 Jan 2025 06:07:29 GMT  
		Size: 87.3 MB (87317317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:6ac2cc9df80a940059df674017b44946a2093eb9d91527d3f362cb57e9c32dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9091944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3d7eefeb7d586ced21ace0a174e158fe8b6569f91ee85b4cc552833aea5ba`

```dockerfile
```

-	Layers:
	-	`sha256:b634c3c799883509bce1b89c75c2ead96d659b0dfaf13e9b735c718e00c54000`  
		Last Modified: Fri, 31 Jan 2025 06:07:26 GMT  
		Size: 9.1 MB (9080265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6cacc0203203bb5e2b0dc5b58eea283236dd387f6380115979003d44d231d`  
		Last Modified: Fri, 31 Jan 2025 06:07:25 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:f536843be0fef2545bb8db1ce210ccfd6966eff87c9f519922f21cca1cfc4a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:383b3411722669803b7d54d31c368db921fd6ac00a172347bad13838df864f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 MB (655400658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080370b103d53102913defc47db299cf8c84a0dcdfc1114e258d5338009c575b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db47551ffe594247e05af64f2ee0b539027fe44a24d9ea787cc0f58f4b866d`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 20.7 MB (20684209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6dd72cd37e5f381509074012fc2651244616a55998f935e391f59ce15cc76`  
		Last Modified: Fri, 31 Jan 2025 01:31:02 GMT  
		Size: 144.6 MB (144576120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637efe71d51a57f727589904303f896f043f3d108834a5d1cd599f616474526c`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bfa9b24efe55d6a3db1aa002339336d93be891e7d25068a4023690e1fafca3`  
		Last Modified: Fri, 31 Jan 2025 01:31:00 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe306e723f55cb501b9a3e54ea08dc1a7c1e8d97d1aab5581f000ef86cdf34e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071f0e8b538237f20fb18d2ffeef6def84d6d7ef6e8fa634f2d99d88e966d6a`  
		Last Modified: Fri, 31 Jan 2025 02:17:16 GMT  
		Size: 22.0 MB (21971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118feff11296952b6ce99f17515c6dfe12e3fc77368cd46bfd257904bb3f725e`  
		Last Modified: Fri, 31 Jan 2025 02:17:20 GMT  
		Size: 324.9 MB (324901719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537f00220366c718934f3baa14df8b3fe66f9e55831e090e2d3650f691997ff8`  
		Last Modified: Fri, 31 Jan 2025 02:17:15 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa771bc14209e0ddd4129308701f44b374c3905bb86c3c95e805637191c179`  
		Last Modified: Fri, 31 Jan 2025 03:12:47 GMT  
		Size: 113.7 MB (113725771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:6c7d2f3194ed18184e25862d81ddff116f3fe15c205b4303d05dfd75a69fc856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9960679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce619a89f730e1709f79d1f25800907be8ee57992cf57673189c475cd4e2021`

```dockerfile
```

-	Layers:
	-	`sha256:f498d72f3532c8330f46721d5375ac45e80b30ebeff414c30f3aeeda997d142c`  
		Last Modified: Fri, 31 Jan 2025 03:12:46 GMT  
		Size: 9.9 MB (9949367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680087c13487029bd68cbc70beb360f462e2167dac1ec9c721f99c881ff12ecf`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 11.3 KB (11312 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:0035a0f37dacf7ad863461eba7b6108420164ef095141df232ecc4bec9dec823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.7 MB (647722618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf011250ad3089b06baae753527141ab7d762629d7529560da2242024663be6b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
CMD ["jshell"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf530b2c0f5a8586f14e57983174a4dcf54795d479698234c1c7983f493d17c7`  
		Last Modified: Fri, 31 Jan 2025 01:40:32 GMT  
		Size: 143.5 MB (143461674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa0aba811e4e48bd7100f67512210d3a72990fc689c7d29c43c74b93966d80e`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80afd8ab821d41d086fed51e507cf1c857fb3f0eae0160e2982d769853f98bb`  
		Last Modified: Fri, 31 Jan 2025 01:40:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc352b8b4dafeac9910f53d661d7dbf97c29abddc5a7679357de16940b6a315f`  
		Last Modified: Fri, 31 Jan 2025 04:10:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6cec811aedb83e76e62c0d7397dc1b12c62ed2ef8344103ad99fb8deb1d143`  
		Last Modified: Fri, 31 Jan 2025 04:10:26 GMT  
		Size: 21.6 MB (21638907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b10976bc2bd6a36235f4e59a6467064e3dee9a6e41bcbaff95f932826fb5d9`  
		Last Modified: Fri, 31 Jan 2025 04:15:57 GMT  
		Size: 324.9 MB (324901746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b9d527a8c312209643eedf1f88c9a4499906144e0366f74c76072474d185f`  
		Last Modified: Fri, 31 Jan 2025 04:15:50 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce5be925d803291ff779168f5a37bf8decd84fab19dd5de2a221bdaa1b1cb6`  
		Last Modified: Fri, 31 Jan 2025 06:29:56 GMT  
		Size: 108.3 MB (108282160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:73c314022843f8a8ffedb5bb0caf95f0b91554c00c30be8caa64032772ae30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9957117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205ae0a5b5162ee14246fca50ee83b08cc7c899d4864a800a0b4e03c5fe29ad7`

```dockerfile
```

-	Layers:
	-	`sha256:25a13257f4dc2380e2dbf2e58417ec2dda7ad6fd631466385c12af1c7a200aa3`  
		Last Modified: Fri, 31 Jan 2025 06:29:55 GMT  
		Size: 9.9 MB (9945701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76f02694597ce6d986a2d3bdc174ab3e3dc7e3204b2a0963f2990ebe19e82d8`  
		Last Modified: Fri, 31 Jan 2025 06:29:53 GMT  
		Size: 11.4 KB (11416 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:711e655338d4505d0020cce26e08e784c0f6d3d80230094c7d80ad2f1f807261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:7e103effb7ea0ab23fe748ffa3e236e2a49169a08e675f3ee0044ecd6bfd251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672801837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d28dd4d61661ea383398aa9d7a9fad0212bd576e8e525fa83b997fa08bae2f`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0931c9e72f8c3f7940d5aa8a47dd3c9101ec0d7760f0461a14839a0769b2d8`  
		Last Modified: Fri, 31 Jan 2025 03:13:06 GMT  
		Size: 232.3 MB (232282129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:e32a05356942029fc314bf649323a540d5c79a0ab5d0bf5b1dfe92edfbd84c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11257873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f69539d718fa7468a9c166c88c09b10404c0d4aed665db08fb7fa33c7127218`

```dockerfile
```

-	Layers:
	-	`sha256:5cdac46d202e4f40c143e4f3bf4457902eb39788d7759275f9d9d5419a936162`  
		Last Modified: Fri, 31 Jan 2025 03:13:01 GMT  
		Size: 11.2 MB (11246921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b22ee0b9c13541f0651c1e3a507321f5150e4dc877a778509bbab533b1c4e2`  
		Last Modified: Fri, 31 Jan 2025 03:13:00 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e99af981e7162a1109c399fa0537359b501bba123ca3e9de9393965c2cdd12fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.4 MB (650426491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8fb3954d3200df24ee66b0120a4839a3a17993e26c049bdb4fe0944934eec4`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
USER root
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV R_HOME=/usr/lib/R
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be0505553c3c7b0e1b999754845da0a0d6fb4616156e098e53425008f0cf369`  
		Last Modified: Fri, 31 Jan 2025 06:09:14 GMT  
		Size: 213.5 MB (213503612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:0b6e02423cfde442a732c3dd76193dc5d3195dcf7de531f01af9e706886a71e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11244006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feffeaeb96bc21ca9879d28e3ca6e42aa10a8c5a363c7d50b5b81142978de673`

```dockerfile
```

-	Layers:
	-	`sha256:cf869baee8c2b16fc27b9467e1dde7ad12c8d3a94fafedd906d3feda7a11db1c`  
		Last Modified: Fri, 31 Jan 2025 06:09:10 GMT  
		Size: 11.2 MB (11232962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab248c4f2b15ec3a2e52acc30ee1424f2b525bdd88fb32cb58b33df1db4f4d7`  
		Last Modified: Fri, 31 Jan 2025 06:09:09 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:d2c03185a189d96bf4425f636604f4a31016c64e155d96f9f4222545d262ddbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:4e9ff2eb29b80929345417fd19f89ddf103c2d71572d007c6a63bd4f360d2824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 MB (440519708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189cc83771793b7a8da07f6a61c4773fef494a8dacce818c2bfa2180b5c1ca30`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058f73b8f4937ab8fb3b4c159a4ec63b748de89e82bb46cb05905502be6f5c3`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 20.3 MB (20251256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937e0a2086c23a09d1f20c16ad505f7c97bcf945194fbbab952915ef7d69f7a`  
		Last Modified: Fri, 31 Jan 2025 01:29:53 GMT  
		Size: 47.2 MB (47216682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3083818c14451f2bc51269701808b2b3c9c7c12b5da3128ac588e4a492151d`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75914dcd1327ce474ab3e8866264f65336bafa9a087b135efcfbe0d94c3b36`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c048a11358b77ca16bde6e96d38bbd9e1486e170a3534fbb33df6c5ab67ad`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 20.6 MB (20632950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209969351800f6c5c23dab2b44088e150d0ad6a76ede9c63cdef58d775e81600`  
		Last Modified: Fri, 31 Jan 2025 02:16:58 GMT  
		Size: 324.9 MB (324901728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcceb42cae2df01e0d3301d77316d657a994c3760ea21edc3984d1174a6136fb`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:019b44e11a351add66d984ad7c99d2f9cdd0ed7f00b35918e8ed55bb461c164f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944c6a0287ca22e1868c4ce3c776617bd4d307bb225f96d95b07a26143e846e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe2754cb3b5f97101cdbbbd6f53ebb42c650037ff3b69e040abd64de7a78db11`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 4.4 MB (4350295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713161fd8d106a444f41e50fa79658de15c26684958d58407b81262ef8f9645f`  
		Last Modified: Fri, 31 Jan 2025 02:16:54 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:00fbb5aa059226b5ce13a8fb908611522ca762877d27d8e51c6b8a71692f1941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436922879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93208192d1ee1ecd53fbdfb430f3610a448b2580c26cfee0bd3e2801e087954`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Dec 2024 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Dec 2024 05:28:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 22 Dec 2024 05:28:31 GMT
ARG spark_uid=185
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz.asc GPG_KEY=19F745C40A0E550420BB2C522541488DA93FE4B4
# Sun, 22 Dec 2024 05:28:31 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
COPY entrypoint.sh /opt/ # buildkit
# Sun, 22 Dec 2024 05:28:31 GMT
ENV SPARK_HOME=/opt/spark
# Sun, 22 Dec 2024 05:28:31 GMT
WORKDIR /opt/spark/work-dir
# Sun, 22 Dec 2024 05:28:31 GMT
USER spark
# Sun, 22 Dec 2024 05:28:31 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5cbd8f8a9d4fd365f05b40f0e9f7243d8fa9880bb6cb42a95d5c08fa77b95`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeae19ca17ba4ac0173b71785622aa2166dd4bdae7eb5d1793775db6fef6169`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 20.4 MB (20369373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7304ff98d3a5d8f86d94febce65d72c38b429df312f9cb3aaeb11609152a97ad`  
		Last Modified: Fri, 31 Jan 2025 04:18:01 GMT  
		Size: 324.9 MB (324901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4bf098b610b8c74e4aaed9ada40bdd8e9b67e295df96bf58c371858a9d074`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:f4736964a74326185067144f205071de11a2be31ea9c553c22fd1d1394d85e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f11782d877094b9fb430dfc0725714f47e5d56136bcc064a835100131df25e`

```dockerfile
```

-	Layers:
	-	`sha256:9c1941de307e486fe65d9b7fb916b9619c08e7cbfdfc8308ac459aff33f73a75`  
		Last Modified: Fri, 31 Jan 2025 04:17:55 GMT  
		Size: 4.4 MB (4352475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120fb5f184566419d9e9386d1ad72d83f9419f04a344ceaabb6d1f16b5a9eb23`  
		Last Modified: Fri, 31 Jan 2025 04:17:54 GMT  
		Size: 23.3 KB (23270 bytes)  
		MIME: application/vnd.in-toto+json
