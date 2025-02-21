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
