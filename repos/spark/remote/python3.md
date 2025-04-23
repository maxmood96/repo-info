## `spark:python3`

```console
$ docker pull spark@sha256:055f041d28e09389c5b6d776d48944ed1dd154d136f77f738f6ce17dfa0e266c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:afc406bd2d59aed10dc6a391680cc89854e50b25e587d6a33f207c87567f6324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.8 MB (534805523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7fd0a512e589b07eb14faf85fce03de74d35e52527faceafed795e22cf27ad`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Feb 2025 04:45:43 GMT
ARG RELEASE
# Fri, 28 Feb 2025 04:45:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Feb 2025 04:45:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Feb 2025 04:45:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Feb 2025 04:45:43 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Feb 2025 04:45:43 GMT
CMD ["/bin/bash"]
# Fri, 28 Feb 2025 04:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Feb 2025 04:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2025 04:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 28 Feb 2025 04:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Fri, 28 Feb 2025 04:45:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 28 Feb 2025 04:45:43 GMT
ARG spark_uid=185
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 28 Feb 2025 04:45:43 GMT
WORKDIR /opt/spark/work-dir
# Fri, 28 Feb 2025 04:45:43 GMT
USER spark
# Fri, 28 Feb 2025 04:45:43 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 28 Feb 2025 04:45:43 GMT
USER root
# Fri, 28 Feb 2025 04:45:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
USER spark
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d9fc7fd4671de2143244d173ce3b99e9b376023664c13ab227a00907c7948`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 20.3 MB (20260483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e029366186745d92cec2e8f7b7d20aea0b4028b9914c30a251d5d1cab31a8a`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 47.2 MB (47224320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75792e74185b69d14904e3cf6aee93d670fb601a9a082c1cab49d881d45559ca`  
		Last Modified: Wed, 23 Apr 2025 16:31:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53352117d7a5046c71e9f7af5c219de7acfb4ae2aef847bc6519c338e408e5b5`  
		Last Modified: Wed, 23 Apr 2025 16:31:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3942c200723215f4a4f94b088b1ec651d8235c75309c2e3e16079420bc8f8665`  
		Last Modified: Wed, 23 Apr 2025 17:16:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f7f6eeebca5fc192ee573294964230191728bda6bd8ce3632407c23e55a8c6`  
		Last Modified: Wed, 23 Apr 2025 17:16:04 GMT  
		Size: 20.6 MB (20633430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883e3802ae79d0ea1d8509935e7a03fb675fbca885dbede886c6c49f70bbe3e0`  
		Last Modified: Wed, 23 Apr 2025 17:16:12 GMT  
		Size: 324.8 MB (324795125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37510bb81fdcf940ba72104c0bb70f8d9f0066790c0a920bf591a151f6dc57`  
		Last Modified: Wed, 23 Apr 2025 17:16:03 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e85e217690fb258c74062b3ae9c72278750aee08313bb10aa3776ce73e85754`  
		Last Modified: Wed, 23 Apr 2025 18:11:45 GMT  
		Size: 94.4 MB (94375732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:baabdb386487822229db7d8d8d8eb1229f836ac1aef88bbf157cd31f6e773c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e10fc7e5d1f00de9e05800e3b44f4e1d84767639a1745a05227bfe87855d5`

```dockerfile
```

-	Layers:
	-	`sha256:8bed5e82ea48098cceb6594dd6b9bdad4f16fed122ce6a9204be9991f9f2fe5f`  
		Last Modified: Wed, 23 Apr 2025 18:11:44 GMT  
		Size: 9.1 MB (9077168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4b232ff5d947e0c3edd32e5297c62132e2c84ad5f5369fabcb50a94a92baaf`  
		Last Modified: Wed, 23 Apr 2025 18:11:43 GMT  
		Size: 11.6 KB (11563 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b3b9f61bcbd7b1117d81b6ca4a0998020d671ca5d766e5abbf71abdc9689f692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.1 MB (524133216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f83ee8c8420ef9867454833fd04f8031659c6f4e98582b42617aaf2a9ecab9`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 28 Feb 2025 04:45:43 GMT
ARG spark_uid=185
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.5/spark-3.5.5-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Fri, 28 Feb 2025 04:45:43 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
COPY entrypoint.sh /opt/ # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
ENV SPARK_HOME=/opt/spark
# Fri, 28 Feb 2025 04:45:43 GMT
WORKDIR /opt/spark/work-dir
# Fri, 28 Feb 2025 04:45:43 GMT
USER spark
# Fri, 28 Feb 2025 04:45:43 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Fri, 28 Feb 2025 04:45:43 GMT
USER root
# Fri, 28 Feb 2025 04:45:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Feb 2025 04:45:43 GMT
USER spark
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Wed, 09 Apr 2025 06:57:19 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbef7ef4106cc1e17b0f759b9b3b9ffa91b2dfba84898221d407458316c37f57`  
		Last Modified: Wed, 09 Apr 2025 07:02:12 GMT  
		Size: 45.6 MB (45577470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09887e6904a1677f5c1c950314787913473133366be7215280c0250673c3f070`  
		Last Modified: Wed, 09 Apr 2025 07:02:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e76030eaf5c6647bc2500115119c43a37229f7f6168c954265763d8a7c246f3`  
		Last Modified: Wed, 09 Apr 2025 07:02:11 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b218d7ca9d32c408a2853d11baf5208914743b6c6e5c839fd14dad088a375de`  
		Last Modified: Wed, 09 Apr 2025 16:38:36 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3770f117cefb9facb4087ddfebd0809b0bc5fcf31af9f6b6adf5d8a315daa0a`  
		Last Modified: Wed, 09 Apr 2025 16:38:37 GMT  
		Size: 20.4 MB (20367936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e4033322c07008a0c93bcea3109f79887156e8f8a78d3a1e45b9e89352f801`  
		Last Modified: Wed, 09 Apr 2025 16:38:44 GMT  
		Size: 324.8 MB (324795106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c13d69936698751b4d795355e789c0bf537ac7f0d0ff9eda0c7de85e084edb2`  
		Last Modified: Wed, 09 Apr 2025 16:38:36 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b666dc80acf8674ded6d14df3375c66762020f0120c3f80211e0691248526a78`  
		Last Modified: Wed, 09 Apr 2025 19:56:01 GMT  
		Size: 87.3 MB (87316032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:638de22e14512d7bf8b29b336270b11b2834cabe194f18a89e16ac2d5124dc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9092666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef64ae3939b7f8dc2c9f370bc86868f59fa85777b96c901a037c836e31fcf2`

```dockerfile
```

-	Layers:
	-	`sha256:05bab2e4f0083dfa035969eff427e6c98176d550958503adb502760c8d411993`  
		Last Modified: Wed, 09 Apr 2025 19:55:59 GMT  
		Size: 9.1 MB (9080987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c72eecee8ede52dd21522583d6031670c66156fd81e1ca5419480796c8ca541`  
		Last Modified: Wed, 09 Apr 2025 19:55:59 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json
