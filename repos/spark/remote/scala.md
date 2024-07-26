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
