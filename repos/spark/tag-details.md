<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spark`

-	[`spark:3.4.3`](#spark343)
-	[`spark:3.4.3-python3`](#spark343-python3)
-	[`spark:3.4.3-r`](#spark343-r)
-	[`spark:3.4.3-scala`](#spark343-scala)
-	[`spark:3.4.3-scala2.12-java11-python3-r-ubuntu`](#spark343-scala212-java11-python3-r-ubuntu)
-	[`spark:3.4.3-scala2.12-java11-python3-ubuntu`](#spark343-scala212-java11-python3-ubuntu)
-	[`spark:3.4.3-scala2.12-java11-r-ubuntu`](#spark343-scala212-java11-r-ubuntu)
-	[`spark:3.4.3-scala2.12-java11-ubuntu`](#spark343-scala212-java11-ubuntu)
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

## `spark:3.4.3`

```console
$ docker pull spark@sha256:ac54fa05b838b1c26c16c4883b38220bc47ba68b998e033abeb3b39982363f57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3` - linux; amd64

```console
$ docker pull spark@sha256:9c45cbb51f66a03b26ae0000018d3cb35040acb87045c962b8ff68f8efa30695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529521664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc66f5c069fd82028c5dd6afea76ebfa08d26ac07af54db951337c03c044fe9c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b73dcbdf3a26f2a0f077354c5b7f85ae93cd7c17b4c7b8559bf9b8f2f5f6a2`  
		Last Modified: Wed, 02 Oct 2024 03:58:23 GMT  
		Size: 94.4 MB (94372659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3` - unknown; unknown

```console
$ docker pull spark@sha256:0edf58687d0cc7424a9d4dac7dbe1575e4328b3e88906c41a3134b8dc4b74bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e138aea6afd2a68768d547e0e9040b02d9250491b6e9873cf275fc16fbb46d`

```dockerfile
```

