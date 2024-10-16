## `spark:latest`

```console
$ docker pull spark@sha256:49d01f754834ebaf8885f85a393e126c8778b87918fda6391f55c6921ac19f3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:9a3c72ea8a773af1b43951353ea8e51b7391867d40eb88ec57ce9b2f21a46aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535901231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5e366a92e384ce176432bac6d036bb94f64133faa872176a70a0cb40f71dd`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 06:58:10 GMT
ARG RELEASE
# Thu, 10 Oct 2024 06:58:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 06:58:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 06:58:10 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 10 Oct 2024 06:58:10 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 10 Oct 2024 06:58:10 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Oct 2024 06:58:10 GMT
ARG spark_uid=185
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz.asc GPG_KEY=0A2D660358B6F6F8071FD16F6606986CF5A8447C
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 10 Oct 2024 06:58:10 GMT
WORKDIR /opt/spark/work-dir
# Thu, 10 Oct 2024 06:58:10 GMT
USER spark
# Thu, 10 Oct 2024 06:58:10 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 10 Oct 2024 06:58:10 GMT
USER root
# Thu, 10 Oct 2024 06:58:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
USER spark
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e085fa4865328b7a9c7c42be8b9513024d4f44bdc2920894ac00c62a9a95e`  
		Last Modified: Wed, 16 Oct 2024 02:16:41 GMT  
		Size: 16.9 MB (16934550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8300be05210183f961f2c35314f4f15210e564b0c7f333d1a3afd203646c8c0`  
		Last Modified: Wed, 16 Oct 2024 02:18:30 GMT  
		Size: 47.2 MB (47196928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0ca105b5f255f467491418fd72fdfe42e6a1356de685f87662169b0715f451`  
		Last Modified: Wed, 16 Oct 2024 02:18:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ea3932c65771704f94238e80a4b73fb336047b0985f7f41eab190ca652d1b9`  
		Last Modified: Wed, 16 Oct 2024 02:18:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed8b9ebc6451c11fe12453e6931d0c7e0d0a827a7a01d411c7c780e2be51f05`  
		Last Modified: Wed, 16 Oct 2024 16:24:02 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00206c27ad91d6a4595fcd40a0c025ba577cd18fda075abcb9f917201df0bb8d`  
		Last Modified: Wed, 16 Oct 2024 16:24:02 GMT  
		Size: 23.9 MB (23947340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71da398fd0a4337403e3faa61829e612468f99c0d3af498196532ebcdfab579d`  
		Last Modified: Wed, 16 Oct 2024 16:24:06 GMT  
		Size: 324.9 MB (324868536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddb1c9ce5e0d636c27b1d21500de7f9f164d55f96ed9c33cf31e1ac29bfff4b`  
		Last Modified: Wed, 16 Oct 2024 16:24:02 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f54175807c732e5c5b55fdd47c2d27bfdad4bd8a4888986f802101b1732d1a`  
		Last Modified: Wed, 16 Oct 2024 16:52:14 GMT  
		Size: 94.4 MB (94364067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:1e8e66020d8f19fa5c26fc5fd060fbd4de52a8ab9cf4cd57f9fc86a0767e5e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0098ee9ae65e54ff049e3e6342a1310316e7b7cc4965be58f3143d1d90e7dcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8c9cb527f1bc9792376c5618c7b06f6209792bb400e563b0a7ba318c871b9f8a`  
		Last Modified: Wed, 16 Oct 2024 16:52:13 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c59e11f18693bdc8b6a6d0845f72f83566ef6fedee734945a8cf5add343745`  
		Last Modified: Wed, 16 Oct 2024 16:52:12 GMT  
		Size: 11.6 KB (11567 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:b0ed5c1caf908308818b9ef14f9221a2a56243e1711b1361e393189c1e2c6336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525415924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec55649e51b872a71d17eaa6e469f43d02f2a38de63ee8a9667ef04d18370966`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 06:58:10 GMT
ARG RELEASE
# Thu, 10 Oct 2024 06:58:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 06:58:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 06:58:10 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 10 Oct 2024 06:58:10 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 10 Oct 2024 06:58:10 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 10 Oct 2024 06:58:10 GMT
ARG spark_uid=185
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz.asc GPG_KEY=0A2D660358B6F6F8071FD16F6606986CF5A8447C
# Thu, 10 Oct 2024 06:58:10 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv RELEASE /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     ln -s "$(basename /opt/spark/examples/jars/spark-examples_*.jar)" /opt/spark/examples/jars/spark-examples.jar;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
COPY entrypoint.sh /opt/ # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV SPARK_HOME=/opt/spark
# Thu, 10 Oct 2024 06:58:10 GMT
WORKDIR /opt/spark/work-dir
# Thu, 10 Oct 2024 06:58:10 GMT
USER spark
# Thu, 10 Oct 2024 06:58:10 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Thu, 10 Oct 2024 06:58:10 GMT
USER root
# Thu, 10 Oct 2024 06:58:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
USER spark
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d2e9d896341dc2470e5877241905d4df074cef3aed1d0a5b7c9b27fcfb590a`  
		Last Modified: Wed, 16 Oct 2024 01:15:36 GMT  
		Size: 16.8 MB (16789035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d3e6ce9d9873a23088d4c8c20f3e10edd65e6c24d73b130226a512c01f1400`  
		Last Modified: Wed, 16 Oct 2024 01:17:12 GMT  
		Size: 45.6 MB (45557194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf02aa5afe6fa866f8bc348417b9dc717c82ce4393d6ddebffa8090195f2c09a`  
		Last Modified: Wed, 16 Oct 2024 01:17:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4363290e96cb0da840d7de94f4ee52632025634df704f2350d22a1e513cfc321`  
		Last Modified: Wed, 16 Oct 2024 01:17:07 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e8eb86b9fe31ac21097d83b17edb9695cb071e946f70fbc352fd299054ce60`  
		Last Modified: Wed, 16 Oct 2024 04:58:42 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb231e5978db36dbb625e58c18301fad1caa9cdffaa315e6cdd873d0a69ea166`  
		Last Modified: Wed, 16 Oct 2024 04:58:43 GMT  
		Size: 23.7 MB (23670309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c7defcca6136a3721aaadbff4ab880771a0c918be43a37e604743396d960d6`  
		Last Modified: Wed, 16 Oct 2024 04:58:55 GMT  
		Size: 324.9 MB (324868566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa346eea64ba59dd9bab00d70e43d7c74517ed93c1c4420bd8c8a34ba11d663`  
		Last Modified: Wed, 16 Oct 2024 04:58:43 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cd51b5fb4804c3a894a4ff67373734e4f16257a0a611e4ceee8648b46c2633`  
		Last Modified: Wed, 16 Oct 2024 06:16:36 GMT  
		Size: 87.3 MB (87320700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:7275f1943dc25cf0933bf3748ace92977d7ac1651328197477d8562224c4acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62512efd76a1903fff76a638d206cd9f3565b1e2f8339a33ccb3e667b6e7745c`

```dockerfile
```

-	Layers:
	-	`sha256:e15030ba9c91151a9f37e4329e111d94c202eb71f695765785149a4876b2e13d`  
		Last Modified: Wed, 16 Oct 2024 06:16:33 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802d2c9b8866e65240aa1e03ee3d226adc5aab565cb287120c3c5997530345d3`  
		Last Modified: Wed, 16 Oct 2024 06:16:33 GMT  
		Size: 11.7 KB (11743 bytes)  
		MIME: application/vnd.in-toto+json
