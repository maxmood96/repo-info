## `spark:r`

```console
$ docker pull spark@sha256:15341ab27538bc090b7c1dbf33294abd2c58296d3a5110357a20b33d38f77bf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:a4c4c4aace21e77b695f514a3da65ce1e7072830542612684635e9cd5f636a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673793744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6ddb9b42a877f7944924d86b5204ff858ceacc67ba91250372c046d8561fff`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Mon, 12 Aug 2024 09:09:28 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 09:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 12 Aug 2024 09:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 09:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 12 Aug 2024 09:09:28 GMT
ARG spark_uid=185
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.2/spark-3.5.2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.2/spark-3.5.2-bin-hadoop3.tgz.asc GPG_KEY=D76E23B9F11B5BF6864613C4F7051850A0AF904D
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV SPARK_HOME=/opt/spark
# Mon, 12 Aug 2024 09:09:28 GMT
WORKDIR /opt/spark/work-dir
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
# Mon, 12 Aug 2024 09:09:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Mon, 12 Aug 2024 09:09:28 GMT
USER root
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV R_HOME=/usr/lib/R
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b774bb3b629182074f56c4fd66bcbe6c07f5e0078a79dc1520e6715111a73e0`  
		Last Modified: Wed, 02 Oct 2024 02:20:32 GMT  
		Size: 16.9 MB (16934012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a7e8d41460cfca7295663b3f57b7c84907be828639764465fb657240b2415`  
		Last Modified: Wed, 02 Oct 2024 02:22:18 GMT  
		Size: 47.2 MB (47197102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a39e0ccbc1ca6775300f1055383c61c498b946347a98145a03ac109e9554ca`  
		Last Modified: Wed, 02 Oct 2024 02:22:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6313b3869ab6cc2cf6ce82d9a97e1eea96ac4e9f3d7d5ce78de8c9a37251db1`  
		Last Modified: Wed, 02 Oct 2024 02:22:12 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b7bfccf9f7f77ca7736246456d4b8d8e73d73c3dcaa55b25b7d7674e6cd5a`  
		Last Modified: Wed, 02 Oct 2024 02:59:55 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3885a3d71b44bd1874094c53868d492f6f181ba91dfcc4dfcd1371f0cdc845b3`  
		Last Modified: Wed, 02 Oct 2024 02:59:57 GMT  
		Size: 23.9 MB (23947080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c46a5ad6ce6952a3a656dcb6c25e90ff14208bbf306feca7bd26ebc0cc31c`  
		Last Modified: Wed, 02 Oct 2024 03:00:05 GMT  
		Size: 324.8 MB (324826640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e42693bffd8697220e09982db353a175c3c4c1d21955ed790aa9dc83a70816`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582dd79fa172abe3791a2c5840fec4b3e683e432db4be1c374bc436532a4b86`  
		Last Modified: Wed, 02 Oct 2024 03:59:09 GMT  
		Size: 232.3 MB (232299158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:4e5c2dfefec338cd1c1a4bc93f3d87a291e37969f24dc87939eb719b1a1b833c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11189423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d812d56d1708f1a1590d489d162a4d382474bae50f96e532603226aae6a24ed`

```dockerfile
```

-	Layers:
	-	`sha256:7f2d6ceda7040d87709a2faf61071359f6f29585b4b1c33a159afe8884483957`  
		Last Modified: Wed, 02 Oct 2024 03:59:04 GMT  
		Size: 11.2 MB (11178500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b621796ac74804fa0264a97ac9aa4626983254fbb7a59c0ad742a9ce0de8aeba`  
		Last Modified: Wed, 02 Oct 2024 03:59:03 GMT  
		Size: 10.9 KB (10923 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:88e727dd18b6bcd6fcc7d2bf716ab2eb6d188ac864954f77417da208e0c01c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651561657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2481c255bf395ac03e4afb749a45ccfb3209c80f5c21110d8931356607b97afc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Mon, 12 Aug 2024 09:09:28 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 09:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 12 Aug 2024 09:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 09:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 12 Aug 2024 09:09:28 GMT
ARG spark_uid=185
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.5.2/spark-3.5.2-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.5.2/spark-3.5.2-bin-hadoop3.tgz.asc GPG_KEY=D76E23B9F11B5BF6864613C4F7051850A0AF904D
# Mon, 12 Aug 2024 09:09:28 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
COPY entrypoint.sh /opt/ # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV SPARK_HOME=/opt/spark
# Mon, 12 Aug 2024 09:09:28 GMT
WORKDIR /opt/spark/work-dir
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
# Mon, 12 Aug 2024 09:09:28 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Mon, 12 Aug 2024 09:09:28 GMT
USER root
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV R_HOME=/usr/lib/R
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce166e93a5597cccb210bdd5f43826b631f39899dea924699bc4088c0e76f62`  
		Last Modified: Wed, 02 Oct 2024 01:25:01 GMT  
		Size: 16.8 MB (16788912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bffdcf1c7da6f3241a1ec373bdc6fbcda829c82288319794504b576fda5ada8`  
		Last Modified: Wed, 02 Oct 2024 01:26:40 GMT  
		Size: 45.6 MB (45557192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86742142e23e18d393559c275dc52226bcbb49dacc2893267bc0cb7b243b0e5`  
		Last Modified: Wed, 02 Oct 2024 01:26:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12d890905f80749141823dcec87e6cd26b9eacf5f18287734641aca3abfb49d`  
		Last Modified: Wed, 02 Oct 2024 01:26:34 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f4290ade569df2946aec2d556278bc770a928cc9f38b52bd8cd3c9882fc3c`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d191468e62c4fab09447bd3299a2010815fd06fc556a9f094e680d707f73402`  
		Last Modified: Wed, 02 Oct 2024 04:16:29 GMT  
		Size: 23.7 MB (23670232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8171c68305836bb1b2acf51b830a681d121f266ffcffc7e9c91b42812526899b`  
		Last Modified: Wed, 02 Oct 2024 04:16:35 GMT  
		Size: 324.8 MB (324826630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc542ef3434a0f91dd7127d8fb9e0303b4067a17bf769f298bf5309eaf1c2a22`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374f98006a33e1c920b5aec641c17eba38c31c15e5522155c0c9ace76dc7f4fc`  
		Last Modified: Wed, 02 Oct 2024 06:19:31 GMT  
		Size: 213.5 MB (213508836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:096313b278d1bbeeda74bee191308aed2ceee8144211f70cbe5af6d297540894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11174026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c67325d54d81323a1564e17f8caecd6e236b564b675e1e23161d27f36203d`

```dockerfile
```

-	Layers:
	-	`sha256:a7742b6eeb235ae4fae2b3239919e1fb6848405acdd5eed9aa5ac4b635da781d`  
		Last Modified: Wed, 02 Oct 2024 06:19:25 GMT  
		Size: 11.2 MB (11162951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c6bcdeab5dae4f1d0a2a732e014da04c723559d6137b4e61761f2f0f0403fc`  
		Last Modified: Wed, 02 Oct 2024 06:19:25 GMT  
		Size: 11.1 KB (11075 bytes)  
		MIME: application/vnd.in-toto+json
