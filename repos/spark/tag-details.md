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
-	[`spark:3.5.3`](#spark353)
-	[`spark:3.5.3-java17`](#spark353-java17)
-	[`spark:3.5.3-java17-python3`](#spark353-java17-python3)
-	[`spark:3.5.3-java17-r`](#spark353-java17-r)
-	[`spark:3.5.3-java17-scala`](#spark353-java17-scala)
-	[`spark:3.5.3-python3`](#spark353-python3)
-	[`spark:3.5.3-r`](#spark353-r)
-	[`spark:3.5.3-scala`](#spark353-scala)
-	[`spark:3.5.3-scala2.12-java11-python3-r-ubuntu`](#spark353-scala212-java11-python3-r-ubuntu)
-	[`spark:3.5.3-scala2.12-java11-python3-ubuntu`](#spark353-scala212-java11-python3-ubuntu)
-	[`spark:3.5.3-scala2.12-java11-r-ubuntu`](#spark353-scala212-java11-r-ubuntu)
-	[`spark:3.5.3-scala2.12-java11-ubuntu`](#spark353-scala212-java11-ubuntu)
-	[`spark:3.5.3-scala2.12-java17-python3-r-ubuntu`](#spark353-scala212-java17-python3-r-ubuntu)
-	[`spark:3.5.3-scala2.12-java17-python3-ubuntu`](#spark353-scala212-java17-python3-ubuntu)
-	[`spark:3.5.3-scala2.12-java17-r-ubuntu`](#spark353-scala212-java17-r-ubuntu)
-	[`spark:3.5.3-scala2.12-java17-ubuntu`](#spark353-scala212-java17-ubuntu)
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

## `spark:3.5.3`

```console
$ docker pull spark@sha256:f9632407249cc8b4d3e889e86b6df17e85c0e6cb24ea138eb440c408a4f95e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3` - linux; amd64

```console
$ docker pull spark@sha256:fe6222480d459e09a546e0f23facb7ceb2da5aa3fbc4c751556d3b601e3ce735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535909762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157f30b6c76c836b874ee482f7579478aff604f19149117a44e4245f398ad93`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22faaabba23eb151412e244d9f07351a2536bd6379069915f5a190b158d470`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 94.4 MB (94373216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3` - unknown; unknown

```console
$ docker pull spark@sha256:47b8ee21a8339c70023b7b27196932d3bd46557144736c6355a53b4c7af46f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da073156fbd1c48888ab3e38c9127edf9e7a3a6c0599bd77647a07d5a447a57f`

```dockerfile
```

-	Layers:
	-	`sha256:e88cd75ff8b3fc07be0a67c81d7692f335870729b18eede09defa26dc30e5ea9`  
		Last Modified: Thu, 10 Oct 2024 17:50:35 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d943fa4dd5eb865fd6b0b6f8fe8e96e57dde593dd66f3421df9348997731ece1`  
		Last Modified: Thu, 10 Oct 2024 17:50:34 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cc88b9b7dff73d804b684f2148d8fa22e4f184c8af9d7bac6b2b6e0a27bf3887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525424754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c0f60b3fd8a1c3eb7ee05625e184e93296e1181b879a13bd197f3c5075404b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834e25b1fdecf400ed4c97e4303666572437c4e246679754f7ee6c25ce0c5a5`  
		Last Modified: Thu, 10 Oct 2024 18:01:55 GMT  
		Size: 87.3 MB (87330002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3` - unknown; unknown

```console
$ docker pull spark@sha256:a199d5a0a336f948129f9634ea7ad3132ca4c12a4142242f40237894ccbfdd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a83d9152b13a75ecb34d76666c6e32e2447f3a4027938849d7a8c794dd9c9a`

```dockerfile
```

-	Layers:
	-	`sha256:08fbf8ecd311e701ecbdc6e7dd1aa94eb6f922f69839eaa447c475f8516f7f33`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c54d20ead64ba8c4c871d1d7b31c1c52975e1ba1737998193765cf162221f6`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17`

```console
$ docker pull spark@sha256:15fd585bd079757bea4b95d32156f3c9c2aa65ad4569a98b8f60d03bb3e09f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17` - linux; amd64

```console
$ docker pull spark@sha256:45b46e330c1ad9a13c069ee4c6d6cf8a90dfe80eeef91b79c3f3c30a23f22a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.7 MB (656691105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b578b1aabc200732eb84fa21de9f835eca39f491c6f0b84163212c939c2ad6b6`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0664f69259dddc403e624d449dcec1834771d756f72768daab7d705813bc72`  
		Last Modified: Thu, 10 Oct 2024 17:50:39 GMT  
		Size: 113.9 MB (113887291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:f6e28bdb4cb5d62ce310359b7584ef422b69d69985fc201e48e365f1a518d09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80d64de68c00422f14d9610bc0867bc064da5980378a35a42b70431d1137860`

```dockerfile
```

-	Layers:
	-	`sha256:3c8c89cb79640af82d8d7cfeb005cfe1aa956b93824fd40aa78e9f8e5612aa14`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 9.9 MB (9888571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a2c6774e534bde5335ca7a0207e90ac1e28bc4c8c94519126da1fc76ae074`  
		Last Modified: Thu, 10 Oct 2024 17:50:36 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:150cdde64ab677a2df5594a55360de116f9a1329d4e871e3529e96791f484381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649059495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21247e8844b41c4799aec04308838509c6643738ecfc2b20bb25fb003c4fe327`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7cd4ea97e9d886fc3526508027981465b1f7a9a95d852fb94b55e5e4615bc`  
		Last Modified: Thu, 10 Oct 2024 17:58:40 GMT  
		Size: 108.4 MB (108431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:e476248bd888d0ddb22c4be5322efbf617c973bbabfaf46819aaa1e6a0f6f942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c0d37c05374dd3a64168f1a671606da6a31ce3a73dd6bbf1f0793f0ecbf1ac`

```dockerfile
```

-	Layers:
	-	`sha256:8e2874da8a7497166ff6427ddf2be01490b0ed58997a8a60ec8e7d4c71debc16`  
		Last Modified: Thu, 10 Oct 2024 17:58:38 GMT  
		Size: 9.9 MB (9883018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29817cb171189faf238e212ee6415e46ceae76f58965f3f1c3a853cdb286f102`  
		Last Modified: Thu, 10 Oct 2024 17:58:37 GMT  
		Size: 11.4 KB (11447 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-python3`

```console
$ docker pull spark@sha256:15fd585bd079757bea4b95d32156f3c9c2aa65ad4569a98b8f60d03bb3e09f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-python3` - linux; amd64

```console
$ docker pull spark@sha256:45b46e330c1ad9a13c069ee4c6d6cf8a90dfe80eeef91b79c3f3c30a23f22a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.7 MB (656691105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b578b1aabc200732eb84fa21de9f835eca39f491c6f0b84163212c939c2ad6b6`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0664f69259dddc403e624d449dcec1834771d756f72768daab7d705813bc72`  
		Last Modified: Thu, 10 Oct 2024 17:50:39 GMT  
		Size: 113.9 MB (113887291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:f6e28bdb4cb5d62ce310359b7584ef422b69d69985fc201e48e365f1a518d09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80d64de68c00422f14d9610bc0867bc064da5980378a35a42b70431d1137860`

```dockerfile
```

-	Layers:
	-	`sha256:3c8c89cb79640af82d8d7cfeb005cfe1aa956b93824fd40aa78e9f8e5612aa14`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 9.9 MB (9888571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a2c6774e534bde5335ca7a0207e90ac1e28bc4c8c94519126da1fc76ae074`  
		Last Modified: Thu, 10 Oct 2024 17:50:36 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:150cdde64ab677a2df5594a55360de116f9a1329d4e871e3529e96791f484381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649059495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21247e8844b41c4799aec04308838509c6643738ecfc2b20bb25fb003c4fe327`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7cd4ea97e9d886fc3526508027981465b1f7a9a95d852fb94b55e5e4615bc`  
		Last Modified: Thu, 10 Oct 2024 17:58:40 GMT  
		Size: 108.4 MB (108431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-python3` - unknown; unknown

```console
$ docker pull spark@sha256:e476248bd888d0ddb22c4be5322efbf617c973bbabfaf46819aaa1e6a0f6f942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c0d37c05374dd3a64168f1a671606da6a31ce3a73dd6bbf1f0793f0ecbf1ac`

```dockerfile
```

-	Layers:
	-	`sha256:8e2874da8a7497166ff6427ddf2be01490b0ed58997a8a60ec8e7d4c71debc16`  
		Last Modified: Thu, 10 Oct 2024 17:58:38 GMT  
		Size: 9.9 MB (9883018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29817cb171189faf238e212ee6415e46ceae76f58965f3f1c3a853cdb286f102`  
		Last Modified: Thu, 10 Oct 2024 17:58:37 GMT  
		Size: 11.4 KB (11447 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-r`

```console
$ docker pull spark@sha256:51559788ad1d9a9dcb202e0b6ea9b4bdc256d94056d55ae9ae2baaefba9e9e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-r` - linux; amd64

```console
$ docker pull spark@sha256:bc0042179ecc589a16f7cc932022c68bc39319bb428dccf9d30a9e7a060dcf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.1 MB (862113442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da9f733f36c7b4adfbf0703f197723e348b5112291670ee2795e339004c0806`
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c130b12258fbe67cb351cc36dd3628adc8380c15149c13b1a2858d408f2e95`  
		Last Modified: Thu, 10 Oct 2024 17:51:26 GMT  
		Size: 319.3 MB (319309628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:bcc42ba94f61f1c0c13c77922f548fb376590a9706e493f3eb9db8cb4d9a67b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17924792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4312eca0395866eb277fbded0f890ac4bef52d73c90db509d6998227c3278150`

```dockerfile
```

-	Layers:
	-	`sha256:e77f1313a8b577ad9581e39c202190d7a5e12cdd54427eac77e6284f26dd0317`  
		Last Modified: Thu, 10 Oct 2024 17:51:21 GMT  
		Size: 17.9 MB (17914140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43550b113405e9c8847397db471f66b01f1cbb2adc12d9959d0f725465cdd95c`  
		Last Modified: Thu, 10 Oct 2024 17:51:21 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:771af0da2711d25b41f9751e640c5b91f763fc736b1549889079487d03736f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 MB (843106891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cc8a5a33b83f1f115374196db41932a9b4f2d5cbf0b0181f10155a32ed118`
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f096e6c54686da60760a9569ab5facf860749535c002e2c21de1bd3ca17847`  
		Last Modified: Thu, 10 Oct 2024 18:00:54 GMT  
		Size: 302.5 MB (302479325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-r` - unknown; unknown

```console
$ docker pull spark@sha256:60764fc7a7235f409a8eda79b0f0f93b61053af6c5c4a76b564393376bfa3254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17890654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b91ae301b4fb43881a399ed481d5a80242746e361c217afc90f6abe3e384b97`

```dockerfile
```

-	Layers:
	-	`sha256:3228f8de36649929832282605e04ed7de312d9c092f6f00fe0112149cae783a1`  
		Last Modified: Thu, 10 Oct 2024 18:00:47 GMT  
		Size: 17.9 MB (17879861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f5b3d2de8a8669d565f24cd2cd968f611d0a6f0f8d9d1acb1ff1b893feb041`  
		Last Modified: Thu, 10 Oct 2024 18:00:46 GMT  
		Size: 10.8 KB (10793 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-java17-scala`

```console
$ docker pull spark@sha256:932058bc6de36f513383244a3b66df8b002f719c6fb1de87ace58484b2402052
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-java17-scala` - linux; amd64

```console
$ docker pull spark@sha256:554187eefc46a16620714e0d3ec45913b6cab6151bbeb2a82de6da5f1b893003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542803814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4bfbcc24a0230566b6f0d0f3699661aaaa4c3aae8191b97a93af91a128460c`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:f76fd50070bafba195836260047b26fb37155c0fa81db54105aa3684eef549ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4547120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d945b649bc4735a7a18ff29156798d998f3ce0c46e2e9e71dfc3298d528f9852`

```dockerfile
```

-	Layers:
	-	`sha256:6d7e02d7413a7a6b77abbe0d53e6b29246a7e8590320f8cde635f3eb1ec163ff`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 4.5 MB (4524288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7feb9145fc932e1d0e86f2ee1ed05f200bdd20b94bed9eb3607da382988c9f`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 22.8 KB (22832 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-java17-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:76ff7dce22dae9397b9ca9ffcec68a6e300c7785a7e3d78d9c0963d6469c459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.6 MB (540627566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ed409e77bd89735c98a6385658126752c8590c7205dbb97a3af3b10db8b1ff`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-java17-scala` - unknown; unknown

```console
$ docker pull spark@sha256:696d7b3a5d11e26ab1910e9a4add00fe82929305c5b1c65eaa056ed734b92244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632cd49f3194cab7f06680a9af698a2f621c7b742acda24738c7aae7826d088`

```dockerfile
```

-	Layers:
	-	`sha256:ee8076eea28c81b43cd9d6b3b8ba7bf35eddf69076fa22c940d9f047d5a03050`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 4.6 MB (4619903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a73d62ef6f28ee89f05c7cd116751885b3258a0e517ab521966ef6016b8698`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 22.9 KB (22937 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-python3`

```console
$ docker pull spark@sha256:f9632407249cc8b4d3e889e86b6df17e85c0e6cb24ea138eb440c408a4f95e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-python3` - linux; amd64

```console
$ docker pull spark@sha256:fe6222480d459e09a546e0f23facb7ceb2da5aa3fbc4c751556d3b601e3ce735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535909762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157f30b6c76c836b874ee482f7579478aff604f19149117a44e4245f398ad93`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22faaabba23eb151412e244d9f07351a2536bd6379069915f5a190b158d470`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 94.4 MB (94373216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:47b8ee21a8339c70023b7b27196932d3bd46557144736c6355a53b4c7af46f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da073156fbd1c48888ab3e38c9127edf9e7a3a6c0599bd77647a07d5a447a57f`

```dockerfile
```

-	Layers:
	-	`sha256:e88cd75ff8b3fc07be0a67c81d7692f335870729b18eede09defa26dc30e5ea9`  
		Last Modified: Thu, 10 Oct 2024 17:50:35 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d943fa4dd5eb865fd6b0b6f8fe8e96e57dde593dd66f3421df9348997731ece1`  
		Last Modified: Thu, 10 Oct 2024 17:50:34 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cc88b9b7dff73d804b684f2148d8fa22e4f184c8af9d7bac6b2b6e0a27bf3887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525424754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c0f60b3fd8a1c3eb7ee05625e184e93296e1181b879a13bd197f3c5075404b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834e25b1fdecf400ed4c97e4303666572437c4e246679754f7ee6c25ce0c5a5`  
		Last Modified: Thu, 10 Oct 2024 18:01:55 GMT  
		Size: 87.3 MB (87330002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-python3` - unknown; unknown

```console
$ docker pull spark@sha256:a199d5a0a336f948129f9634ea7ad3132ca4c12a4142242f40237894ccbfdd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a83d9152b13a75ecb34d76666c6e32e2447f3a4027938849d7a8c794dd9c9a`

```dockerfile
```

-	Layers:
	-	`sha256:08fbf8ecd311e701ecbdc6e7dd1aa94eb6f922f69839eaa447c475f8516f7f33`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c54d20ead64ba8c4c871d1d7b31c1c52975e1ba1737998193765cf162221f6`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-r`

```console
$ docker pull spark@sha256:1a59cf771ed941c79f5806fa97bffe25dececa3bb375e742db14101c9139df30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-r` - linux; amd64

```console
$ docker pull spark@sha256:120d5b971bb083abb0a19d7b2d35b6a530c2dbf2b7c6dc1de3ec0ebd4dd0e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673835815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046bd7ad09381484ae4dcdaa1e77b77b5b2b50ea91a80abcb457e4419fcccfdc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ec65aab84c9d063fafcab6440221038b276f48f7ec7f279d4cff91ea879fc`  
		Last Modified: Thu, 10 Oct 2024 17:51:03 GMT  
		Size: 232.3 MB (232299269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:99980c1561759bf1b3158631466eb82eef0b65d0bcd5f9504ff70e1ac04c5a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11189423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285a766f5770c129be758b6c6b603d4a323203430e5a01238e9130e1aa519c0`

```dockerfile
```

-	Layers:
	-	`sha256:d4c9726585014b5dbaf80dca3642fde69cf3f4ad6438e8f767e191b9af4cefba`  
		Last Modified: Thu, 10 Oct 2024 17:51:01 GMT  
		Size: 11.2 MB (11178500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9383401e0e16a27f0a7ad8551bd6d456e2a129177cea97435f88441f45df81`  
		Last Modified: Thu, 10 Oct 2024 17:50:59 GMT  
		Size: 10.9 KB (10923 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ebcb1944e4cd26537f3991c3a4d1d91fb726a18d8e986fb45a3ace9450085af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651603751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e106ef8fcf83084297feb9f84369bf27087f997532ca0a8f95568945ce6505a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e5784522b120123ce82c87564ac17c54e1c9ad3f25c849b145ace886e5af2`  
		Last Modified: Thu, 10 Oct 2024 18:03:37 GMT  
		Size: 213.5 MB (213508999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-r` - unknown; unknown

```console
$ docker pull spark@sha256:be936d3ccfb8840dba070cc9faa8c3a800804a720b20b7f63549453b7b276f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11174026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c94e08d7243d1b98042da8160277491585cbee6e313fa074c2daaa5388d5cc3`

```dockerfile
```

-	Layers:
	-	`sha256:35d65347af080febae54fb710ba2dac35e4b0a4fc06242fcc6922f1bc475d1f9`  
		Last Modified: Thu, 10 Oct 2024 18:03:32 GMT  
		Size: 11.2 MB (11162951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252ae9b7292a410118277a97d2eabb2c8a44dbcda97f1f2f21eee44e68db45dc`  
		Last Modified: Thu, 10 Oct 2024 18:03:31 GMT  
		Size: 11.1 KB (11075 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala`

```console
$ docker pull spark@sha256:e8877d2e8140931649910eec3bc45042665467423a0a8cd294624a1b341a4f85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala` - linux; amd64

```console
$ docker pull spark@sha256:32ce1aa7d3d75f1c0d1c217e85017e5d11a95d68ee5cec5bc071736c6a8c5b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441536546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336f1c2ab53718832db7c723b320ab9ffc54efe57ec1d64b16edbe32b8c6535a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:90a4018752845e0f4594b403b46674ceb032679e525bb9c6fb1f38f4c0d70877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6f4ffab80da12d02458adcc6dcf145d0061f6b164e86f005bb4d6758d79604`

```dockerfile
```

-	Layers:
	-	`sha256:d780b92754f75ef32015189ce89011be4a7f197b27a12b2962fe0a8516b9cba9`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be458b2b8b65ba413fb3f25b6d8511c07fe87f9c299261aad4f2e5f780adc919`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 23.1 KB (23127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fe2510cee6f908606bfd7f6d73e25b46d7ed5339b78b1986781f99e77c37fd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438094752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9add04dfea1fee747d00b8612bda54b4cc72fb2511361d3a5041955ac34f3e3b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala` - unknown; unknown

```console
$ docker pull spark@sha256:11a7adadcdfa8d589093ba60954637aef6a049a2b5630ca5aaafa4197d262b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9db13bcd33be01e09ad5a78a8850011070f961096426ff2ce93790e70bc6e2`

```dockerfile
```

-	Layers:
	-	`sha256:5895cf7711c3c5dece548129739746ed74a2563dfd7772e8d4ae0b18a491cdfc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b3c95ed9fde271922828bdab3fec041a27ebb7c5b4aa3593f49cd5e8717de`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-python3-r-ubuntu`

```console
$ docker pull spark@sha256:a73594c0a6266dd44f90d9bc4600bf337d563d4cf6b8914d346284eb36288a2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:0ead2a17874564fde47fb846f3a6add4b58dfbcb47b2ce282aada1074f1876c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.5 MB (695458352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a36fcaebbe0667d6a09d43e96b7527ec9627ac4ec70a1b01eb1fd9d51b4a12`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8897f0bdb3bcc40e1381dc78c29d0764416a9c8e4d488d8c47a0a34cf1df57b`  
		Last Modified: Thu, 10 Oct 2024 17:51:14 GMT  
		Size: 253.9 MB (253921806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:c04e64bfaf1eceba4170c1d248e4f0b9344fe3081f1e4b9fc56595c65ff6f3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12311903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd667102cf12c8005eb724df55c59915fc812e472c836dad3c16d26e337ebf8`

```dockerfile
```

-	Layers:
	-	`sha256:fca34fb3814193d5d9c3239fe5f3e7ee9d58ac8d2d868b349af58024375687ab`  
		Last Modified: Thu, 10 Oct 2024 17:51:10 GMT  
		Size: 12.3 MB (12301390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b964d68b898280e07c939a24e7c5756fc737390d49961249c6f1180be38f4cfe`  
		Last Modified: Thu, 10 Oct 2024 17:51:10 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:792836aafb3c37ad4493ffdef88355bec711284b14826d3c3e6dced0684c7bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.2 MB (673242521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfc6dc4e72b1fe34e906cdddae7af32e3a288587230fbed842c44fccbe93992`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19e50cbbcc6fe86ec6fae825cd86e3444cdb2f10febcd9aa129d4accd653a7`  
		Last Modified: Thu, 10 Oct 2024 17:57:31 GMT  
		Size: 235.1 MB (235147769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:8c8fc40a936bd9813c8f5313dd2e5d3d8ce246104b6c459c649c7efcd4e3dd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12296526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33255fee3ae2f127151e5f808d210cd1e50934225fe23f1271536e8676663d2a`

```dockerfile
```

-	Layers:
	-	`sha256:876adce8872d0722225d159447ad171c8a0e5135fb123a8875a46ed938f79279`  
		Last Modified: Thu, 10 Oct 2024 17:57:23 GMT  
		Size: 12.3 MB (12285884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7942576212ffcd2e43c8271b916e388b108f06b1a75bb5c3a58440ddd2606cbc`  
		Last Modified: Thu, 10 Oct 2024 17:57:22 GMT  
		Size: 10.6 KB (10642 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-python3-ubuntu`

```console
$ docker pull spark@sha256:f9632407249cc8b4d3e889e86b6df17e85c0e6cb24ea138eb440c408a4f95e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fe6222480d459e09a546e0f23facb7ceb2da5aa3fbc4c751556d3b601e3ce735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535909762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157f30b6c76c836b874ee482f7579478aff604f19149117a44e4245f398ad93`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22faaabba23eb151412e244d9f07351a2536bd6379069915f5a190b158d470`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 94.4 MB (94373216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:47b8ee21a8339c70023b7b27196932d3bd46557144736c6355a53b4c7af46f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da073156fbd1c48888ab3e38c9127edf9e7a3a6c0599bd77647a07d5a447a57f`

```dockerfile
```

-	Layers:
	-	`sha256:e88cd75ff8b3fc07be0a67c81d7692f335870729b18eede09defa26dc30e5ea9`  
		Last Modified: Thu, 10 Oct 2024 17:50:35 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d943fa4dd5eb865fd6b0b6f8fe8e96e57dde593dd66f3421df9348997731ece1`  
		Last Modified: Thu, 10 Oct 2024 17:50:34 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cc88b9b7dff73d804b684f2148d8fa22e4f184c8af9d7bac6b2b6e0a27bf3887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525424754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c0f60b3fd8a1c3eb7ee05625e184e93296e1181b879a13bd197f3c5075404b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834e25b1fdecf400ed4c97e4303666572437c4e246679754f7ee6c25ce0c5a5`  
		Last Modified: Thu, 10 Oct 2024 18:01:55 GMT  
		Size: 87.3 MB (87330002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:a199d5a0a336f948129f9634ea7ad3132ca4c12a4142242f40237894ccbfdd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a83d9152b13a75ecb34d76666c6e32e2447f3a4027938849d7a8c794dd9c9a`

```dockerfile
```

-	Layers:
	-	`sha256:08fbf8ecd311e701ecbdc6e7dd1aa94eb6f922f69839eaa447c475f8516f7f33`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c54d20ead64ba8c4c871d1d7b31c1c52975e1ba1737998193765cf162221f6`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-r-ubuntu`

```console
$ docker pull spark@sha256:1a59cf771ed941c79f5806fa97bffe25dececa3bb375e742db14101c9139df30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:120d5b971bb083abb0a19d7b2d35b6a530c2dbf2b7c6dc1de3ec0ebd4dd0e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673835815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046bd7ad09381484ae4dcdaa1e77b77b5b2b50ea91a80abcb457e4419fcccfdc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ec65aab84c9d063fafcab6440221038b276f48f7ec7f279d4cff91ea879fc`  
		Last Modified: Thu, 10 Oct 2024 17:51:03 GMT  
		Size: 232.3 MB (232299269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:99980c1561759bf1b3158631466eb82eef0b65d0bcd5f9504ff70e1ac04c5a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11189423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285a766f5770c129be758b6c6b603d4a323203430e5a01238e9130e1aa519c0`

```dockerfile
```

-	Layers:
	-	`sha256:d4c9726585014b5dbaf80dca3642fde69cf3f4ad6438e8f767e191b9af4cefba`  
		Last Modified: Thu, 10 Oct 2024 17:51:01 GMT  
		Size: 11.2 MB (11178500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9383401e0e16a27f0a7ad8551bd6d456e2a129177cea97435f88441f45df81`  
		Last Modified: Thu, 10 Oct 2024 17:50:59 GMT  
		Size: 10.9 KB (10923 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ebcb1944e4cd26537f3991c3a4d1d91fb726a18d8e986fb45a3ace9450085af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651603751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e106ef8fcf83084297feb9f84369bf27087f997532ca0a8f95568945ce6505a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e5784522b120123ce82c87564ac17c54e1c9ad3f25c849b145ace886e5af2`  
		Last Modified: Thu, 10 Oct 2024 18:03:37 GMT  
		Size: 213.5 MB (213508999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:be936d3ccfb8840dba070cc9faa8c3a800804a720b20b7f63549453b7b276f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11174026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c94e08d7243d1b98042da8160277491585cbee6e313fa074c2daaa5388d5cc3`

```dockerfile
```

-	Layers:
	-	`sha256:35d65347af080febae54fb710ba2dac35e4b0a4fc06242fcc6922f1bc475d1f9`  
		Last Modified: Thu, 10 Oct 2024 18:03:32 GMT  
		Size: 11.2 MB (11162951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252ae9b7292a410118277a97d2eabb2c8a44dbcda97f1f2f21eee44e68db45dc`  
		Last Modified: Thu, 10 Oct 2024 18:03:31 GMT  
		Size: 11.1 KB (11075 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java11-ubuntu`

```console
$ docker pull spark@sha256:e8877d2e8140931649910eec3bc45042665467423a0a8cd294624a1b341a4f85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java11-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:32ce1aa7d3d75f1c0d1c217e85017e5d11a95d68ee5cec5bc071736c6a8c5b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441536546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336f1c2ab53718832db7c723b320ab9ffc54efe57ec1d64b16edbe32b8c6535a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:90a4018752845e0f4594b403b46674ceb032679e525bb9c6fb1f38f4c0d70877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6f4ffab80da12d02458adcc6dcf145d0061f6b164e86f005bb4d6758d79604`

```dockerfile
```

-	Layers:
	-	`sha256:d780b92754f75ef32015189ce89011be4a7f197b27a12b2962fe0a8516b9cba9`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be458b2b8b65ba413fb3f25b6d8511c07fe87f9c299261aad4f2e5f780adc919`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 23.1 KB (23127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java11-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fe2510cee6f908606bfd7f6d73e25b46d7ed5339b78b1986781f99e77c37fd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438094752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9add04dfea1fee747d00b8612bda54b4cc72fb2511361d3a5041955ac34f3e3b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java11-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:11a7adadcdfa8d589093ba60954637aef6a049a2b5630ca5aaafa4197d262b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9db13bcd33be01e09ad5a78a8850011070f961096426ff2ce93790e70bc6e2`

```dockerfile
```

-	Layers:
	-	`sha256:5895cf7711c3c5dece548129739746ed74a2563dfd7772e8d4ae0b18a491cdfc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b3c95ed9fde271922828bdab3fec041a27ebb7c5b4aa3593f49cd5e8717de`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-python3-r-ubuntu`

```console
$ docker pull spark@sha256:0bade7dc19e90e96854bcdef4949300179422d057969341b3759ea0cf2500863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:fb077f2b4dc7ded523670d84eac9b971816b84203bc315d0f82ab4f5e9b9b4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.0 MB (876975134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aaf4cc99c41add390c6ed8a17d62464c94db3cb21d290debfa66db5317829a`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd2f8a9397bb2d738a5a361d296f5c0c22693db1be71a0eb47fc2921f98824b`  
		Last Modified: Thu, 10 Oct 2024 17:51:30 GMT  
		Size: 334.2 MB (334171320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:09edcc0327b0f886003a2edd4a8b245fa1c96a91ffa95bd04f4731646ab5b443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18936585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f122dd5b17ff082dec918ba8882542bc23ce60c505d26bd6ef5fa84a69c1fe21`

```dockerfile
```

-	Layers:
	-	`sha256:df616e779a7225e53a2c4b5cdcfe397157d517dfa14bfdc2007a9467c66c487c`  
		Last Modified: Thu, 10 Oct 2024 17:51:26 GMT  
		Size: 18.9 MB (18926068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fffac368acc23857e74d2ea50626be533b15e6a00e456e65f60eac11040466e`  
		Last Modified: Thu, 10 Oct 2024 17:51:26 GMT  
		Size: 10.5 KB (10517 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:5c23021740e3392be45ed26bfb0981da490f5d61f66bb0f158023df8fa9cff96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.8 MB (857812593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e508617e10cb5240133ecab1e85380e6e1c7fe72f19fd92a2f69a65e4e363`
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
RUN set -ex;     apt-get update;     apt-get install -y python3 python3-pip;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da58a8fe88be0afdb045b790cc019b462445200d9da42dc5baf42fc4f367ec72`  
		Last Modified: Thu, 10 Oct 2024 17:52:36 GMT  
		Size: 317.2 MB (317185027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e4d65a7d0357b8679b88e8e26926b816383dfcebdd21ccdd3eb66420a836ce8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18902445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0b7303809f3bff0805f28d53c782812ccba3d0ce34cee1365979f4b7d5a00e`

```dockerfile
```

-	Layers:
	-	`sha256:51ade7b1ea6f1222bbb6a76fbd6f4e51b1e8d779d53f5350d76fb85a670e37b6`  
		Last Modified: Thu, 10 Oct 2024 17:52:29 GMT  
		Size: 18.9 MB (18891801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9247998b54cecbdf300dff034ff430f7dd48967e51b00b41193813788acc942`  
		Last Modified: Thu, 10 Oct 2024 17:52:28 GMT  
		Size: 10.6 KB (10644 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-python3-ubuntu`

```console
$ docker pull spark@sha256:15fd585bd079757bea4b95d32156f3c9c2aa65ad4569a98b8f60d03bb3e09f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:45b46e330c1ad9a13c069ee4c6d6cf8a90dfe80eeef91b79c3f3c30a23f22a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.7 MB (656691105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b578b1aabc200732eb84fa21de9f835eca39f491c6f0b84163212c939c2ad6b6`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0664f69259dddc403e624d449dcec1834771d756f72768daab7d705813bc72`  
		Last Modified: Thu, 10 Oct 2024 17:50:39 GMT  
		Size: 113.9 MB (113887291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f6e28bdb4cb5d62ce310359b7584ef422b69d69985fc201e48e365f1a518d09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80d64de68c00422f14d9610bc0867bc064da5980378a35a42b70431d1137860`

```dockerfile
```

-	Layers:
	-	`sha256:3c8c89cb79640af82d8d7cfeb005cfe1aa956b93824fd40aa78e9f8e5612aa14`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 9.9 MB (9888571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a2c6774e534bde5335ca7a0207e90ac1e28bc4c8c94519126da1fc76ae074`  
		Last Modified: Thu, 10 Oct 2024 17:50:36 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:150cdde64ab677a2df5594a55360de116f9a1329d4e871e3529e96791f484381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649059495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21247e8844b41c4799aec04308838509c6643738ecfc2b20bb25fb003c4fe327`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7cd4ea97e9d886fc3526508027981465b1f7a9a95d852fb94b55e5e4615bc`  
		Last Modified: Thu, 10 Oct 2024 17:58:40 GMT  
		Size: 108.4 MB (108431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-python3-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:e476248bd888d0ddb22c4be5322efbf617c973bbabfaf46819aaa1e6a0f6f942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c0d37c05374dd3a64168f1a671606da6a31ce3a73dd6bbf1f0793f0ecbf1ac`

```dockerfile
```

-	Layers:
	-	`sha256:8e2874da8a7497166ff6427ddf2be01490b0ed58997a8a60ec8e7d4c71debc16`  
		Last Modified: Thu, 10 Oct 2024 17:58:38 GMT  
		Size: 9.9 MB (9883018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29817cb171189faf238e212ee6415e46ceae76f58965f3f1c3a853cdb286f102`  
		Last Modified: Thu, 10 Oct 2024 17:58:37 GMT  
		Size: 11.4 KB (11447 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-r-ubuntu`

```console
$ docker pull spark@sha256:51559788ad1d9a9dcb202e0b6ea9b4bdc256d94056d55ae9ae2baaefba9e9e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:bc0042179ecc589a16f7cc932022c68bc39319bb428dccf9d30a9e7a060dcf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.1 MB (862113442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da9f733f36c7b4adfbf0703f197723e348b5112291670ee2795e339004c0806`
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c130b12258fbe67cb351cc36dd3628adc8380c15149c13b1a2858d408f2e95`  
		Last Modified: Thu, 10 Oct 2024 17:51:26 GMT  
		Size: 319.3 MB (319309628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:bcc42ba94f61f1c0c13c77922f548fb376590a9706e493f3eb9db8cb4d9a67b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17924792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4312eca0395866eb277fbded0f890ac4bef52d73c90db509d6998227c3278150`

```dockerfile
```

-	Layers:
	-	`sha256:e77f1313a8b577ad9581e39c202190d7a5e12cdd54427eac77e6284f26dd0317`  
		Last Modified: Thu, 10 Oct 2024 17:51:21 GMT  
		Size: 17.9 MB (17914140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43550b113405e9c8847397db471f66b01f1cbb2adc12d9959d0f725465cdd95c`  
		Last Modified: Thu, 10 Oct 2024 17:51:21 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:771af0da2711d25b41f9751e640c5b91f763fc736b1549889079487d03736f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 MB (843106891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691cc8a5a33b83f1f115374196db41932a9b4f2d5cbf0b0181f10155a32ed118`
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f096e6c54686da60760a9569ab5facf860749535c002e2c21de1bd3ca17847`  
		Last Modified: Thu, 10 Oct 2024 18:00:54 GMT  
		Size: 302.5 MB (302479325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-r-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:60764fc7a7235f409a8eda79b0f0f93b61053af6c5c4a76b564393376bfa3254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17890654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b91ae301b4fb43881a399ed481d5a80242746e361c217afc90f6abe3e384b97`

```dockerfile
```

-	Layers:
	-	`sha256:3228f8de36649929832282605e04ed7de312d9c092f6f00fe0112149cae783a1`  
		Last Modified: Thu, 10 Oct 2024 18:00:47 GMT  
		Size: 17.9 MB (17879861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f5b3d2de8a8669d565f24cd2cd968f611d0a6f0f8d9d1acb1ff1b893feb041`  
		Last Modified: Thu, 10 Oct 2024 18:00:46 GMT  
		Size: 10.8 KB (10793 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:3.5.3-scala2.12-java17-ubuntu`

```console
$ docker pull spark@sha256:932058bc6de36f513383244a3b66df8b002f719c6fb1de87ace58484b2402052
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:3.5.3-scala2.12-java17-ubuntu` - linux; amd64

```console
$ docker pull spark@sha256:554187eefc46a16620714e0d3ec45913b6cab6151bbeb2a82de6da5f1b893003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542803814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4bfbcc24a0230566b6f0d0f3699661aaaa4c3aae8191b97a93af91a128460c`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:f76fd50070bafba195836260047b26fb37155c0fa81db54105aa3684eef549ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4547120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d945b649bc4735a7a18ff29156798d998f3ce0c46e2e9e71dfc3298d528f9852`

```dockerfile
```

-	Layers:
	-	`sha256:6d7e02d7413a7a6b77abbe0d53e6b29246a7e8590320f8cde635f3eb1ec163ff`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 4.5 MB (4524288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7feb9145fc932e1d0e86f2ee1ed05f200bdd20b94bed9eb3607da382988c9f`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 22.8 KB (22832 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:3.5.3-scala2.12-java17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:76ff7dce22dae9397b9ca9ffcec68a6e300c7785a7e3d78d9c0963d6469c459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.6 MB (540627566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ed409e77bd89735c98a6385658126752c8590c7205dbb97a3af3b10db8b1ff`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:3.5.3-scala2.12-java17-ubuntu` - unknown; unknown

```console
$ docker pull spark@sha256:696d7b3a5d11e26ab1910e9a4add00fe82929305c5b1c65eaa056ed734b92244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632cd49f3194cab7f06680a9af698a2f621c7b742acda24738c7aae7826d088`

```dockerfile
```

-	Layers:
	-	`sha256:ee8076eea28c81b43cd9d6b3b8ba7bf35eddf69076fa22c940d9f047d5a03050`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 4.6 MB (4619903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a73d62ef6f28ee89f05c7cd116751885b3258a0e517ab521966ef6016b8698`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 22.9 KB (22937 bytes)  
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
$ docker pull spark@sha256:f9632407249cc8b4d3e889e86b6df17e85c0e6cb24ea138eb440c408a4f95e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:latest` - linux; amd64

```console
$ docker pull spark@sha256:fe6222480d459e09a546e0f23facb7ceb2da5aa3fbc4c751556d3b601e3ce735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535909762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157f30b6c76c836b874ee482f7579478aff604f19149117a44e4245f398ad93`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22faaabba23eb151412e244d9f07351a2536bd6379069915f5a190b158d470`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 94.4 MB (94373216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:47b8ee21a8339c70023b7b27196932d3bd46557144736c6355a53b4c7af46f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da073156fbd1c48888ab3e38c9127edf9e7a3a6c0599bd77647a07d5a447a57f`

```dockerfile
```

-	Layers:
	-	`sha256:e88cd75ff8b3fc07be0a67c81d7692f335870729b18eede09defa26dc30e5ea9`  
		Last Modified: Thu, 10 Oct 2024 17:50:35 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d943fa4dd5eb865fd6b0b6f8fe8e96e57dde593dd66f3421df9348997731ece1`  
		Last Modified: Thu, 10 Oct 2024 17:50:34 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:latest` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cc88b9b7dff73d804b684f2148d8fa22e4f184c8af9d7bac6b2b6e0a27bf3887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525424754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c0f60b3fd8a1c3eb7ee05625e184e93296e1181b879a13bd197f3c5075404b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834e25b1fdecf400ed4c97e4303666572437c4e246679754f7ee6c25ce0c5a5`  
		Last Modified: Thu, 10 Oct 2024 18:01:55 GMT  
		Size: 87.3 MB (87330002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:latest` - unknown; unknown

```console
$ docker pull spark@sha256:a199d5a0a336f948129f9634ea7ad3132ca4c12a4142242f40237894ccbfdd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a83d9152b13a75ecb34d76666c6e32e2447f3a4027938849d7a8c794dd9c9a`

```dockerfile
```

-	Layers:
	-	`sha256:08fbf8ecd311e701ecbdc6e7dd1aa94eb6f922f69839eaa447c475f8516f7f33`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c54d20ead64ba8c4c871d1d7b31c1c52975e1ba1737998193765cf162221f6`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3`

```console
$ docker pull spark@sha256:f9632407249cc8b4d3e889e86b6df17e85c0e6cb24ea138eb440c408a4f95e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3` - linux; amd64

```console
$ docker pull spark@sha256:fe6222480d459e09a546e0f23facb7ceb2da5aa3fbc4c751556d3b601e3ce735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.9 MB (535909762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157f30b6c76c836b874ee482f7579478aff604f19149117a44e4245f398ad93`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a22faaabba23eb151412e244d9f07351a2536bd6379069915f5a190b158d470`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 94.4 MB (94373216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:47b8ee21a8339c70023b7b27196932d3bd46557144736c6355a53b4c7af46f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9034693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da073156fbd1c48888ab3e38c9127edf9e7a3a6c0599bd77647a07d5a447a57f`

```dockerfile
```

-	Layers:
	-	`sha256:e88cd75ff8b3fc07be0a67c81d7692f335870729b18eede09defa26dc30e5ea9`  
		Last Modified: Thu, 10 Oct 2024 17:50:35 GMT  
		Size: 9.0 MB (9023159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d943fa4dd5eb865fd6b0b6f8fe8e96e57dde593dd66f3421df9348997731ece1`  
		Last Modified: Thu, 10 Oct 2024 17:50:34 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:cc88b9b7dff73d804b684f2148d8fa22e4f184c8af9d7bac6b2b6e0a27bf3887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525424754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c0f60b3fd8a1c3eb7ee05625e184e93296e1181b879a13bd197f3c5075404b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834e25b1fdecf400ed4c97e4303666572437c4e246679754f7ee6c25ce0c5a5`  
		Last Modified: Thu, 10 Oct 2024 18:01:55 GMT  
		Size: 87.3 MB (87330002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3` - unknown; unknown

```console
$ docker pull spark@sha256:a199d5a0a336f948129f9634ea7ad3132ca4c12a4142242f40237894ccbfdd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a83d9152b13a75ecb34d76666c6e32e2447f3a4027938849d7a8c794dd9c9a`

```dockerfile
```

-	Layers:
	-	`sha256:08fbf8ecd311e701ecbdc6e7dd1aa94eb6f922f69839eaa447c475f8516f7f33`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 9.0 MB (9027089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c54d20ead64ba8c4c871d1d7b31c1c52975e1ba1737998193765cf162221f6`  
		Last Modified: Thu, 10 Oct 2024 18:01:53 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:python3-java17`

```console
$ docker pull spark@sha256:15fd585bd079757bea4b95d32156f3c9c2aa65ad4569a98b8f60d03bb3e09f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:python3-java17` - linux; amd64

```console
$ docker pull spark@sha256:45b46e330c1ad9a13c069ee4c6d6cf8a90dfe80eeef91b79c3f3c30a23f22a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.7 MB (656691105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b578b1aabc200732eb84fa21de9f835eca39f491c6f0b84163212c939c2ad6b6`
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
	-	`sha256:071ef8e2de16917dc03937126e901fe29a753f29c0e25f2b31036e25cf9fa907`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d6625ac2cf807944cad7794e314c98c8ebf53c491a51b822212a3993a5d639`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 24.9 MB (24897096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d06ebbc7d4d584f0b3dd48eb7004e50978f71f1d8a03e28546b07a62dcef7`  
		Last Modified: Thu, 10 Oct 2024 16:57:19 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9131059daf09574d15cb0364c8419cffbec0ad325b5b4c3ca24c30315f5ee6ad`  
		Last Modified: Thu, 10 Oct 2024 16:57:15 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0664f69259dddc403e624d449dcec1834771d756f72768daab7d705813bc72`  
		Last Modified: Thu, 10 Oct 2024 17:50:39 GMT  
		Size: 113.9 MB (113887291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:f6e28bdb4cb5d62ce310359b7584ef422b69d69985fc201e48e365f1a518d09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80d64de68c00422f14d9610bc0867bc064da5980378a35a42b70431d1137860`

```dockerfile
```

-	Layers:
	-	`sha256:3c8c89cb79640af82d8d7cfeb005cfe1aa956b93824fd40aa78e9f8e5612aa14`  
		Last Modified: Thu, 10 Oct 2024 17:50:38 GMT  
		Size: 9.9 MB (9888571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840a2c6774e534bde5335ca7a0207e90ac1e28bc4c8c94519126da1fc76ae074`  
		Last Modified: Thu, 10 Oct 2024 17:50:36 GMT  
		Size: 11.3 KB (11283 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:python3-java17` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:150cdde64ab677a2df5594a55360de116f9a1329d4e871e3529e96791f484381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649059495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21247e8844b41c4799aec04308838509c6643738ecfc2b20bb25fb003c4fe327`
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
	-	`sha256:0711512eafc93885c200c63ca48e59e65b7ebbc29f38455c344b74767d5cbcc0`  
		Last Modified: Thu, 10 Oct 2024 17:22:33 GMT  
		Size: 324.9 MB (324868544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5854145c9c175e1e50f2ed5977bf62002db8efee7c2ba56f94fc122ea39fd87`  
		Last Modified: Thu, 10 Oct 2024 17:22:26 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7cd4ea97e9d886fc3526508027981465b1f7a9a95d852fb94b55e5e4615bc`  
		Last Modified: Thu, 10 Oct 2024 17:58:40 GMT  
		Size: 108.4 MB (108431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:python3-java17` - unknown; unknown

```console
$ docker pull spark@sha256:e476248bd888d0ddb22c4be5322efbf617c973bbabfaf46819aaa1e6a0f6f942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c0d37c05374dd3a64168f1a671606da6a31ce3a73dd6bbf1f0793f0ecbf1ac`

```dockerfile
```

-	Layers:
	-	`sha256:8e2874da8a7497166ff6427ddf2be01490b0ed58997a8a60ec8e7d4c71debc16`  
		Last Modified: Thu, 10 Oct 2024 17:58:38 GMT  
		Size: 9.9 MB (9883018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29817cb171189faf238e212ee6415e46ceae76f58965f3f1c3a853cdb286f102`  
		Last Modified: Thu, 10 Oct 2024 17:58:37 GMT  
		Size: 11.4 KB (11447 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:r`

```console
$ docker pull spark@sha256:1a59cf771ed941c79f5806fa97bffe25dececa3bb375e742db14101c9139df30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:r` - linux; amd64

```console
$ docker pull spark@sha256:120d5b971bb083abb0a19d7b2d35b6a530c2dbf2b7c6dc1de3ec0ebd4dd0e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673835815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046bd7ad09381484ae4dcdaa1e77b77b5b2b50ea91a80abcb457e4419fcccfdc`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ec65aab84c9d063fafcab6440221038b276f48f7ec7f279d4cff91ea879fc`  
		Last Modified: Thu, 10 Oct 2024 17:51:03 GMT  
		Size: 232.3 MB (232299269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:99980c1561759bf1b3158631466eb82eef0b65d0bcd5f9504ff70e1ac04c5a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11189423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285a766f5770c129be758b6c6b603d4a323203430e5a01238e9130e1aa519c0`

```dockerfile
```

-	Layers:
	-	`sha256:d4c9726585014b5dbaf80dca3642fde69cf3f4ad6438e8f767e191b9af4cefba`  
		Last Modified: Thu, 10 Oct 2024 17:51:01 GMT  
		Size: 11.2 MB (11178500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9383401e0e16a27f0a7ad8551bd6d456e2a129177cea97435f88441f45df81`  
		Last Modified: Thu, 10 Oct 2024 17:50:59 GMT  
		Size: 10.9 KB (10923 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:r` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:ebcb1944e4cd26537f3991c3a4d1d91fb726a18d8e986fb45a3ace9450085af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.6 MB (651603751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e106ef8fcf83084297feb9f84369bf27087f997532ca0a8f95568945ce6505a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
RUN set -ex;     apt-get update;     apt-get install -y r-base r-base-dev;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Oct 2024 06:58:10 GMT
ENV R_HOME=/usr/lib/R
# Thu, 10 Oct 2024 06:58:10 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e5784522b120123ce82c87564ac17c54e1c9ad3f25c849b145ace886e5af2`  
		Last Modified: Thu, 10 Oct 2024 18:03:37 GMT  
		Size: 213.5 MB (213508999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:r` - unknown; unknown

```console
$ docker pull spark@sha256:be936d3ccfb8840dba070cc9faa8c3a800804a720b20b7f63549453b7b276f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11174026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c94e08d7243d1b98042da8160277491585cbee6e313fa074c2daaa5388d5cc3`

```dockerfile
```

-	Layers:
	-	`sha256:35d65347af080febae54fb710ba2dac35e4b0a4fc06242fcc6922f1bc475d1f9`  
		Last Modified: Thu, 10 Oct 2024 18:03:32 GMT  
		Size: 11.2 MB (11162951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252ae9b7292a410118277a97d2eabb2c8a44dbcda97f1f2f21eee44e68db45dc`  
		Last Modified: Thu, 10 Oct 2024 18:03:31 GMT  
		Size: 11.1 KB (11075 bytes)  
		MIME: application/vnd.in-toto+json

## `spark:scala`

```console
$ docker pull spark@sha256:e8877d2e8140931649910eec3bc45042665467423a0a8cd294624a1b341a4f85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `spark:scala` - linux; amd64

```console
$ docker pull spark@sha256:32ce1aa7d3d75f1c0d1c217e85017e5d11a95d68ee5cec5bc071736c6a8c5b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441536546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336f1c2ab53718832db7c723b320ab9ffc54efe57ec1d64b16edbe32b8c6535a`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
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
	-	`sha256:03e85a5c795fcd895df6a00fac561b2ac88ea6592d335794075bdb068a1caec6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc1bfe04566a36c1007351808e5cca8675ee80c5113be8dcabbda0c7fd39c95`  
		Last Modified: Thu, 10 Oct 2024 16:57:38 GMT  
		Size: 23.9 MB (23947138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d419c0615b95b47638dfc58a53aaf8d4ef6ac9cfa086c034669a2aca017371c`  
		Last Modified: Thu, 10 Oct 2024 16:57:42 GMT  
		Size: 324.9 MB (324868543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35081647c8a32a5be46cf37e8c9d202163768e6bc31b8631bddea32b0f63aa6`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:90a4018752845e0f4594b403b46674ceb032679e525bb9c6fb1f38f4c0d70877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6f4ffab80da12d02458adcc6dcf145d0061f6b164e86f005bb4d6758d79604`

```dockerfile
```

-	Layers:
	-	`sha256:d780b92754f75ef32015189ce89011be4a7f197b27a12b2962fe0a8516b9cba9`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 4.3 MB (4301046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be458b2b8b65ba413fb3f25b6d8511c07fe87f9c299261aad4f2e5f780adc919`  
		Last Modified: Thu, 10 Oct 2024 16:57:37 GMT  
		Size: 23.1 KB (23127 bytes)  
		MIME: application/vnd.in-toto+json

### `spark:scala` - linux; arm64 variant v8

```console
$ docker pull spark@sha256:fe2510cee6f908606bfd7f6d73e25b46d7ed5339b78b1986781f99e77c37fd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.1 MB (438094752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9add04dfea1fee747d00b8612bda54b4cc72fb2511361d3a5041955ac34f3e3b`
-	Entrypoint: `["\/opt\/entrypoint.sh"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:e13a4671218d26ae32083574b0dc03c2826a046bf3c35cf88b18419c67edd24b`  
		Last Modified: Thu, 10 Oct 2024 17:24:16 GMT  
		Size: 324.9 MB (324868561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587c909f7f7adeb10d9eb758db3743300e645ff8c06529b583410984fad63cc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 2.1 KB (2133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spark:scala` - unknown; unknown

```console
$ docker pull spark@sha256:11a7adadcdfa8d589093ba60954637aef6a049a2b5630ca5aaafa4197d262b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9db13bcd33be01e09ad5a78a8850011070f961096426ff2ce93790e70bc6e2`

```dockerfile
```

-	Layers:
	-	`sha256:5895cf7711c3c5dece548129739746ed74a2563dfd7772e8d4ae0b18a491cdfc`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 4.3 MB (4301349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b3c95ed9fde271922828bdab3fec041a27ebb7c5b4aa3593f49cd5e8717de`  
		Last Modified: Thu, 10 Oct 2024 17:24:09 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.in-toto+json