-	Layers:
	-	`sha256:b7feae852816f4c1ef071e4e5130168e0285e6a93023317eeb4063d52c9ecbb9`  
		Last Modified: Wed, 02 Oct 2024 03:58:21 GMT  
		Size: 9.0 MB (9013658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72704693f653043b3f415777da0fad9460c17e6574763c1e8ff02e20fba1d878`  
		Last Modified: Wed, 02 Oct 2024 03:58:20 GMT  
		Size: 10.9 KB (10939 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:25bcaca239703f62fdd5ec11b11b41255f664460be87fe7e9aaa7657c329af53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519036839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92dedbdfa8229268e5521835bb5766344c019f7963c7fcdcba7966d7f832eb1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21ecdd1c7686172c3d9e1a41800b333ddcbf578dc8be5bc634cabacbaaee01`  
		Last Modified: Wed, 02 Oct 2024 06:20:40 GMT  
		Size: 87.3 MB (87329669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3` - unknown; unknown

```console
$ docker pull spark@sha256:3936504911f35bd10ff682df51f1e3b2ccce4cd36f0cee848d6bae124ebbcf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9028656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e289a8ee73038f28531cb09a89498f4e0bfeca6bf3880e95e27aa813d671d`

```dockerfile
```

-	Layers:
	-	`sha256:a447223ef128748fdb4cf7a3ff94e6fe4859ec993ef04fe2b9b9aad16be659e9`  
		Last Modified: Wed, 02 Oct 2024 06:20:38 GMT  
		Size: 9.0 MB (9017564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ce000534555a1c15bee38f7f0e6894465a8cc39348230d0f350d974d1e2a9b`  
		Last Modified: Wed, 02 Oct 2024 06:20:37 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-python3`

```console
$ docker pull spark@sha256:ac54fa05b838b1c26c16c4883b38220bc47ba68b998e033abeb3b39982363f57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-python3` - linux; amd64

```console
$ docker pull spark@sha256:9c45cbb51f66a03b26ae0000018d3cb35040acb87045c962b8ff68f8efa30695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529521664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc66f5c069fd82028c5dd6afea76ebfa08d26ac07af54db951337c03c044fe9c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b73dcbdf3a26f2a0f077354c5b7f85ae93cd7c17b4c7b8559bf9b8f2f5f6a2`  
		Last Modified: Wed, 02 Oct 2024 03:58:23 GMT  
		Size: 94.4 MB (94372659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:0edf58687d0cc7424a9d4dac7dbe1575e4328b3e88906c41a3134b8dc4b74bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e138aea6afd2a68768d547e0e9040b02d9250491b6e9873cf275fc16fbb46d`

```dockerfile
```

-	Layers:
	-	`sha256:b7feae852816f4c1ef071e4e5130168e0285e6a93023317eeb4063d52c9ecbb9`  
		Last Modified: Wed, 02 Oct 2024 03:58:21 GMT  
		Size: 9.0 MB (9013658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72704693f653043b3f415777da0fad9460c17e6574763c1e8ff02e20fba1d878`  
		Last Modified: Wed, 02 Oct 2024 03:58:20 GMT  
		Size: 10.9 KB (10939 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:25bcaca239703f62fdd5ec11b11b41255f664460be87fe7e9aaa7657c329af53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519036839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92dedbdfa8229268e5521835bb5766344c019f7963c7fcdcba7966d7f832eb1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21ecdd1c7686172c3d9e1a41800b333ddcbf578dc8be5bc634cabacbaaee01`  
		Last Modified: Wed, 02 Oct 2024 06:20:40 GMT  
		Size: 87.3 MB (87329669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:3936504911f35bd10ff682df51f1e3b2ccce4cd36f0cee848d6bae124ebbcf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9028656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e289a8ee73038f28531cb09a89498f4e0bfeca6bf3880e95e27aa813d671d`

```dockerfile
```

-	Layers:
	-	`sha256:a447223ef128748fdb4cf7a3ff94e6fe4859ec993ef04fe2b9b9aad16be659e9`  
		Last Modified: Wed, 02 Oct 2024 06:20:38 GMT  
		Size: 9.0 MB (9017564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ce000534555a1c15bee38f7f0e6894465a8cc39348230d0f350d974d1e2a9b`  
		Last Modified: Wed, 02 Oct 2024 06:20:37 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-r`

```console
$ docker pull spark@sha256:1731641cea6b2100576eed6fbd7ad5098b69b7bc256e6001d457617ee44808f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-r` - linux; amd64

```console
$ docker pull spark@sha256:971a46080cfcc85e1a2e650aacf3cebc50bf094d98cb8f79e688fdcb3deafe75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.4 MB (667448542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d3e9b43b9b5e9179f637407779c394ad635b61242f2f976c11b736934a903c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ea69062378d53a9c86dc76dc717e72b6b88071a8ddec376a3b20d6a06cba9`  
		Last Modified: Wed, 02 Oct 2024 03:59:08 GMT  
		Size: 232.3 MB (232299537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:35871160e3d87f9dace657729a128f135b609fe9ce32c047956c58760f9e49bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11179944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac50afb29715d0d75d50e28abc0cf9cc2da44e58168964b0ed9cf787ecc4bee`

```dockerfile
```

-	Layers:
	-	`sha256:86ced091612bcc3e8546ba8ff2a33bac3f421ac1cc99f792808f93c0c2e60e76`  
		Last Modified: Wed, 02 Oct 2024 03:59:01 GMT  
		Size: 11.2 MB (11169307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfcd51a9b190db35847fd3fd776c7f3fb495321f7ac279bf4c6985e19a9d6ab`  
		Last Modified: Wed, 02 Oct 2024 03:59:00 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:96b7f61164f39580dae450a230de924cc10c6bf45048a0a61702c7f5e2041cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.2 MB (645215830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f58726e645456f5c8d5bcf26d815b49802f1702455e54637ad25572a91d0e7d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab2b84e04e7158f0996eb840fb7bcc65b2b61f8b25a7c0e1d2935bd6517e083`  
		Last Modified: Wed, 02 Oct 2024 06:22:23 GMT  
		Size: 213.5 MB (213508660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:7c7ca28afdfa0f1ec9f58ebdf134aa7efb1b97bb9e9a01d6fe877fed890c7b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11164523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee79a3b1dd7e1f03d181d61a5f23ccdd199931c30a23a6f4bda26a997061dd66`

```dockerfile
```

-	Layers:
	-	`sha256:4d9c2541d024a87167453f36a4bd0d8f44218ee4077d015ca0a1e21df63318f6`  
		Last Modified: Wed, 02 Oct 2024 06:22:18 GMT  
		Size: 11.2 MB (11153746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1632e1568bf23814fc3d3dad4fc9858cbafac8e60833fe3553f66869d87aba44`  
		Last Modified: Wed, 02 Oct 2024 06:22:17 GMT  
		Size: 10.8 KB (10777 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala`

```console
$ docker pull spark@sha256:0da19c741bfa8c32b907186a835b87befe94f79e6ce251edf75aad986ee0bd69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala` - linux; amd64

```console
$ docker pull spark@sha256:14eca1fe8e57cc8a1788880ffe4a77047e9cc2f05c51d83c1ce16fd2b817b67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.1 MB (435149005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8529001039bce47adfa63de2b0cfd4a5299d5f0eb8b3a66856df1e2ac50aa700`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:6113557e139512c7641ff602e432db335abef3c05992c187c478c7ab9396e256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7779ed1455ca79e5f87de1999ad8ba91f2f3f716752ebeb1b51d9556f81a1e0`

```dockerfile
```

-	Layers:
	-	`sha256:2b1603009f62e15e9bb85905ce7bf46636ea57a3ecec3d294b87afd66bf36d62`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 4.3 MB (4291845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeaafddd3caf9bff4d18910d2bac2cabbb6eb01346f537032bd86288097cb6c1`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 22.4 KB (22412 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:190cc75f8a10cdfd479beb3b6e5797f9084e680db6785fc3ce9de0c15cb669f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431707170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde56e7f9457e5167f3e135509b35f310f4e45b6297725f6a226f8e3550c8646`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:74fd1f81fa06c1a732100dedaae4b98ea5f0ea5e20a3300c4bf5b02625f90b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b303329f8c1da8a29ffe1c403cb89f06e279a55cc1c6da3d504e5231e610ad`

```dockerfile
```

-	Layers:
	-	`sha256:026eaef9cceb20a3257262b61f9ac8d9e0615c7f29b611904573e8bd3d771423`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 4.3 MB (4292136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7337a4f4e3c48cbc2aedc9b2c7f583b246c98ad7a938634f95b0275266cecbaf`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 22.5 KB (22516 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:9dc6afd720c8f8ae599ac3a102b40cba06c72753eeef3ff8d3dcc4ad7413f084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:01a8d877296fd23006a92b0bbb7707d3756ee68bacadee81538f2407e00b5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.1 MB (689071045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6c4689f985f95c1714b5c53c00e05d77d00af406cf932cb81104740234c58a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44fa80f4111ec41ac55b60cb2852d1f13d9ef4dc7d427020579288113b6eb29`  
		Last Modified: Wed, 02 Oct 2024 03:59:00 GMT  
		Size: 253.9 MB (253922040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d38f3672af5205a53a5b8ced56438732d855704ca1cbc87b02dd054896f4ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12302998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2e51ded02bb6eb1aeca4789c1dc28919dc5a6bcbd861a07545be6b365e6c79`

```dockerfile
```

-	Layers:
	-	`sha256:4828ce5d14dea5ff7a0afe1cb6ce7fb6e2509e1687ccf0029b21def35f3ab154`  
		Last Modified: Wed, 02 Oct 2024 03:58:56 GMT  
		Size: 12.3 MB (12292483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c08e53c1a4652f91fc396939356fe7ed4a018c6aaa143ac6aadd2fe52c4fa1`  
		Last Modified: Wed, 02 Oct 2024 03:58:55 GMT  
		Size: 10.5 KB (10515 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:514a993614e88d5071ba9acdafc5b020bdb8f12e62de955a36cd40f86660013c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.9 MB (666853238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3ea493a46d1423409b4ba0b47ea9e677074004ad682ef21a7dff94a2ccdb98`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aed203e71d026a99bf9498ba031cd4ed522424dcb5d53356d1322f60b801a6`  
		Last Modified: Wed, 02 Oct 2024 06:16:34 GMT  
		Size: 235.1 MB (235146068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2688058efbcaad3313295e56dfb7ea5b10ad0d004d5c48b152212503caad565e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12287620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d86d1e2b9e0fcd737d64fbe318ce5568461cd0247b650aa13f8c81b9f1ccf2c`

```dockerfile
```

-	Layers:
	-	`sha256:03c4b7769eeafafebb0c177d20d4895c48d9f41dc7895f8bf24f91878fc5f7b3`  
		Last Modified: Wed, 02 Oct 2024 06:16:29 GMT  
		Size: 12.3 MB (12276977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f0185e65aa6655aff8f702b3389e25e2d7537c581c9b69371380beb8779563`  
		Last Modified: Wed, 02 Oct 2024 06:16:28 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:ac54fa05b838b1c26c16c4883b38220bc47ba68b998e033abeb3b39982363f57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:9c45cbb51f66a03b26ae0000018d3cb35040acb87045c962b8ff68f8efa30695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529521664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc66f5c069fd82028c5dd6afea76ebfa08d26ac07af54db951337c03c044fe9c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b73dcbdf3a26f2a0f077354c5b7f85ae93cd7c17b4c7b8559bf9b8f2f5f6a2`  
		Last Modified: Wed, 02 Oct 2024 03:58:23 GMT  
		Size: 94.4 MB (94372659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:0edf58687d0cc7424a9d4dac7dbe1575e4328b3e88906c41a3134b8dc4b74bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e138aea6afd2a68768d547e0e9040b02d9250491b6e9873cf275fc16fbb46d`

```dockerfile
```

-	Layers:
	-	`sha256:b7feae852816f4c1ef071e4e5130168e0285e6a93023317eeb4063d52c9ecbb9`  
		Last Modified: Wed, 02 Oct 2024 03:58:21 GMT  
		Size: 9.0 MB (9013658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72704693f653043b3f415777da0fad9460c17e6574763c1e8ff02e20fba1d878`  
		Last Modified: Wed, 02 Oct 2024 03:58:20 GMT  
		Size: 10.9 KB (10939 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:25bcaca239703f62fdd5ec11b11b41255f664460be87fe7e9aaa7657c329af53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.0 MB (519036839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92dedbdfa8229268e5521835bb5766344c019f7963c7fcdcba7966d7f832eb1`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21ecdd1c7686172c3d9e1a41800b333ddcbf578dc8be5bc634cabacbaaee01`  
		Last Modified: Wed, 02 Oct 2024 06:20:40 GMT  
		Size: 87.3 MB (87329669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:3936504911f35bd10ff682df51f1e3b2ccce4cd36f0cee848d6bae124ebbcf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9028656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e289a8ee73038f28531cb09a89498f4e0bfeca6bf3880e95e27aa813d671d`

```dockerfile
```

-	Layers:
	-	`sha256:a447223ef128748fdb4cf7a3ff94e6fe4859ec993ef04fe2b9b9aad16be659e9`  
		Last Modified: Wed, 02 Oct 2024 06:20:38 GMT  
		Size: 9.0 MB (9017564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ce000534555a1c15bee38f7f0e6894465a8cc39348230d0f350d974d1e2a9b`  
		Last Modified: Wed, 02 Oct 2024 06:20:37 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:1731641cea6b2100576eed6fbd7ad5098b69b7bc256e6001d457617ee44808f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:971a46080cfcc85e1a2e650aacf3cebc50bf094d98cb8f79e688fdcb3deafe75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.4 MB (667448542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d3e9b43b9b5e9179f637407779c394ad635b61242f2f976c11b736934a903c`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ea69062378d53a9c86dc76dc717e72b6b88071a8ddec376a3b20d6a06cba9`  
		Last Modified: Wed, 02 Oct 2024 03:59:08 GMT  
		Size: 232.3 MB (232299537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:35871160e3d87f9dace657729a128f135b609fe9ce32c047956c58760f9e49bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11179944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac50afb29715d0d75d50e28abc0cf9cc2da44e58168964b0ed9cf787ecc4bee`

```dockerfile
```

-	Layers:
	-	`sha256:86ced091612bcc3e8546ba8ff2a33bac3f421ac1cc99f792808f93c0c2e60e76`  
		Last Modified: Wed, 02 Oct 2024 03:59:01 GMT  
		Size: 11.2 MB (11169307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfcd51a9b190db35847fd3fd776c7f3fb495321f7ac279bf4c6985e19a9d6ab`  
		Last Modified: Wed, 02 Oct 2024 03:59:00 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:96b7f61164f39580dae450a230de924cc10c6bf45048a0a61702c7f5e2041cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.2 MB (645215830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f58726e645456f5c8d5bcf26d815b49802f1702455e54637ad25572a91d0e7d`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
USER root
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV R_HOME=/usr/lib/R
# Tue, 13 Aug 2024 18:44:34 GMT
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab2b84e04e7158f0996eb840fb7bcc65b2b61f8b25a7c0e1d2935bd6517e083`  
		Last Modified: Wed, 02 Oct 2024 06:22:23 GMT  
		Size: 213.5 MB (213508660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:7c7ca28afdfa0f1ec9f58ebdf134aa7efb1b97bb9e9a01d6fe877fed890c7b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11164523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee79a3b1dd7e1f03d181d61a5f23ccdd199931c30a23a6f4bda26a997061dd66`

```dockerfile
```

-	Layers:
	-	`sha256:4d9c2541d024a87167453f36a4bd0d8f44218ee4077d015ca0a1e21df63318f6`  
		Last Modified: Wed, 02 Oct 2024 06:22:18 GMT  
		Size: 11.2 MB (11153746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1632e1568bf23814fc3d3dad4fc9858cbafac8e60833fe3553f66869d87aba44`  
		Last Modified: Wed, 02 Oct 2024 06:22:17 GMT  
		Size: 10.8 KB (10777 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.4.3-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:0da19c741bfa8c32b907186a835b87befe94f79e6ce251edf75aad986ee0bd69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.4.3-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:14eca1fe8e57cc8a1788880ffe4a77047e9cc2f05c51d83c1ce16fd2b817b67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.1 MB (435149005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8529001039bce47adfa63de2b0cfd4a5299d5f0eb8b3a66856df1e2ac50aa700`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
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
	-	`sha256:83c5b0de22dfc7c4a94caa74b3b59246fbfb186700cae5ad5d739e92188b6b67`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db18edb9dbccf14a409c7dca4e522f6cc933e72526dce01ff4b60c8b851e49`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 23.9 MB (23947142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101337a8d7dafdc62635fab130240e627b80b95616b1d8181249193286d5b4d`  
		Last Modified: Wed, 02 Oct 2024 03:00:01 GMT  
		Size: 318.5 MB (318481052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c612d430a0ef86a7e843660129523885fef8ef69638b02775e67bd655f12c11`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:6113557e139512c7641ff602e432db335abef3c05992c187c478c7ab9396e256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7779ed1455ca79e5f87de1999ad8ba91f2f3f716752ebeb1b51d9556f81a1e0`

```dockerfile
```

-	Layers:
	-	`sha256:2b1603009f62e15e9bb85905ce7bf46636ea57a3ecec3d294b87afd66bf36d62`  
		Last Modified: Wed, 02 Oct 2024 02:59:54 GMT  
		Size: 4.3 MB (4291845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeaafddd3caf9bff4d18910d2bac2cabbb6eb01346f537032bd86288097cb6c1`  
		Last Modified: Wed, 02 Oct 2024 02:59:53 GMT  
		Size: 22.4 KB (22412 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.4.3-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:190cc75f8a10cdfd479beb3b6e5797f9084e680db6785fc3ce9de0c15cb669f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431707170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde56e7f9457e5167f3e135509b35f310f4e45b6297725f6a226f8e3550c8646`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Aug 2024 18:44:34 GMT
ARG RELEASE
# Tue, 13 Aug 2024 18:44:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 18:44:34 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 18:44:34 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 13 Aug 2024 18:44:34 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Aug 2024 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 18:44:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Aug 2024 18:44:34 GMT
ARG spark_uid=185
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN groupadd --system --gid=${spark_uid} spark &&     useradd --system --uid=${spark_uid} --gid=spark spark # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     apt-get update;     apt-get install -y gnupg2 wget bash tini libc6 libpam-modules krb5-user libnss3 procps net-tools gosu libnss-wrapper;     mkdir -p /opt/spark;     mkdir /opt/spark/python;     mkdir -p /opt/spark/examples;     mkdir -p /opt/spark/work-dir;     chmod g+w /opt/spark/work-dir;     touch /opt/spark/RELEASE;     chown -R spark:spark /opt/spark;     echo "auth required pam_wheel.so use_uid" >> /etc/pam.d/su;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_TGZ_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz SPARK_TGZ_ASC_URL=https://archive.apache.org/dist/spark/spark-3.4.3/spark-3.4.3-bin-hadoop3.tgz.asc GPG_KEY=F28C9C925C188C35E345614DEDA00CE834F0FC5C
# Tue, 13 Aug 2024 18:44:34 GMT
# ARGS: spark_uid=185
RUN set -ex;     export SPARK_TMP="$(mktemp -d)";     cd $SPARK_TMP;     wget -nv -O spark.tgz "$SPARK_TGZ_URL";     wget -nv -O spark.tgz.asc "$SPARK_TGZ_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-key "$GPG_KEY" ||     gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY";     gpg --batch --verify spark.tgz.asc spark.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" spark.tgz.asc;         tar -xf spark.tgz --strip-components=1;     chown -R spark:spark .;     mv jars /opt/spark/;     mv bin /opt/spark/;     mv sbin /opt/spark/;     mv kubernetes/dockerfiles/spark/decom.sh /opt/;     mv examples /opt/spark/;     mv kubernetes/tests /opt/spark/;     mv data /opt/spark/;     mv python/pyspark /opt/spark/python/pyspark/;     mv python/lib /opt/spark/python/lib/;     mv R /opt/spark/;     chmod a+x /opt/decom.sh;     cd ..;     rm -rf "$SPARK_TMP"; # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
COPY entrypoint.sh /opt/ # buildkit
# Tue, 13 Aug 2024 18:44:34 GMT
ENV SPARK_HOME=/opt/spark
# Tue, 13 Aug 2024 18:44:34 GMT
WORKDIR /opt/spark/work-dir
# Tue, 13 Aug 2024 18:44:34 GMT
USER spark
# Tue, 13 Aug 2024 18:44:34 GMT
ENTRYPOINT ["/opt/entrypoint.sh"]
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
	-	`sha256:a14060d87c12ba09b68232cbdcaa33a0c49a4ef3737f12e84aa21a7ab53f1f59`  
		Last Modified: Wed, 02 Oct 2024 04:18:04 GMT  
		Size: 318.5 MB (318481030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7fe18e8243d6c97304e9fbe6a9058b2a37d6c542b20a869c43a6be37b07f0`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 2.1 KB (2082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.4.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:74fd1f81fa06c1a732100dedaae4b98ea5f0ea5e20a3300c4bf5b02625f90b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b303329f8c1da8a29ffe1c403cb89f06e279a55cc1c6da3d504e5231e610ad`

```dockerfile
```

-	Layers:
	-	`sha256:026eaef9cceb20a3257262b61f9ac8d9e0615c7f29b611904573e8bd3d771423`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 4.3 MB (4292136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7337a4f4e3c48cbc2aedc9b2c7f583b246c98ad7a938634f95b0275266cecbaf`  
		Last Modified: Wed, 02 Oct 2024 04:17:58 GMT  
		Size: 22.5 KB (22516 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2`

```console
$ docker pull spark@sha256:a52c6fd30c051c9bd67e05731642c3c509c7897013e3a630e74540ca781d7eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2` - linux; amd64

```console
$ docker pull spark@sha256:391d7ee2ac9edce7e60d43cd4b303d44d02ae531e4811e472745f1560c2c0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535866963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2006195df41288bab7acbc48f4badc9e9a5fc52eaf51e9b0252023f7a889d20`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cc6bda7d77b09c1fdbf1646b4ae18ae979b295bd43d9d8a69a66bbaf18c9fa6e`  
		Last Modified: Wed, 02 Oct 2024 03:58:16 GMT  
		Size: 94.4 MB (94372377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2` - unknown; unknown

```console
$ docker pull spark@sha256:be2dabf8fd5f36e0049765a327f6c6b1d842ca9fb4b5d381f8a70a59b138684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f149a5a8cd6bd591e611a15f3fc107df199f42f622e15576caf95844d3529f`

```dockerfile
```

-	Layers:
	-	`sha256:c22a02684770691bf7e3bb725182ad05f8e991cfa66c238219efdc89c1268dd1`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1d208f1f141f4f282ea9ce9bac68b86fc2a4490f281ac3b62dc614f6d81b25`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:28e0eebfd7cb6484ce4bc0b1098ae92212f04a9a2aac055d55ad54154262c336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525383383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612aae4775d87dc5a751acecfe1b018e4196bd88b2396d50bbba5b232dde9cc3`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e74d847c76e29fcfbe9e81cc2b82008d4f4fc8fe71df47b58fa08bbed0328d`  
		Last Modified: Wed, 02 Oct 2024 06:17:47 GMT  
		Size: 87.3 MB (87330562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2` - unknown; unknown

```console
$ docker pull spark@sha256:4e726c55f4acf3bbbb9e4d59a7a30625fd79d47b7e88399702d41fb9937c3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92ed320fe2d5040ab7e2e23705a5aa612d898a90ec39eff146727bbbd24333`

```dockerfile
```

-	Layers:
	-	`sha256:6fd01b175fc4817adaa8c121d905e2618ced1b5af5f5e98348edb1ce3cfdbdd1`  
		Last Modified: Wed, 02 Oct 2024 06:17:44 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a477ffffd67ff71e047f2809d5cb220aa5a1c51dc79dd6525104f82a70ec08`  
		Last Modified: Wed, 02 Oct 2024 06:17:43 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-java17`

```console
$ docker pull spark@sha256:0281d18704a625043b07302fda6dd29f1ee674a9ce963a6c8e7f783ee0f5b527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-java17` - linux; amd64

```console
$ docker pull spark@sha256:acf631a8aab38592f57500fbf086f8e4525b09103462870748843b4dab5d4552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558595184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb3e8d9a352699ae60d342762e83f7dbfdcd8c7e1e1cdb46f3380d35df77577`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53761970764de3460089e38f86d2b14457eafdafb6b7d5761e37f0c0be82107`  
		Last Modified: Tue, 17 Sep 2024 03:01:58 GMT  
		Size: 118.3 MB (118276396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17` - unknown; unknown

```console
$ docker pull spark@sha256:5c4e1a1731e2e5d3867d004d76e27450a48f8627fe80d9a06dd6ef7e2376f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6495a9cba2f7e3026788357dfacd4fb665e9dffc0b80c711297f3375920e8b`

```dockerfile
```

-	Layers:
	-	`sha256:3198ea97f5b615fc32c52fd831013f85c733326f9679222b8ba1db2054801b21`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 9.7 MB (9738492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbef3e46342ea6a466308252abf8c82fdb11ee2f2534b872666af608020bb055`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2d72a89414cdb91f8c47743c51d53eb50c24c9ba738a193b90f515511da0ae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd93d2430a0359673d152eb4432c6aa60b4f053f06f7541a803d1bc9c1d4d319`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53071672103a9f73c7d180c542245f7fbe79ffbcd09a50eaf7e500a6ea948971`  
		Last Modified: Tue, 17 Sep 2024 08:41:45 GMT  
		Size: 114.3 MB (114298029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17` - unknown; unknown

```console
$ docker pull spark@sha256:9dc8a1114306263783eef8cc8958882cb92fe2e1010e6022b1695ba0c2905c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acac5f0e510e8a6bb5acfade884ca55b315d36173e6b33cb739fcb697c77c50`

```dockerfile
```

-	Layers:
	-	`sha256:43712af2d49acf91396c3d2ee0de5dd9e2e0f3c7ddabbfe2dafd8ba8334b174f`  
		Last Modified: Tue, 17 Sep 2024 08:41:43 GMT  
		Size: 9.7 MB (9733558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d024ea648d2dde5d7c35203974bc7b9cd985df0a50b6f6bdac79a5a350be59`  
		Last Modified: Tue, 17 Sep 2024 08:41:42 GMT  
		Size: 11.7 KB (11719 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-java17-python3`

```console
$ docker pull spark@sha256:0281d18704a625043b07302fda6dd29f1ee674a9ce963a6c8e7f783ee0f5b527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:acf631a8aab38592f57500fbf086f8e4525b09103462870748843b4dab5d4552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558595184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb3e8d9a352699ae60d342762e83f7dbfdcd8c7e1e1cdb46f3380d35df77577`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53761970764de3460089e38f86d2b14457eafdafb6b7d5761e37f0c0be82107`  
		Last Modified: Tue, 17 Sep 2024 03:01:58 GMT  
		Size: 118.3 MB (118276396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:5c4e1a1731e2e5d3867d004d76e27450a48f8627fe80d9a06dd6ef7e2376f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6495a9cba2f7e3026788357dfacd4fb665e9dffc0b80c711297f3375920e8b`

```dockerfile
```

-	Layers:
	-	`sha256:3198ea97f5b615fc32c52fd831013f85c733326f9679222b8ba1db2054801b21`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 9.7 MB (9738492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbef3e46342ea6a466308252abf8c82fdb11ee2f2534b872666af608020bb055`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2d72a89414cdb91f8c47743c51d53eb50c24c9ba738a193b90f515511da0ae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd93d2430a0359673d152eb4432c6aa60b4f053f06f7541a803d1bc9c1d4d319`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53071672103a9f73c7d180c542245f7fbe79ffbcd09a50eaf7e500a6ea948971`  
		Last Modified: Tue, 17 Sep 2024 08:41:45 GMT  
		Size: 114.3 MB (114298029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:9dc8a1114306263783eef8cc8958882cb92fe2e1010e6022b1695ba0c2905c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acac5f0e510e8a6bb5acfade884ca55b315d36173e6b33cb739fcb697c77c50`

```dockerfile
```

-	Layers:
	-	`sha256:43712af2d49acf91396c3d2ee0de5dd9e2e0f3c7ddabbfe2dafd8ba8334b174f`  
		Last Modified: Tue, 17 Sep 2024 08:41:43 GMT  
		Size: 9.7 MB (9733558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d024ea648d2dde5d7c35203974bc7b9cd985df0a50b6f6bdac79a5a350be59`  
		Last Modified: Tue, 17 Sep 2024 08:41:42 GMT  
		Size: 11.7 KB (11719 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-java17-r`

```console
$ docker pull spark@sha256:d697c37f77413756a87e977ca5959f5d3fd29cbf06c81f37c21e049d4fbc343c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:f9feaa5553b8d45131d657ab44951d5d7d115ef58ae89c720c16215e0dad675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764152004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335270e29da39fe69af8faa991de3cfe7c1654241ea1414b8baca1019c4fc12`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48181282a70e41fda20d85f380f43ad75d6a630f24e249746d066270d9578a7a`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 323.8 MB (323833216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:f1a7657e72b0ad3487c89030920d6ec616bad138dd2779a568fa72bf8d144387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5bb32fbc6714cda413a94ef2b56af1aa3bc5e51bf8e0f9592339a74ff78ff9`

```dockerfile
```

-	Layers:
	-	`sha256:550616b02d13de4a5c4012ec335981c56c02ba3fc8a49b955246cf68962f6aee`  
		Last Modified: Tue, 17 Sep 2024 03:02:48 GMT  
		Size: 17.8 MB (17764061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc754b915ddb9c4446960e4b1c938848b52e582196712b1bca8e051d40ea74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:48 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e9d45dd1957cc413a2607554bfafe0e4ddc3c1cb97c68b67740d9a615671d0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.9 MB (745850674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e196fc93bef6e38161347ce13fb2616513160a4ee85697d0650306c8ca23ef`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1880bd0bc4b0b103e890767cb8cc1149a3cc382f8485a4dba35aa446571ddf1f`  
		Last Modified: Tue, 17 Sep 2024 08:43:57 GMT  
		Size: 308.5 MB (308503103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:18d434b567435bc5056c0287d69c7cbbce59431925aec1e0e8fd385a402d3700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3b792e9849af5810a57f586961e65e0cbf88bc027061ccb38fc1373facc73e`

```dockerfile
```

-	Layers:
	-	`sha256:698fbeecefc663c9332f4a3eeabf9590b823207a25ccae2686ef775cd73841c9`  
		Last Modified: Tue, 17 Sep 2024 08:43:51 GMT  
		Size: 17.7 MB (17730401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7619c3468b0d56e952e1e1402b1c1333f85cb1e1b0a29af12441f9dbba3a5b`  
		Last Modified: Tue, 17 Sep 2024 08:43:50 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-java17-scala`

```console
$ docker pull spark@sha256:b421ca96ff4303870a1ab9756fb750d21c6058c1620f9b102940954662a2a56b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:54f96bd89455f7e548dada5fa333fb8f1424cdd4f3d602d49f6f64e70085f134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 MB (440318788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2153bfb5198a77181eb88d5ab94e0a2e391818dfb2a6646a9f485f59437043ae`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:060d6583c8b44da67add97ade4a8d8ad744f99909e4bb20b1ddc4fa91c02430f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54cfc803730c2f2f7c45872f53e3625d2776cd2db7f1a980ed8e25ffa26eed8`

```dockerfile
```

-	Layers:
	-	`sha256:ba406e69ef3b341a585d257faa40e9b9d0125e0b6150c781f6ccb669143ee810`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 4.2 MB (4217781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf144db3c0ded63510590ca748f2fdd37b83588d5aed37208647b1d9998d57bc`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:675ac0be6a24553fd7cb0a7f2678681dff499764ecdaf55d91689a50573e7ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437347571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283e9a4225f11188b153ad5e313b85f5058e5117738c4b30b55554efc8664459`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f76b333059318e1bc5fe0ad6741581c9e1febc09729cb6725c3b0008bc622655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4325f5dfb7c1e9739322d037af25186512435947e3fd5cc2d635ceeafdf1d45`

```dockerfile
```

-	Layers:
	-	`sha256:d68d4f1988b64b03b686640333604f9dfce8b43faaf732cfb8f3081923a29c95`  
		Last Modified: Tue, 17 Sep 2024 06:48:11 GMT  
		Size: 4.2 MB (4218096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298a87c88667a1ca4228e25174b77a4005ec47cdabbd3f0e7416955ff807a5fd`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-python3`

```console
$ docker pull spark@sha256:a52c6fd30c051c9bd67e05731642c3c509c7897013e3a630e74540ca781d7eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-python3` - linux; amd64

```console
$ docker pull spark@sha256:391d7ee2ac9edce7e60d43cd4b303d44d02ae531e4811e472745f1560c2c0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535866963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2006195df41288bab7acbc48f4badc9e9a5fc52eaf51e9b0252023f7a889d20`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cc6bda7d77b09c1fdbf1646b4ae18ae979b295bd43d9d8a69a66bbaf18c9fa6e`  
		Last Modified: Wed, 02 Oct 2024 03:58:16 GMT  
		Size: 94.4 MB (94372377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:be2dabf8fd5f36e0049765a327f6c6b1d842ca9fb4b5d381f8a70a59b138684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f149a5a8cd6bd591e611a15f3fc107df199f42f622e15576caf95844d3529f`

```dockerfile
```

-	Layers:
	-	`sha256:c22a02684770691bf7e3bb725182ad05f8e991cfa66c238219efdc89c1268dd1`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1d208f1f141f4f282ea9ce9bac68b86fc2a4490f281ac3b62dc614f6d81b25`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:28e0eebfd7cb6484ce4bc0b1098ae92212f04a9a2aac055d55ad54154262c336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525383383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612aae4775d87dc5a751acecfe1b018e4196bd88b2396d50bbba5b232dde9cc3`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e74d847c76e29fcfbe9e81cc2b82008d4f4fc8fe71df47b58fa08bbed0328d`  
		Last Modified: Wed, 02 Oct 2024 06:17:47 GMT  
		Size: 87.3 MB (87330562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:4e726c55f4acf3bbbb9e4d59a7a30625fd79d47b7e88399702d41fb9937c3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92ed320fe2d5040ab7e2e23705a5aa612d898a90ec39eff146727bbbd24333`

```dockerfile
```

-	Layers:
	-	`sha256:6fd01b175fc4817adaa8c121d905e2618ced1b5af5f5e98348edb1ce3cfdbdd1`  
		Last Modified: Wed, 02 Oct 2024 06:17:44 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a477ffffd67ff71e047f2809d5cb220aa5a1c51dc79dd6525104f82a70ec08`  
		Last Modified: Wed, 02 Oct 2024 06:17:43 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-r`

```console
$ docker pull spark@sha256:15341ab27538bc090b7c1dbf33294abd2c58296d3a5110357a20b33d38f77bf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-r` - linux; amd64

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

### `spark:3.5.2-r` - unknown; unknown

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

### `spark:3.5.2-r` - linux; arm64 variant v8

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

### `spark:3.5.2-r` - unknown; unknown

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

## `spark:3.5.2-scala`

```console
$ docker pull spark@sha256:b03fbd56c502308f012e20e30573de899609b854d41f6a26b5dac6da34fc0928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala` - linux; amd64

```console
$ docker pull spark@sha256:d2904426f936daaead9c83f9f6660956ea69fda8f2d98e90aeb6d273c4261636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441494586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376d88654452d8ff164d8e696df69e82e5149b98adaa418b00afbe73e48850e`
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

### `spark:3.5.2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:c28d0d371311829e42eda9ed5cc856929a928746437b69093de687043da92c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9aebca05865f4fcf28cc2406dae3c169fc44a2635b530529984fc9fa26a860`

```dockerfile
```

-	Layers:
	-	`sha256:90c594b9c58dd9d1842f1155e124d6bc743adebaf58867d50cf4a2795d440354`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b38f2527244efd5730d0e3db88c37b79ff3ed88978a06cd25505901d744a688`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 22.7 KB (22706 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5b7e31e8af65104f9ef770a8c201be68a2eacef2ed2eb07ce64c6bde72b07563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438052821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa4e36aa2a158f51cb6f78b884d9ab22b4b36417113978aab64e36b78db59f`
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

### `spark:3.5.2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:8af255ae39c7ec0d21a93e109b6412dd2f62cac4a1711436a716d6511db0c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde7eb4dd1d70b933df0b090fbdabe343282586eae2350bfb7138f93ae4caa4`

```dockerfile
```

-	Layers:
	-	`sha256:63b452f90f3f3590905d0b8c9f2a876dd1b1bb5d1cbbf42e58dd0f8718c7afb1`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:396db8a2cd553d11ea1095a60d4956c130bc9e78af6dc9fbf81369077eeffadf`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 22.8 KB (22822 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:b64ca3d8258be90164b364d222ea1b22070904abd88bfa39a77f3aca34e0f82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:83039398c7c804b99d37cfa375fe9e9b20eaf2fa2bf4e03bb950121fdfc994e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.4 MB (695416438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819aef2098977ec9b78457079e6f67230c17b52db885065db4411261bf61cf34`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a40ad696a9c84a87b4fcc3ffdc02ed9ee9501bfc7af737ba1f936d967c74f0cb`  
		Last Modified: Wed, 02 Oct 2024 03:59:09 GMT  
		Size: 253.9 MB (253921852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d3cf13fee5191bc9f8c5c752c3cd5a8a3389611a1c578b86d9653d7af683da2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12311904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1dfe0ffd4eb0b5c732a5549f59e239de496b15806b951f8ff2fa58b90f8f54`

```dockerfile
```

-	Layers:
	-	`sha256:9c3b3f8c88876cc803ff69fdc58b0736c52845d02c65c522a95e069ae20d05b5`  
		Last Modified: Wed, 02 Oct 2024 03:59:00 GMT  
		Size: 12.3 MB (12301390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411051f9ae06ce962f391bc5763601d93dd2e537a6d67595e4bb68d18d8a7fa1`  
		Last Modified: Wed, 02 Oct 2024 03:58:59 GMT  
		Size: 10.5 KB (10514 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:9f271fddadb9ed4bbfeb852bfa94903fb83db629464c8c1b3180cfaeb99023b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.2 MB (673198947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c5698697daa677dbacf1f8d79309d1e9334ddfb385faaf02785074341fdbe`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:93d1caaa7b34551df59df6d7c283d4ca93f307d01f64c1aed7a836a603cf00fd`  
		Last Modified: Wed, 02 Oct 2024 06:14:22 GMT  
		Size: 235.1 MB (235146126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a30939382a1effb7c728a0f554db84b853f82776f49071b0fa48cf90de3f96fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12296527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede65a6a448fd03a31db4cebb43d79ae0e73e3d1d806026a0c7daaa71f12f668`

```dockerfile
```

-	Layers:
	-	`sha256:6a3cfb8a04d3ee5cb806104424d91eaa91483dc5868d1829732ab916dbcc21ac`  
		Last Modified: Wed, 02 Oct 2024 06:14:18 GMT  
		Size: 12.3 MB (12285884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acbc3312e73b6f1151c776f5e9b11132415962d9a3dc94d153aa92df1be33f1`  
		Last Modified: Wed, 02 Oct 2024 06:14:17 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:a52c6fd30c051c9bd67e05731642c3c509c7897013e3a630e74540ca781d7eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:391d7ee2ac9edce7e60d43cd4b303d44d02ae531e4811e472745f1560c2c0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535866963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2006195df41288bab7acbc48f4badc9e9a5fc52eaf51e9b0252023f7a889d20`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cc6bda7d77b09c1fdbf1646b4ae18ae979b295bd43d9d8a69a66bbaf18c9fa6e`  
		Last Modified: Wed, 02 Oct 2024 03:58:16 GMT  
		Size: 94.4 MB (94372377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:be2dabf8fd5f36e0049765a327f6c6b1d842ca9fb4b5d381f8a70a59b138684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f149a5a8cd6bd591e611a15f3fc107df199f42f622e15576caf95844d3529f`

```dockerfile
```

-	Layers:
	-	`sha256:c22a02684770691bf7e3bb725182ad05f8e991cfa66c238219efdc89c1268dd1`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1d208f1f141f4f282ea9ce9bac68b86fc2a4490f281ac3b62dc614f6d81b25`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:28e0eebfd7cb6484ce4bc0b1098ae92212f04a9a2aac055d55ad54154262c336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525383383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612aae4775d87dc5a751acecfe1b018e4196bd88b2396d50bbba5b232dde9cc3`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e74d847c76e29fcfbe9e81cc2b82008d4f4fc8fe71df47b58fa08bbed0328d`  
		Last Modified: Wed, 02 Oct 2024 06:17:47 GMT  
		Size: 87.3 MB (87330562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4e726c55f4acf3bbbb9e4d59a7a30625fd79d47b7e88399702d41fb9937c3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92ed320fe2d5040ab7e2e23705a5aa612d898a90ec39eff146727bbbd24333`

```dockerfile
```

-	Layers:
	-	`sha256:6fd01b175fc4817adaa8c121d905e2618ced1b5af5f5e98348edb1ce3cfdbdd1`  
		Last Modified: Wed, 02 Oct 2024 06:17:44 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a477ffffd67ff71e047f2809d5cb220aa5a1c51dc79dd6525104f82a70ec08`  
		Last Modified: Wed, 02 Oct 2024 06:17:43 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:15341ab27538bc090b7c1dbf33294abd2c58296d3a5110357a20b33d38f77bf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java11-r-ubuntu` - linux; amd64

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

### `spark:3.5.2-scala2.12-java11-r-ubuntu` - unknown; unknown

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

### `spark:3.5.2-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

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

### `spark:3.5.2-scala2.12-java11-r-ubuntu` - unknown; unknown

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

## `spark:3.5.2-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:b03fbd56c502308f012e20e30573de899609b854d41f6a26b5dac6da34fc0928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:d2904426f936daaead9c83f9f6660956ea69fda8f2d98e90aeb6d273c4261636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441494586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376d88654452d8ff164d8e696df69e82e5149b98adaa418b00afbe73e48850e`
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

### `spark:3.5.2-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c28d0d371311829e42eda9ed5cc856929a928746437b69093de687043da92c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9aebca05865f4fcf28cc2406dae3c169fc44a2635b530529984fc9fa26a860`

```dockerfile
```

-	Layers:
	-	`sha256:90c594b9c58dd9d1842f1155e124d6bc743adebaf58867d50cf4a2795d440354`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b38f2527244efd5730d0e3db88c37b79ff3ed88978a06cd25505901d744a688`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 22.7 KB (22706 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5b7e31e8af65104f9ef770a8c201be68a2eacef2ed2eb07ce64c6bde72b07563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438052821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa4e36aa2a158f51cb6f78b884d9ab22b4b36417113978aab64e36b78db59f`
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

### `spark:3.5.2-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8af255ae39c7ec0d21a93e109b6412dd2f62cac4a1711436a716d6511db0c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde7eb4dd1d70b933df0b090fbdabe343282586eae2350bfb7138f93ae4caa4`

```dockerfile
```

-	Layers:
	-	`sha256:63b452f90f3f3590905d0b8c9f2a876dd1b1bb5d1cbbf42e58dd0f8718c7afb1`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:396db8a2cd553d11ea1095a60d4956c130bc9e78af6dc9fbf81369077eeffadf`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 22.8 KB (22822 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:5a6d934722711916ff36ca6701e713deb19d75f30142ca911b3ab76c92fa6b7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:2c23ffd58aed28ae825171f8aade6553210aa8cb78e9d8f63a7747eba1eb1c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **778.9 MB (778874082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97f5fe73439dda2f78e0563346d6858f5d5e28738e30cabb0efc3b54a0a8197`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV R_HOME=/usr/lib/R
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb16725baeacc40d0d9a1dcb5fbca2da8409617c1d1d9b6aa58357ab0dc2ed64`  
		Last Modified: Tue, 17 Sep 2024 03:02:54 GMT  
		Size: 338.6 MB (338555294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:363c9045bb43905b3ef88519248b37d3e11bcbfe99959e3879474fc110d3ab97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18786499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c592d7e29b5badf34359d5cb991b8087ef11a14950936540313fb2854fe3e7`

```dockerfile
```

-	Layers:
	-	`sha256:39cf09f6db81c66595126feb94be5862c9bd6d5f98416fb962870c8fdc6d27ad`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 18.8 MB (18775989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4191dcdca6dd42cd828a408844fd93434a9a29f1c5cb181b5699bd80add3ad4`  
		Last Modified: Tue, 17 Sep 2024 03:02:49 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:1d3bbeac6966e0c343eaf15aaa4b8431bc0622ed749aa65d1ffb1b3c2dcad763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 MB (760378605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8d6f2f34a7320e046d051a2a39dab94b146c60269ac462ce097f53566e096a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
ENV R_HOME=/usr/lib/R
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008ff8e0accea1a88348faea4a38e9b996fddf827b847a473684b16b612272d1`  
		Last Modified: Tue, 17 Sep 2024 08:40:18 GMT  
		Size: 323.0 MB (323031034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ffd236b8a53878c9c5628d9a23d6e58cadc00f6d8b183a572c4a755f464d5e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18753260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52619ee2fac45cd018a3808fb9261040110fa310068c30981f6282a0752be72d`

```dockerfile
```

-	Layers:
	-	`sha256:90dee13e2226e7a0e65f8dfb32a00c6f41b4d188c0fd7b83c5000f427188a828`  
		Last Modified: Tue, 17 Sep 2024 08:40:11 GMT  
		Size: 18.7 MB (18742341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113f999128c17cf11cc0fc5cd276e3493ce307586ff48d1f287caaeff599e6b3`  
		Last Modified: Tue, 17 Sep 2024 08:40:10 GMT  
		Size: 10.9 KB (10919 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:0281d18704a625043b07302fda6dd29f1ee674a9ce963a6c8e7f783ee0f5b527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:acf631a8aab38592f57500fbf086f8e4525b09103462870748843b4dab5d4552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558595184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb3e8d9a352699ae60d342762e83f7dbfdcd8c7e1e1cdb46f3380d35df77577`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53761970764de3460089e38f86d2b14457eafdafb6b7d5761e37f0c0be82107`  
		Last Modified: Tue, 17 Sep 2024 03:01:58 GMT  
		Size: 118.3 MB (118276396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:5c4e1a1731e2e5d3867d004d76e27450a48f8627fe80d9a06dd6ef7e2376f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6495a9cba2f7e3026788357dfacd4fb665e9dffc0b80c711297f3375920e8b`

```dockerfile
```

-	Layers:
	-	`sha256:3198ea97f5b615fc32c52fd831013f85c733326f9679222b8ba1db2054801b21`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 9.7 MB (9738492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbef3e46342ea6a466308252abf8c82fdb11ee2f2534b872666af608020bb055`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2d72a89414cdb91f8c47743c51d53eb50c24c9ba738a193b90f515511da0ae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd93d2430a0359673d152eb4432c6aa60b4f053f06f7541a803d1bc9c1d4d319`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53071672103a9f73c7d180c542245f7fbe79ffbcd09a50eaf7e500a6ea948971`  
		Last Modified: Tue, 17 Sep 2024 08:41:45 GMT  
		Size: 114.3 MB (114298029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:9dc8a1114306263783eef8cc8958882cb92fe2e1010e6022b1695ba0c2905c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acac5f0e510e8a6bb5acfade884ca55b315d36173e6b33cb739fcb697c77c50`

```dockerfile
```

-	Layers:
	-	`sha256:43712af2d49acf91396c3d2ee0de5dd9e2e0f3c7ddabbfe2dafd8ba8334b174f`  
		Last Modified: Tue, 17 Sep 2024 08:41:43 GMT  
		Size: 9.7 MB (9733558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d024ea648d2dde5d7c35203974bc7b9cd985df0a50b6f6bdac79a5a350be59`  
		Last Modified: Tue, 17 Sep 2024 08:41:42 GMT  
		Size: 11.7 KB (11719 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:d697c37f77413756a87e977ca5959f5d3fd29cbf06c81f37c21e049d4fbc343c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:f9feaa5553b8d45131d657ab44951d5d7d115ef58ae89c720c16215e0dad675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.2 MB (764152004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335270e29da39fe69af8faa991de3cfe7c1654241ea1414b8baca1019c4fc12`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48181282a70e41fda20d85f380f43ad75d6a630f24e249746d066270d9578a7a`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 323.8 MB (323833216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f1a7657e72b0ad3487c89030920d6ec616bad138dd2779a568fa72bf8d144387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5bb32fbc6714cda413a94ef2b56af1aa3bc5e51bf8e0f9592339a74ff78ff9`

```dockerfile
```

-	Layers:
	-	`sha256:550616b02d13de4a5c4012ec335981c56c02ba3fc8a49b955246cf68962f6aee`  
		Last Modified: Tue, 17 Sep 2024 03:02:48 GMT  
		Size: 17.8 MB (17764061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc754b915ddb9c4446960e4b1c938848b52e582196712b1bca8e051d40ea74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:48 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:e9d45dd1957cc413a2607554bfafe0e4ddc3c1cb97c68b67740d9a615671d0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.9 MB (745850674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e196fc93bef6e38161347ce13fb2616513160a4ee85697d0650306c8ca23ef`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1880bd0bc4b0b103e890767cb8cc1149a3cc382f8485a4dba35aa446571ddf1f`  
		Last Modified: Tue, 17 Sep 2024 08:43:57 GMT  
		Size: 308.5 MB (308503103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:18d434b567435bc5056c0287d69c7cbbce59431925aec1e0e8fd385a402d3700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3b792e9849af5810a57f586961e65e0cbf88bc027061ccb38fc1373facc73e`

```dockerfile
```

-	Layers:
	-	`sha256:698fbeecefc663c9332f4a3eeabf9590b823207a25ccae2686ef775cd73841c9`  
		Last Modified: Tue, 17 Sep 2024 08:43:51 GMT  
		Size: 17.7 MB (17730401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7619c3468b0d56e952e1e1402b1c1333f85cb1e1b0a29af12441f9dbba3a5b`  
		Last Modified: Tue, 17 Sep 2024 08:43:50 GMT  
		Size: 11.1 KB (11067 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.2-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:b421ca96ff4303870a1ab9756fb750d21c6058c1620f9b102940954662a2a56b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.2-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:54f96bd89455f7e548dada5fa333fb8f1424cdd4f3d602d49f6f64e70085f134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 MB (440318788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2153bfb5198a77181eb88d5ab94e0a2e391818dfb2a6646a9f485f59437043ae`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:060d6583c8b44da67add97ade4a8d8ad744f99909e4bb20b1ddc4fa91c02430f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54cfc803730c2f2f7c45872f53e3625d2776cd2db7f1a980ed8e25ffa26eed8`

```dockerfile
```

-	Layers:
	-	`sha256:ba406e69ef3b341a585d257faa40e9b9d0125e0b6150c781f6ccb669143ee810`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 4.2 MB (4217781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf144db3c0ded63510590ca748f2fdd37b83588d5aed37208647b1d9998d57bc`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.2-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:675ac0be6a24553fd7cb0a7f2678681dff499764ecdaf55d91689a50573e7ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437347571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283e9a4225f11188b153ad5e313b85f5058e5117738c4b30b55554efc8664459`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.2-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f76b333059318e1bc5fe0ad6741581c9e1febc09729cb6725c3b0008bc622655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4325f5dfb7c1e9739322d037af25186512435947e3fd5cc2d635ceeafdf1d45`

```dockerfile
```

-	Layers:
	-	`sha256:d68d4f1988b64b03b686640333604f9dfce8b43faaf732cfb8f3081923a29c95`  
		Last Modified: Tue, 17 Sep 2024 06:48:11 GMT  
		Size: 4.2 MB (4218096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298a87c88667a1ca4228e25174b77a4005ec47cdabbd3f0e7416955ff807a5fd`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 22.7 KB (22714 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2`

```console
$ docker pull spark@sha256:8ee19d3767ef0b49eccaeb53a0757d296ae860030e4ed3e184c13e623bb2628d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2` - linux; amd64

```console
$ docker pull spark@sha256:f452c462462ad3b91d0660f6b2e2c8628cf2df425d1e639cece477e426930d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **775.9 MB (775854662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972404e95ccc273aabf9107ac67d0b1984a6b9b134b4dcad0bff79245c3211b1`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4354418089c076326deb2b7f0ffc9d05a6646b2b4141d5ddac0a2667c257ca`  
		Last Modified: Tue, 08 Oct 2024 17:50:59 GMT  
		Size: 113.9 MB (113887481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:448da97355a7a1014a32766a597eee63797850f399fd77576e7cdd761d2b4abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208d78b1d61bb0cf774ba5cd41ae7d56ffc707a24eb3755962c23b7a5f8109c`

```dockerfile
```

-	Layers:
	-	`sha256:d1705abf590ccdfe97ace3dfb8751b091641ed402443a811960c823790c04fe6`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 10.0 MB (10015520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9fac52666a58eae057890afc3b1a096e6b7f4ebb7fb5748d6e0e44aee8b568`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 11.1 KB (11072 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d2d6d5f074acedaa1ad7f24a784859020e406427c45d3395958266a85fe0624e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.2 MB (768222538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f171be635a93386351a0c96ba03e5597ee7840bed7aa5587bfe936923291c7`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f0df5b87ceb6f5259db659f4764f1176ec42c66fb0dc2b7ee57d77f9cc2f7`  
		Last Modified: Tue, 08 Oct 2024 18:03:27 GMT  
		Size: 108.4 MB (108431515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2` - unknown; unknown

```console
$ docker pull spark@sha256:61a092c6d7d04ef354aadd8f5231777edf2a0f112708d4fbcaa91c3bcf870736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10021179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3da6c0af881992a6c46c447420788ff83911f02b2987f8639126cadd662589b`

```dockerfile
```

-	Layers:
	-	`sha256:922751ea9281a4e990bccc89214e16f25e63348dbc30309d6d55658a5e09bce2`  
		Last Modified: Tue, 08 Oct 2024 18:03:22 GMT  
		Size: 10.0 MB (10009955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9eef8165ba2b68078289e9738d47c773ea50b096120689fdc77e64c7c84f6`  
		Last Modified: Tue, 08 Oct 2024 18:03:21 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21`

```console
$ docker pull spark@sha256:1d473d5bf0a92b73d49399b432b39df10106d1e47f29b93ed317cc552a9c319a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21` - linux; amd64

```console
$ docker pull spark@sha256:fed179db509ff0aa53b34aec4fc973e7cb8b95d1e8c78db07437fd77ddd63e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.3 MB (789263662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0b7f7e66c7c4e2952eb0c807e61761ccb8b90c3cf1e01a30991b479ec1abc5`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678b2a0fa4a71c7d3ab106f08416a1a7b39d99295000c2b218b7b6c3d905010`  
		Last Modified: Tue, 08 Oct 2024 17:51:07 GMT  
		Size: 113.9 MB (113886615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:2aa98c06cffcb0eedecfa9ace3a77f0a1290a9867b0cc28adcc8a6013816e639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10030388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65911f109bfb4dc7c00bb9c665e2e729da68b9d4d9ce3fd86ae2c629e2aa03d`

```dockerfile
```

-	Layers:
	-	`sha256:7c6652b2b030ec087129c2966b211f578eafbc432b8200f798c941552cb5333a`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 10.0 MB (10019289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b65b37bb6d87571187821ad9c4cf2a3329c346daf71d33d542df0d37665148d`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ceb67b1faa9783a0f68073a84dd49a1b9b3aa58d210783106e750581ebdf1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.0 MB (781013044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c515005990cfc759e075db2760b18a04252624bd55add8d23ec277c2edad8267`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c36288f05e88c1aee71a937cec2ee7725195dbe65ea01f8c76c0f9641bf6c`  
		Last Modified: Tue, 08 Oct 2024 17:59:39 GMT  
		Size: 108.4 MB (108432273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21` - unknown; unknown

```console
$ docker pull spark@sha256:ea7249a94b6fda3ebd8f3ee1bc4407ba3636cd3c74f746062dd1e2505e82dc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10024975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87771b04fc2b04ab566f503ae73c3b982b27b60a26116220f8b761d10e703bc1`

```dockerfile
```

-	Layers:
	-	`sha256:0aa966cba350c6e99f3ed53d1f3dff980b4589ca4660aef1f03c22f052f2f1a6`  
		Last Modified: Tue, 08 Oct 2024 17:59:36 GMT  
		Size: 10.0 MB (10013724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0944ac5fa1553d27f2631a22278f5914c73628ee68e8d6ed6b12a27a06f1dc`  
		Last Modified: Tue, 08 Oct 2024 17:59:35 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-python3`

```console
$ docker pull spark@sha256:1d473d5bf0a92b73d49399b432b39df10106d1e47f29b93ed317cc552a9c319a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-python3` - linux; amd64

```console
$ docker pull spark@sha256:fed179db509ff0aa53b34aec4fc973e7cb8b95d1e8c78db07437fd77ddd63e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.3 MB (789263662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0b7f7e66c7c4e2952eb0c807e61761ccb8b90c3cf1e01a30991b479ec1abc5`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678b2a0fa4a71c7d3ab106f08416a1a7b39d99295000c2b218b7b6c3d905010`  
		Last Modified: Tue, 08 Oct 2024 17:51:07 GMT  
		Size: 113.9 MB (113886615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:2aa98c06cffcb0eedecfa9ace3a77f0a1290a9867b0cc28adcc8a6013816e639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10030388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65911f109bfb4dc7c00bb9c665e2e729da68b9d4d9ce3fd86ae2c629e2aa03d`

```dockerfile
```

-	Layers:
	-	`sha256:7c6652b2b030ec087129c2966b211f578eafbc432b8200f798c941552cb5333a`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 10.0 MB (10019289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b65b37bb6d87571187821ad9c4cf2a3329c346daf71d33d542df0d37665148d`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ceb67b1faa9783a0f68073a84dd49a1b9b3aa58d210783106e750581ebdf1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.0 MB (781013044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c515005990cfc759e075db2760b18a04252624bd55add8d23ec277c2edad8267`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c36288f05e88c1aee71a937cec2ee7725195dbe65ea01f8c76c0f9641bf6c`  
		Last Modified: Tue, 08 Oct 2024 17:59:39 GMT  
		Size: 108.4 MB (108432273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-python3` - unknown; unknown

```console
$ docker pull spark@sha256:ea7249a94b6fda3ebd8f3ee1bc4407ba3636cd3c74f746062dd1e2505e82dc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10024975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87771b04fc2b04ab566f503ae73c3b982b27b60a26116220f8b761d10e703bc1`

```dockerfile
```

-	Layers:
	-	`sha256:0aa966cba350c6e99f3ed53d1f3dff980b4589ca4660aef1f03c22f052f2f1a6`  
		Last Modified: Tue, 08 Oct 2024 17:59:36 GMT  
		Size: 10.0 MB (10013724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0944ac5fa1553d27f2631a22278f5914c73628ee68e8d6ed6b12a27a06f1dc`  
		Last Modified: Tue, 08 Oct 2024 17:59:35 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-r`

```console
$ docker pull spark@sha256:ce87d49f9944116903caf5d5cfc8b2c37e500e75b611030c6c50b6cc750cec0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-r` - linux; amd64

```console
$ docker pull spark@sha256:475f5ac65fc99f695bdc8fc16ef367a1a1f912f2b96ba8b756f1198432afbfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.7 MB (994687057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d772cf7424b4d16692c0dcb86a91469b72f37360601db35bb076871afddb34c`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e249da86e5aa3603d8b89acd4e889efa846e2253fc4acc4131f5d0947bcfc426`  
		Last Modified: Tue, 08 Oct 2024 17:52:11 GMT  
		Size: 319.3 MB (319310010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:d100ac74f90c8dbbf8d54abe562daf697f0fcf76f145f50d91b08ac411b46801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18055915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525ea80313d696f5b1f9fa0bec5bb23558a58506ba358b98f22dbce8c2728600`

```dockerfile
```

-	Layers:
	-	`sha256:9944ff5d2bb611690a7d7ff98da7c6308b6caecf24368f18bb79624b6157839f`  
		Last Modified: Tue, 08 Oct 2024 17:52:04 GMT  
		Size: 18.0 MB (18045152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391b3fdac6f29ec9a0a7a821ff9038aa7a4d7318e8d3175e4235eefcc1e00342`  
		Last Modified: Tue, 08 Oct 2024 17:52:03 GMT  
		Size: 10.8 KB (10763 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d95740553864c92ca56ef19728672748fff6d81337b38062b6ed98c3a3310ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.1 MB (975059663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdaf7f86e5395349e8ce28fcdbbe3f9e3460e7e899a6570ee8183221b4a9d20`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a9568d4e54c351aa7f7961a4fe84c432b25049ab18b723a8df506ee38e931`  
		Last Modified: Tue, 08 Oct 2024 18:02:01 GMT  
		Size: 302.5 MB (302478892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-r` - unknown; unknown

```console
$ docker pull spark@sha256:deb666ab30d479a81217bd70a36a26a1dca8282e6e49e3b5032a6547a859f6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18021776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fa7d92eb52130a5579d0e89ec51b9390b030a702c329eeb3e74de76d809140`

```dockerfile
```

-	Layers:
	-	`sha256:58c2faecd05266f5828b21d0ced072f26fcfee95047826cb2be0f8059fcf2aad`  
		Last Modified: Tue, 08 Oct 2024 18:01:55 GMT  
		Size: 18.0 MB (18010873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6fa15c8ab702a9db724600ae307afbf8b68d9a52087f318ca9454530496e74`  
		Last Modified: Tue, 08 Oct 2024 18:01:54 GMT  
		Size: 10.9 KB (10903 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-java21-scala`

```console
$ docker pull spark@sha256:0d3efee40e3ee5e57fafd123f3e12ddc10dba0e446b585afbfa97a2b632fc156
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-java21-scala` - linux; amd64

```console
$ docker pull spark@sha256:83eb94329e41afa2f20bc6883b36b5c19dc3da6f147500a8a129aedc07b78a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.4 MB (675377047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c379b3916e88d7e79b48177f9fee4a858c1e3412ea527ab6bbfc67dadc8fde`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:61104ede3535131a70bc8114cb63b209a7b8dd8c4c33acd0f20a8741b2bf62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de834e4d1a0fd899c07753d088e09a06ccf9fe581fcbc439ae815dd1690598`

```dockerfile
```

-	Layers:
	-	`sha256:fbd98e9b9b3ef15666b50493b8f9c118038166f8b17e4672eba64a703411047c`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 4.7 MB (4655300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4809721de48427d1b304287ba343c18edc347c84c3ebb78156012960d2dadc47`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 23.0 KB (22977 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-java21-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f9c11a10b16f916cc7517bc05de253cf8c81885ca4b6697df17cddfbd331b619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672580771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd9a932563c0437ca41152681c8711583c6000dab64276f741b6c81ee77cb72`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-java21-scala` - unknown; unknown

```console
$ docker pull spark@sha256:29b423a2f9f0814bf9de2efa4dffd2265ae8eadb23adcccdd1b88e29e3640a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4773996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d855dfee88cbc62dac473e2bbe43e2a00a4ce001639f75ad5debb3e9392d51`

```dockerfile
```

-	Layers:
	-	`sha256:38e61672a9c2550e241443a99c4ad1829ef64ae2d3532549c8f8a9d15b039ae2`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 4.8 MB (4750915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa1724d40b35092b53ed1ca87952e8be4c5d4ca569eed1e8512dadb8dfb0e1f`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 23.1 KB (23081 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-python3`

```console
$ docker pull spark@sha256:8ee19d3767ef0b49eccaeb53a0757d296ae860030e4ed3e184c13e623bb2628d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-python3` - linux; amd64

```console
$ docker pull spark@sha256:f452c462462ad3b91d0660f6b2e2c8628cf2df425d1e639cece477e426930d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **775.9 MB (775854662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972404e95ccc273aabf9107ac67d0b1984a6b9b134b4dcad0bff79245c3211b1`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4354418089c076326deb2b7f0ffc9d05a6646b2b4141d5ddac0a2667c257ca`  
		Last Modified: Tue, 08 Oct 2024 17:50:59 GMT  
		Size: 113.9 MB (113887481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:448da97355a7a1014a32766a597eee63797850f399fd77576e7cdd761d2b4abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208d78b1d61bb0cf774ba5cd41ae7d56ffc707a24eb3755962c23b7a5f8109c`

```dockerfile
```

-	Layers:
	-	`sha256:d1705abf590ccdfe97ace3dfb8751b091641ed402443a811960c823790c04fe6`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 10.0 MB (10015520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9fac52666a58eae057890afc3b1a096e6b7f4ebb7fb5748d6e0e44aee8b568`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 11.1 KB (11072 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d2d6d5f074acedaa1ad7f24a784859020e406427c45d3395958266a85fe0624e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.2 MB (768222538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f171be635a93386351a0c96ba03e5597ee7840bed7aa5587bfe936923291c7`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f0df5b87ceb6f5259db659f4764f1176ec42c66fb0dc2b7ee57d77f9cc2f7`  
		Last Modified: Tue, 08 Oct 2024 18:03:27 GMT  
		Size: 108.4 MB (108431515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-python3` - unknown; unknown

```console
$ docker pull spark@sha256:61a092c6d7d04ef354aadd8f5231777edf2a0f112708d4fbcaa91c3bcf870736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10021179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3da6c0af881992a6c46c447420788ff83911f02b2987f8639126cadd662589b`

```dockerfile
```

-	Layers:
	-	`sha256:922751ea9281a4e990bccc89214e16f25e63348dbc30309d6d55658a5e09bce2`  
		Last Modified: Tue, 08 Oct 2024 18:03:22 GMT  
		Size: 10.0 MB (10009955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9eef8165ba2b68078289e9738d47c773ea50b096120689fdc77e64c7c84f6`  
		Last Modified: Tue, 08 Oct 2024 18:03:21 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-r`

```console
$ docker pull spark@sha256:4a770909beb5f0862324256a618327dc1ec089a61097310f7a2cca52c547bc57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-r` - linux; amd64

```console
$ docker pull spark@sha256:891762f04c30f78c405be44042791bcbc11e64067471e60b9ce41c122fb341c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.3 MB (981277608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5d74fbe1151869102aa6ad0c2620f225feca28a067beaff7c853f545e8fda4`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219a986d1231aa063d9c872065d7fffffbfd239762088a20aa7fabbbc857bfc2`  
		Last Modified: Tue, 08 Oct 2024 17:51:47 GMT  
		Size: 319.3 MB (319310427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:40edfab0e3bcd546d3faf1a69d5b40f32ef553788e63168ca79e492ea2814c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18052147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861e5f6ad5873a7cc423c186ca49e2847aa8707c0883d468d156a896619b644e`

```dockerfile
```

-	Layers:
	-	`sha256:29d22dd42324d957588b5a7ffe92f08c742b26edd3366e54de5d7f38fbcd3488`  
		Last Modified: Tue, 08 Oct 2024 17:51:43 GMT  
		Size: 18.0 MB (18041397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2708f5c8d44acc149f22b91961a755a162a7af7450405dd1373cbb7506e665`  
		Last Modified: Tue, 08 Oct 2024 17:51:42 GMT  
		Size: 10.8 KB (10750 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:be1218562bc25999200fdade784c182cefd2cdec829137e848ec1a60d7f2ba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.3 MB (962269329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7674ddae9cfee11255a059e978fd66d0e27ac35a591050140592ee97c4a0525`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff6fdb1308fe94fdc86aadcb3a827b4fe607025a433850088a403e5af86f7b9`  
		Last Modified: Tue, 08 Oct 2024 18:05:52 GMT  
		Size: 302.5 MB (302478306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-r` - unknown; unknown

```console
$ docker pull spark@sha256:2dc11c62fcce02ab71d7d6ed9c1d70e72b2dc54b0d147f0eb99db4c38958ccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18018008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2306dacc7a5e1cc812455c889c5e2ab79187a3cdcff7384d83ab479c0ab4a7`

```dockerfile
```

-	Layers:
	-	`sha256:ec26f1f26e21b2b365915787a6f04303b2ec8d4cea37af743055cdb69a150619`  
		Last Modified: Tue, 08 Oct 2024 18:05:44 GMT  
		Size: 18.0 MB (18007118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397e964336e9e440043637d747e271edad375b6f4d5f0409dda9c4e662cf77e9`  
		Last Modified: Tue, 08 Oct 2024 18:05:43 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala`

```console
$ docker pull spark@sha256:cc025df34b1079ce9af860fefd120283a00a8034aa67e9e00c3c363622be6b74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala` - linux; amd64

```console
$ docker pull spark@sha256:0f32feb484b21a893e9f6104004a24d66ffc6d517bd637038c6f4e2739f74371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 MB (661967181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf237fb54677cd6ac7b5c942f8311002d9b7dab8c8764ac818076ccf3b880934`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f3bfc9425877c114cac52976d4d894a140e43922baf8934d91722cdd9bc1820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4674511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8033d4c92415c11faed8d7139b61c62cee3c8237a869d3781956bfc60e5a590`

```dockerfile
```

-	Layers:
	-	`sha256:3f74df0ae6ca748112efb026e091581e0e3f1bd6f4719d4fa61761dc06783d38`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 4.7 MB (4651545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdcfc41d1cda6f01434377f3d5c34802b3ec9d4c15d1c37c5242706b19eec82c`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 23.0 KB (22966 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:986bae796005a635e45570203859d66701ec65d0fcafb13c16b95c097f885638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.8 MB (659791023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956ff0438aba713eebbc8fea28d762da1128f03ed056daebc389ba572eb37fcf`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala` - unknown; unknown

```console
$ docker pull spark@sha256:58cfa5db985722ce2f8c5454f2a0a03853298c7e7468b57b469a58260b3163db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4770230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51edbecf3ced8529aeb0da628365cd8d837c25a58d2f8a1160596b010f574c39`

```dockerfile
```

-	Layers:
	-	`sha256:d9044ac8ea0138b904f8bfb194783cf00de54c74fcd5aeb9025c727a6966471a`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 4.7 MB (4747160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e18f4e13e638b0de8327794041a47b53a956959b8d0dc0de175c5246a1b42d8`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:8ae83dfaa09329a896bf2f2c9173f48a2c7ff66ae1d9727a55df4d69a780657f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:39c1543edd69f927787d6586df8d12f23eb16354f1aa2367faeb6709ff9b51fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.1 MB (996137648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5f995a6d7bc4953e9e27df84ee3cad626aec4abcbc6c3f3a51f54ec68f131a`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de4f7d27226fb4f91b42a91f356a09ecd9efac36137279d11fe0a5834aa1cb1`  
		Last Modified: Tue, 08 Oct 2024 17:52:18 GMT  
		Size: 334.2 MB (334170467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:51df677d007f25b22c05fbad747d5a2007d6914c90f3433ebad2f01f6b5784e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19063931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a045824f90b4d220f4de43ce0500a88a2454217ca0a70cb39f0ed1e039b90b49`

```dockerfile
```

-	Layers:
	-	`sha256:ef6b8e36ebff4938cc542fc15519b530ebe1bfd47bf55841784d01de6ca38bf2`  
		Last Modified: Tue, 08 Oct 2024 17:52:07 GMT  
		Size: 19.1 MB (19053321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a3bfa1121b77168a2b0b8dd4721f655cbf0f25004a3416673e7344937913b2`  
		Last Modified: Tue, 08 Oct 2024 17:52:06 GMT  
		Size: 10.6 KB (10610 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:456df6f2653a2aaa658b3fd98c3c9691492417d273aa35809a575c96601700cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.0 MB (976976735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53cf89e4331b14da79075d28dea541b93321d1eab1a3b1d685978a9c2b80ffe`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8244fb57a8e4cd303b696f3e44a68d4c07f3110100771e819bbe8c9147dc0bcb`  
		Last Modified: Tue, 08 Oct 2024 17:58:20 GMT  
		Size: 317.2 MB (317185712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:b0d34523ec97a4ba343c4b03238588166345842483cf1974e095ea26ce9f1b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19029791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11994f7177b5e8524efbb3b1b742600bed8ec690d5ff8c21048d96f85ce1ee2a`

```dockerfile
```

-	Layers:
	-	`sha256:5d0904c4232e3905f2b2031964018272de5ea6b46a8c1bae96768bf1def5ff43`  
		Last Modified: Tue, 08 Oct 2024 17:58:13 GMT  
		Size: 19.0 MB (19019054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28dd65b301ce60126624708eb52871696524a90a3fa990bb08bfc450ca652888`  
		Last Modified: Tue, 08 Oct 2024 17:58:12 GMT  
		Size: 10.7 KB (10737 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:8ee19d3767ef0b49eccaeb53a0757d296ae860030e4ed3e184c13e623bb2628d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:f452c462462ad3b91d0660f6b2e2c8628cf2df425d1e639cece477e426930d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **775.9 MB (775854662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972404e95ccc273aabf9107ac67d0b1984a6b9b134b4dcad0bff79245c3211b1`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4354418089c076326deb2b7f0ffc9d05a6646b2b4141d5ddac0a2667c257ca`  
		Last Modified: Tue, 08 Oct 2024 17:50:59 GMT  
		Size: 113.9 MB (113887481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:448da97355a7a1014a32766a597eee63797850f399fd77576e7cdd761d2b4abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208d78b1d61bb0cf774ba5cd41ae7d56ffc707a24eb3755962c23b7a5f8109c`

```dockerfile
```

-	Layers:
	-	`sha256:d1705abf590ccdfe97ace3dfb8751b091641ed402443a811960c823790c04fe6`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 10.0 MB (10015520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9fac52666a58eae057890afc3b1a096e6b7f4ebb7fb5748d6e0e44aee8b568`  
		Last Modified: Tue, 08 Oct 2024 17:50:57 GMT  
		Size: 11.1 KB (11072 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d2d6d5f074acedaa1ad7f24a784859020e406427c45d3395958266a85fe0624e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.2 MB (768222538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f171be635a93386351a0c96ba03e5597ee7840bed7aa5587bfe936923291c7`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f0df5b87ceb6f5259db659f4764f1176ec42c66fb0dc2b7ee57d77f9cc2f7`  
		Last Modified: Tue, 08 Oct 2024 18:03:27 GMT  
		Size: 108.4 MB (108431515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:61a092c6d7d04ef354aadd8f5231777edf2a0f112708d4fbcaa91c3bcf870736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10021179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3da6c0af881992a6c46c447420788ff83911f02b2987f8639126cadd662589b`

```dockerfile
```

-	Layers:
	-	`sha256:922751ea9281a4e990bccc89214e16f25e63348dbc30309d6d55658a5e09bce2`  
		Last Modified: Tue, 08 Oct 2024 18:03:22 GMT  
		Size: 10.0 MB (10009955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9eef8165ba2b68078289e9738d47c773ea50b096120689fdc77e64c7c84f6`  
		Last Modified: Tue, 08 Oct 2024 18:03:21 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu`

```console
$ docker pull spark@sha256:4a770909beb5f0862324256a618327dc1ec089a61097310f7a2cca52c547bc57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:891762f04c30f78c405be44042791bcbc11e64067471e60b9ce41c122fb341c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.3 MB (981277608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5d74fbe1151869102aa6ad0c2620f225feca28a067beaff7c853f545e8fda4`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219a986d1231aa063d9c872065d7fffffbfd239762088a20aa7fabbbc857bfc2`  
		Last Modified: Tue, 08 Oct 2024 17:51:47 GMT  
		Size: 319.3 MB (319310427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:40edfab0e3bcd546d3faf1a69d5b40f32ef553788e63168ca79e492ea2814c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18052147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861e5f6ad5873a7cc423c186ca49e2847aa8707c0883d468d156a896619b644e`

```dockerfile
```

-	Layers:
	-	`sha256:29d22dd42324d957588b5a7ffe92f08c742b26edd3366e54de5d7f38fbcd3488`  
		Last Modified: Tue, 08 Oct 2024 17:51:43 GMT  
		Size: 18.0 MB (18041397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2708f5c8d44acc149f22b91961a755a162a7af7450405dd1373cbb7506e665`  
		Last Modified: Tue, 08 Oct 2024 17:51:42 GMT  
		Size: 10.8 KB (10750 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:be1218562bc25999200fdade784c182cefd2cdec829137e848ec1a60d7f2ba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.3 MB (962269329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7674ddae9cfee11255a059e978fd66d0e27ac35a591050140592ee97c4a0525`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff6fdb1308fe94fdc86aadcb3a827b4fe607025a433850088a403e5af86f7b9`  
		Last Modified: Tue, 08 Oct 2024 18:05:52 GMT  
		Size: 302.5 MB (302478306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2dc11c62fcce02ab71d7d6ed9c1d70e72b2dc54b0d147f0eb99db4c38958ccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18018008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2306dacc7a5e1cc812455c889c5e2ab79187a3cdcff7384d83ab479c0ab4a7`

```dockerfile
```

-	Layers:
	-	`sha256:ec26f1f26e21b2b365915787a6f04303b2ec8d4cea37af743055cdb69a150619`  
		Last Modified: Tue, 08 Oct 2024 18:05:44 GMT  
		Size: 18.0 MB (18007118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:397e964336e9e440043637d747e271edad375b6f4d5f0409dda9c4e662cf77e9`  
		Last Modified: Tue, 08 Oct 2024 18:05:43 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java17-ubuntu`

```console
$ docker pull spark@sha256:cc025df34b1079ce9af860fefd120283a00a8034aa67e9e00c3c363622be6b74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0f32feb484b21a893e9f6104004a24d66ffc6d517bd637038c6f4e2739f74371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 MB (661967181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf237fb54677cd6ac7b5c942f8311002d9b7dab8c8764ac818076ccf3b880934`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad3b5e04f2c57070106a37d5d44429d29123ae69ff54b93f63c101129c298d9`  
		Last Modified: Tue, 17 Sep 2024 01:09:45 GMT  
		Size: 145.2 MB (145177133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e94d8e4bef4afb4cff24dcb435416fa3f42401c7ab9b0401e913516968373`  
		Last Modified: Tue, 17 Sep 2024 01:09:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21beeebd32c0abccb0b45e99a7fd283212bb21ac4fad10c36216455082df95d0`  
		Last Modified: Tue, 17 Sep 2024 01:09:33 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51cb1ae108610ef5f29e782111498aee52dc91ea77a6e7d7fe5aace3d31877`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64741316940b6c81e74490fd96342c2e4c72d74674da03dc0261bf9d848c3d2`  
		Last Modified: Tue, 08 Oct 2024 17:04:05 GMT  
		Size: 24.9 MB (24897046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b78ffd9955ecd8f657eaf189f9ae70078bcaa2c81fffa2d3a40a06ce007459`  
		Last Modified: Tue, 08 Oct 2024 17:04:17 GMT  
		Size: 444.0 MB (444031982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a16616650616ad881881bd4b1f82eedcd395e326cb98e2e9530ca07e69d0d8`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f3bfc9425877c114cac52976d4d894a140e43922baf8934d91722cdd9bc1820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4674511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8033d4c92415c11faed8d7139b61c62cee3c8237a869d3781956bfc60e5a590`

```dockerfile
```

-	Layers:
	-	`sha256:3f74df0ae6ca748112efb026e091581e0e3f1bd6f4719d4fa61761dc06783d38`  
		Last Modified: Tue, 08 Oct 2024 17:04:04 GMT  
		Size: 4.7 MB (4651545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdcfc41d1cda6f01434377f3d5c34802b3ec9d4c15d1c37c5242706b19eec82c`  
		Last Modified: Tue, 08 Oct 2024 17:04:03 GMT  
		Size: 23.0 KB (22966 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:986bae796005a635e45570203859d66701ec65d0fcafb13c16b95c097f885638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.8 MB (659791023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956ff0438aba713eebbc8fea28d762da1128f03ed056daebc389ba572eb37fcf`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c661676adabc448000bc17c531badb810755db643cdbd3b77bd5d6af1e70cea8`  
		Last Modified: Tue, 17 Sep 2024 01:39:32 GMT  
		Size: 144.0 MB (143967066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635213e63d52c04685322883d25f6bb5f35e17073ffdc3cb41b45cb406e5c0d0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb782c3b8f552eed1b4a6d0237ac6e9664eb6f27291f628c62fa4586b409055`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30368387f94e0824adaba56b0660977cc87282942e45383a2efaaba3ef6d441`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2b84b98d4649b34e2a70a417bee3d0fd5f1eebf375b97182ce9dbe97df59a`  
		Last Modified: Tue, 08 Oct 2024 17:16:36 GMT  
		Size: 24.6 MB (24561014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafcec38a1cb11cf79e1872188c1c03c6df1a685b98b97c52c808afccd16deed`  
		Last Modified: Tue, 08 Oct 2024 17:16:47 GMT  
		Size: 444.0 MB (444032003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c821c6e38dffa219df553a384837de060325b63c234e2e844e9579a092eb`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:58cfa5db985722ce2f8c5454f2a0a03853298c7e7468b57b469a58260b3163db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4770230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51edbecf3ced8529aeb0da628365cd8d837c25a58d2f8a1160596b010f574c39`

```dockerfile
```

-	Layers:
	-	`sha256:d9044ac8ea0138b904f8bfb194783cf00de54c74fcd5aeb9025c727a6966471a`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 4.7 MB (4747160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e18f4e13e638b0de8327794041a47b53a956959b8d0dc0de175c5246a1b42d8`  
		Last Modified: Tue, 08 Oct 2024 17:16:35 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu`

```console
$ docker pull spark@sha256:78a7cd58e6233fac0e02eb2c17b8d87902726577fcae954296819af0015ecf0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fd50e7ec9d7b33dcf1eb8c7fb37762b53a1144f88528b2ce7761105068264103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1009548227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb5c3fc6a1f8eee556767f7d407d922321c41335030e64be8edb2bb939480d6`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b4e8ef1e0bcbf79acf14d61b67025e4045440ed60d095bd0d93a3236d14480`  
		Last Modified: Tue, 08 Oct 2024 17:52:08 GMT  
		Size: 334.2 MB (334171180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:4f77423b388cfb7ef7223d649a65171ad63d3a6c4d0300c3c9470e7a97e35fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19067671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70923d37f3281857eb288da76c60cbfb02c7c19076aa913d7cdaa4d7ee2d0b77`

```dockerfile
```

-	Layers:
	-	`sha256:3ea408e2cfa5e4693fd22e2eb16f5795645e689fc9c7d190e2930fa7a3f3234d`  
		Last Modified: Tue, 08 Oct 2024 17:52:04 GMT  
		Size: 19.1 MB (19057062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7c61b52ba7a6654bc0f296f6571176640a699082c0311b0421092dae1f9dd6`  
		Last Modified: Tue, 08 Oct 2024 17:52:04 GMT  
		Size: 10.6 KB (10609 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5bcf9b35d325cafa9e5839211fad88ce58f2b86bbfe9ec456340136890e93f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.8 MB (989765494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c50076bb90956c63cf1b06572704711cc68b3833fb0aacf97d855ea0180f6a9`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ced34bbcef85b5cfd2c9abac66e5f84f2e5f9689d618429cbf9306c1847ae2`  
		Last Modified: Tue, 08 Oct 2024 17:55:44 GMT  
		Size: 317.2 MB (317184723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:35ef3894dde18c202b51e031f7d111cb082bff7392bb9b9f59a6f1b0386822a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19033532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c288ed9206450a2e6f3b8d89be522b6d02d627c7994d48f20cc1a80c8e611b62`

```dockerfile
```

-	Layers:
	-	`sha256:191d74f8f2d04f61d3b84eb375096731b021f0b5b34c23a979d8283b2c4b241c`  
		Last Modified: Tue, 08 Oct 2024 17:55:38 GMT  
		Size: 19.0 MB (19022795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292a751e5442da09289f01c654353eb903c951a42409c29b61bfc3d1269c7e0d`  
		Last Modified: Tue, 08 Oct 2024 17:55:37 GMT  
		Size: 10.7 KB (10737 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu`

```console
$ docker pull spark@sha256:1d473d5bf0a92b73d49399b432b39df10106d1e47f29b93ed317cc552a9c319a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fed179db509ff0aa53b34aec4fc973e7cb8b95d1e8c78db07437fd77ddd63e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.3 MB (789263662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0b7f7e66c7c4e2952eb0c807e61761ccb8b90c3cf1e01a30991b479ec1abc5`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678b2a0fa4a71c7d3ab106f08416a1a7b39d99295000c2b218b7b6c3d905010`  
		Last Modified: Tue, 08 Oct 2024 17:51:07 GMT  
		Size: 113.9 MB (113886615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:2aa98c06cffcb0eedecfa9ace3a77f0a1290a9867b0cc28adcc8a6013816e639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10030388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65911f109bfb4dc7c00bb9c665e2e729da68b9d4d9ce3fd86ae2c629e2aa03d`

```dockerfile
```

-	Layers:
	-	`sha256:7c6652b2b030ec087129c2966b211f578eafbc432b8200f798c941552cb5333a`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 10.0 MB (10019289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b65b37bb6d87571187821ad9c4cf2a3329c346daf71d33d542df0d37665148d`  
		Last Modified: Tue, 08 Oct 2024 17:51:06 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ceb67b1faa9783a0f68073a84dd49a1b9b3aa58d210783106e750581ebdf1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.0 MB (781013044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c515005990cfc759e075db2760b18a04252624bd55add8d23ec277c2edad8267`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4c36288f05e88c1aee71a937cec2ee7725195dbe65ea01f8c76c0f9641bf6c`  
		Last Modified: Tue, 08 Oct 2024 17:59:39 GMT  
		Size: 108.4 MB (108432273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:ea7249a94b6fda3ebd8f3ee1bc4407ba3636cd3c74f746062dd1e2505e82dc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10024975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87771b04fc2b04ab566f503ae73c3b982b27b60a26116220f8b761d10e703bc1`

```dockerfile
```

-	Layers:
	-	`sha256:0aa966cba350c6e99f3ed53d1f3dff980b4589ca4660aef1f03c22f052f2f1a6`  
		Last Modified: Tue, 08 Oct 2024 17:59:36 GMT  
		Size: 10.0 MB (10013724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0944ac5fa1553d27f2631a22278f5914c73628ee68e8d6ed6b12a27a06f1dc`  
		Last Modified: Tue, 08 Oct 2024 17:59:35 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu`

```console
$ docker pull spark@sha256:ce87d49f9944116903caf5d5cfc8b2c37e500e75b611030c6c50b6cc750cec0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:475f5ac65fc99f695bdc8fc16ef367a1a1f912f2b96ba8b756f1198432afbfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.7 MB (994687057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d772cf7424b4d16692c0dcb86a91469b72f37360601db35bb076871afddb34c`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e249da86e5aa3603d8b89acd4e889efa846e2253fc4acc4131f5d0947bcfc426`  
		Last Modified: Tue, 08 Oct 2024 17:52:11 GMT  
		Size: 319.3 MB (319310010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:d100ac74f90c8dbbf8d54abe562daf697f0fcf76f145f50d91b08ac411b46801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18055915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525ea80313d696f5b1f9fa0bec5bb23558a58506ba358b98f22dbce8c2728600`

```dockerfile
```

-	Layers:
	-	`sha256:9944ff5d2bb611690a7d7ff98da7c6308b6caecf24368f18bb79624b6157839f`  
		Last Modified: Tue, 08 Oct 2024 17:52:04 GMT  
		Size: 18.0 MB (18045152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391b3fdac6f29ec9a0a7a821ff9038aa7a4d7318e8d3175e4235eefcc1e00342`  
		Last Modified: Tue, 08 Oct 2024 17:52:03 GMT  
		Size: 10.8 KB (10763 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:d95740553864c92ca56ef19728672748fff6d81337b38062b6ed98c3a3310ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.1 MB (975059663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdaf7f86e5395349e8ce28fcdbbe3f9e3460e7e899a6570ee8183221b4a9d20`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a9568d4e54c351aa7f7961a4fe84c432b25049ab18b723a8df506ee38e931`  
		Last Modified: Tue, 08 Oct 2024 18:02:01 GMT  
		Size: 302.5 MB (302478892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:deb666ab30d479a81217bd70a36a26a1dca8282e6e49e3b5032a6547a859f6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18021776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fa7d92eb52130a5579d0e89ec51b9390b030a702c329eeb3e74de76d809140`

```dockerfile
```

-	Layers:
	-	`sha256:58c2faecd05266f5828b21d0ced072f26fcfee95047826cb2be0f8059fcf2aad`  
		Last Modified: Tue, 08 Oct 2024 18:01:55 GMT  
		Size: 18.0 MB (18010873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6fa15c8ab702a9db724600ae307afbf8b68d9a52087f318ca9454530496e74`  
		Last Modified: Tue, 08 Oct 2024 18:01:54 GMT  
		Size: 10.9 KB (10903 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:4.0.0-preview2-scala2.13-java21-ubuntu`

```console
$ docker pull spark@sha256:0d3efee40e3ee5e57fafd123f3e12ddc10dba0e446b585afbfa97a2b632fc156
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:83eb94329e41afa2f20bc6883b36b5c19dc3da6f147500a8a129aedc07b78a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.4 MB (675377047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c379b3916e88d7e79b48177f9fee4a858c1e3412ea527ab6bbfc67dadc8fde`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf49cabfbfcba18d6177c1ac6c7e9330c15d3d20cbc4f88c58bd335ee450a2`  
		Last Modified: Tue, 17 Sep 2024 01:09:37 GMT  
		Size: 17.4 MB (17415206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54db4c1f9d6f27ce90c36e7cca40ed5e610e955177b38bf3736402c34ab97f`  
		Last Modified: Tue, 17 Sep 2024 01:11:02 GMT  
		Size: 158.6 MB (158586989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b36951be918d275edab9841778b60a027cf70933e18d5b9e7732a45361f011`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70236bb1740c337b4db2c3418c657bc84ce3be0091e9c0bdcb8382d808d7f1b`  
		Last Modified: Tue, 17 Sep 2024 01:10:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcc3c1ca9b1e2332e604effcd303a4048660f2cb27d625efc72ed598998fae`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3241a579ad8df6257d5878807f066ce04688da184da122eb7f7df77bed2a017`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 24.9 MB (24897054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca52f721e7ff5b79306fe678125449bb8c45e38036c24f351147ca4e15e2a4`  
		Last Modified: Tue, 08 Oct 2024 17:08:55 GMT  
		Size: 444.0 MB (444031980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7610c8e311c387211f0dab29bb637bb924c49b061c57352ea23492ed5d5b30`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 2.1 KB (2134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:61104ede3535131a70bc8114cb63b209a7b8dd8c4c33acd0f20a8741b2bf62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de834e4d1a0fd899c07753d088e09a06ccf9fe581fcbc439ae815dd1690598`

```dockerfile
```

-	Layers:
	-	`sha256:fbd98e9b9b3ef15666b50493b8f9c118038166f8b17e4672eba64a703411047c`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 4.7 MB (4655300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4809721de48427d1b304287ba343c18edc347c84c3ebb78156012960d2dadc47`  
		Last Modified: Tue, 08 Oct 2024 17:08:48 GMT  
		Size: 23.0 KB (22977 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:f9c11a10b16f916cc7517bc05de253cf8c81885ca4b6697df17cddfbd331b619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672580771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd9a932563c0437ca41152681c8711583c6000dab64276f741b6c81ee77cb72`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c08aee9ece74cacae8ca7dfbcf838605c1e8bf9ae4ef62a9bf1d407ca7dd`  
		Last Modified: Tue, 17 Sep 2024 01:39:26 GMT  
		Size: 18.8 MB (18827958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09549a3282b55b43a30b2d6c2beb9e1411a150ea79cf36555e24ceb3cae93826`  
		Last Modified: Tue, 17 Sep 2024 01:40:38 GMT  
		Size: 156.8 MB (156756708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054d5ba84160b816d15d0d2cb12d6f3ddadc08fd115816d88b7e3d349bf642`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4200e9aedb221f093343029d18baaf7a7a6524ee64058044795320f8d236c`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3eb7121b4ffed7a1dbe4550db5fe37342d67ba3132b0ea6828ace592941adb`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e983fb3eb794776519eb3df50faf2338f0f37fe84b2ce113653768f59aa781e6`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 24.6 MB (24561083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b01b87f822b53fd562ef2b4cc02620a3d89d079c76582af5049c0325f311d`  
		Last Modified: Tue, 08 Oct 2024 17:13:52 GMT  
		Size: 444.0 MB (444032036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce314ee4a6f192d6fb9286bac40116926fcf5243ca7cc1a52884dd31a39cf0c`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:4.0.0-preview2-scala2.13-java21-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:29b423a2f9f0814bf9de2efa4dffd2265ae8eadb23adcccdd1b88e29e3640a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4773996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d855dfee88cbc62dac473e2bbe43e2a00a4ce001639f75ad5debb3e9392d51`

```dockerfile
```

-	Layers:
	-	`sha256:38e61672a9c2550e241443a99c4ad1829ef64ae2d3532549c8f8a9d15b039ae2`  
		Last Modified: Tue, 08 Oct 2024 17:13:44 GMT  
		Size: 4.8 MB (4750915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa1724d40b35092b53ed1ca87952e8be4c5d4ca569eed1e8512dadb8dfb0e1f`  
		Last Modified: Tue, 08 Oct 2024 17:13:43 GMT  
		Size: 23.1 KB (23081 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:latest`

```console
$ docker pull spark@sha256:a52c6fd30c051c9bd67e05731642c3c509c7897013e3a630e74540ca781d7eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:391d7ee2ac9edce7e60d43cd4b303d44d02ae531e4811e472745f1560c2c0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535866963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2006195df41288bab7acbc48f4badc9e9a5fc52eaf51e9b0252023f7a889d20`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cc6bda7d77b09c1fdbf1646b4ae18ae979b295bd43d9d8a69a66bbaf18c9fa6e`  
		Last Modified: Wed, 02 Oct 2024 03:58:16 GMT  
		Size: 94.4 MB (94372377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:be2dabf8fd5f36e0049765a327f6c6b1d842ca9fb4b5d381f8a70a59b138684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f149a5a8cd6bd591e611a15f3fc107df199f42f622e15576caf95844d3529f`

```dockerfile
```

-	Layers:
	-	`sha256:c22a02684770691bf7e3bb725182ad05f8e991cfa66c238219efdc89c1268dd1`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1d208f1f141f4f282ea9ce9bac68b86fc2a4490f281ac3b62dc614f6d81b25`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:28e0eebfd7cb6484ce4bc0b1098ae92212f04a9a2aac055d55ad54154262c336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525383383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612aae4775d87dc5a751acecfe1b018e4196bd88b2396d50bbba5b232dde9cc3`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e74d847c76e29fcfbe9e81cc2b82008d4f4fc8fe71df47b58fa08bbed0328d`  
		Last Modified: Wed, 02 Oct 2024 06:17:47 GMT  
		Size: 87.3 MB (87330562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:4e726c55f4acf3bbbb9e4d59a7a30625fd79d47b7e88399702d41fb9937c3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92ed320fe2d5040ab7e2e23705a5aa612d898a90ec39eff146727bbbd24333`

```dockerfile
```

-	Layers:
	-	`sha256:6fd01b175fc4817adaa8c121d905e2618ced1b5af5f5e98348edb1ce3cfdbdd1`  
		Last Modified: Wed, 02 Oct 2024 06:17:44 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a477ffffd67ff71e047f2809d5cb220aa5a1c51dc79dd6525104f82a70ec08`  
		Last Modified: Wed, 02 Oct 2024 06:17:43 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:a52c6fd30c051c9bd67e05731642c3c509c7897013e3a630e74540ca781d7eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:391d7ee2ac9edce7e60d43cd4b303d44d02ae531e4811e472745f1560c2c0232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535866963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2006195df41288bab7acbc48f4badc9e9a5fc52eaf51e9b0252023f7a889d20`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cc6bda7d77b09c1fdbf1646b4ae18ae979b295bd43d9d8a69a66bbaf18c9fa6e`  
		Last Modified: Wed, 02 Oct 2024 03:58:16 GMT  
		Size: 94.4 MB (94372377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:be2dabf8fd5f36e0049765a327f6c6b1d842ca9fb4b5d381f8a70a59b138684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f149a5a8cd6bd591e611a15f3fc107df199f42f622e15576caf95844d3529f`

```dockerfile
```

-	Layers:
	-	`sha256:c22a02684770691bf7e3bb725182ad05f8e991cfa66c238219efdc89c1268dd1`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1d208f1f141f4f282ea9ce9bac68b86fc2a4490f281ac3b62dc614f6d81b25`  
		Last Modified: Wed, 02 Oct 2024 03:58:15 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:28e0eebfd7cb6484ce4bc0b1098ae92212f04a9a2aac055d55ad54154262c336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525383383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612aae4775d87dc5a751acecfe1b018e4196bd88b2396d50bbba5b232dde9cc3`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b9e74d847c76e29fcfbe9e81cc2b82008d4f4fc8fe71df47b58fa08bbed0328d`  
		Last Modified: Wed, 02 Oct 2024 06:17:47 GMT  
		Size: 87.3 MB (87330562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:4e726c55f4acf3bbbb9e4d59a7a30625fd79d47b7e88399702d41fb9937c3b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92ed320fe2d5040ab7e2e23705a5aa612d898a90ec39eff146727bbbd24333`

```dockerfile
```

-	Layers:
	-	`sha256:6fd01b175fc4817adaa8c121d905e2618ced1b5af5f5e98348edb1ce3cfdbdd1`  
		Last Modified: Wed, 02 Oct 2024 06:17:44 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a477ffffd67ff71e047f2809d5cb220aa5a1c51dc79dd6525104f82a70ec08`  
		Last Modified: Wed, 02 Oct 2024 06:17:43 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:0281d18704a625043b07302fda6dd29f1ee674a9ce963a6c8e7f783ee0f5b527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:acf631a8aab38592f57500fbf086f8e4525b09103462870748843b4dab5d4552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558595184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb3e8d9a352699ae60d342762e83f7dbfdcd8c7e1e1cdb46f3380d35df77577`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df305000fbec477485e515186aabb3372b1a9b994d52bd431e695f5fa50152`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e5fad812f6ba27459f731fab613283e06c341585c71a03066b8e605cf140de`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 24.9 MB (24895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebb93eadeafabbecaf3a1c383286da49bd41b99c976e1fb2a8fcdb4c0db105`  
		Last Modified: Tue, 17 Sep 2024 02:00:48 GMT  
		Size: 324.8 MB (324826635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a17223d4a80593b45d2127704365cb3e8e596c1a1a4bcc88e1db51ecc8c15a`  
		Last Modified: Tue, 17 Sep 2024 02:00:43 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53761970764de3460089e38f86d2b14457eafdafb6b7d5761e37f0c0be82107`  
		Last Modified: Tue, 17 Sep 2024 03:01:58 GMT  
		Size: 118.3 MB (118276396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:5c4e1a1731e2e5d3867d004d76e27450a48f8627fe80d9a06dd6ef7e2376f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9749768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6495a9cba2f7e3026788357dfacd4fb665e9dffc0b80c711297f3375920e8b`

```dockerfile
```

-	Layers:
	-	`sha256:3198ea97f5b615fc32c52fd831013f85c733326f9679222b8ba1db2054801b21`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 9.7 MB (9738492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbef3e46342ea6a466308252abf8c82fdb11ee2f2534b872666af608020bb055`  
		Last Modified: Tue, 17 Sep 2024 03:01:56 GMT  
		Size: 11.3 KB (11276 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:2d72a89414cdb91f8c47743c51d53eb50c24c9ba738a193b90f515511da0ae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd93d2430a0359673d152eb4432c6aa60b4f053f06f7541a803d1bc9c1d4d319`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Mon, 12 Aug 2024 09:09:28 GMT
ARG RELEASE
# Mon, 12 Aug 2024 09:09:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 09:09:28 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 09:09:28 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 12 Aug 2024 09:09:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 09:09:28 GMT
USER spark
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb68f82e18a7dcbd3a312441dd3aa2436ae26b4b8118f534d771ef38d93ef9`  
		Last Modified: Tue, 17 Sep 2024 06:46:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df33fd2c3ef016a654822082cb26ba64f432e71656c444b4d1a057b005e7d3`  
		Last Modified: Tue, 17 Sep 2024 06:46:28 GMT  
		Size: 24.6 MB (24558471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7847a8fd0f9aa486a4efe5383625545b85c98fbe3faf9a909f3a6d8d78ffe8b`  
		Last Modified: Tue, 17 Sep 2024 06:48:18 GMT  
		Size: 324.8 MB (324826627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb987a504fb242058870eebf4e2ce9d2b6d46d541fb09ad46f6b7b805b24345`  
		Last Modified: Tue, 17 Sep 2024 06:48:10 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53071672103a9f73c7d180c542245f7fbe79ffbcd09a50eaf7e500a6ea948971`  
		Last Modified: Tue, 17 Sep 2024 08:41:45 GMT  
		Size: 114.3 MB (114298029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:9dc8a1114306263783eef8cc8958882cb92fe2e1010e6022b1695ba0c2905c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9745277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acac5f0e510e8a6bb5acfade884ca55b315d36173e6b33cb739fcb697c77c50`

```dockerfile
```

-	Layers:
	-	`sha256:43712af2d49acf91396c3d2ee0de5dd9e2e0f3c7ddabbfe2dafd8ba8334b174f`  
		Last Modified: Tue, 17 Sep 2024 08:41:43 GMT  
		Size: 9.7 MB (9733558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d024ea648d2dde5d7c35203974bc7b9cd985df0a50b6f6bdac79a5a350be59`  
		Last Modified: Tue, 17 Sep 2024 08:41:42 GMT  
		Size: 11.7 KB (11719 bytes)  
		MIME: application/vnd.in-toto+json

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

## `spark:scala`

```console
$ docker pull spark@sha256:b03fbd56c502308f012e20e30573de899609b854d41f6a26b5dac6da34fc0928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:d2904426f936daaead9c83f9f6660956ea69fda8f2d98e90aeb6d273c4261636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441494586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376d88654452d8ff164d8e696df69e82e5149b98adaa418b00afbe73e48850e`
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

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:c28d0d371311829e42eda9ed5cc856929a928746437b69093de687043da92c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4323752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9aebca05865f4fcf28cc2406dae3c169fc44a2635b530529984fc9fa26a860`

```dockerfile
```

-	Layers:
	-	`sha256:90c594b9c58dd9d1842f1155e124d6bc743adebaf58867d50cf4a2795d440354`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b38f2527244efd5730d0e3db88c37b79ff3ed88978a06cd25505901d744a688`  
		Last Modified: Wed, 02 Oct 2024 02:59:56 GMT  
		Size: 22.7 KB (22706 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5b7e31e8af65104f9ef770a8c201be68a2eacef2ed2eb07ce64c6bde72b07563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438052821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa4e36aa2a158f51cb6f78b884d9ab22b4b36417113978aab64e36b78db59f`
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

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:8af255ae39c7ec0d21a93e109b6412dd2f62cac4a1711436a716d6511db0c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde7eb4dd1d70b933df0b090fbdabe343282586eae2350bfb7138f93ae4caa4`

```dockerfile
```

-	Layers:
	-	`sha256:63b452f90f3f3590905d0b8c9f2a876dd1b1bb5d1cbbf42e58dd0f8718c7afb1`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:396db8a2cd553d11ea1095a60d4956c130bc9e78af6dc9fbf81369077eeffadf`  
		Last Modified: Wed, 02 Oct 2024 04:16:28 GMT  
		Size: 22.8 KB (22822 bytes)  
		MIME: application/vnd.in-toto+json
