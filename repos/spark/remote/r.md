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
